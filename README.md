# Impact 2020 - App Pipelines in IoT

https://github.com/JockDaRock/impact19-cicd-ws

Before we get started we are going to install something on the desktop while the instructor is talking about what we will be learning.

* Open a terminal window and enter the following command

```bash
docker pull ciscodevnet/vs-cicd-ws-code:latest
```

# Guide of commands and code for the workshop

>Note: Make sure you are logged into the devnet sandbox VPN to complete this workshop. 

* Login to sites with creds... User: `test` Password: `test`

Drone `http://10.10.20.23`
Gogs `http://10.10.20.24:3000`

* In Gogs we will import our code. Follow along on the screen.  You will use the below URL to import our codebase.

```bash
https://github.com/CiscoDevNet/cicd-idpw-sample-code
```

* Next we will activate our repo.  Follow along with the instructor to activate the repo and drone connection.

* Login to Fog Director with creds... User: `admin` Password: `admin_123`

```bash
https://10.10.20.50
```

* Start the docker container we will use to connect to our lab content

* Open a terminal window and run the following command.

```bash
docker run -it -p 127.0.0.1:8443:8443 ciscodevnet/vs-cicd-ws-code:latest --allow-http --no-auth
```

* In your browser, navigate to `http://127.0.0.1:8443`.

From here on out we will work in the web based code editor and terminal.

* In the VS Code site open a terminal window

* In the that terminal window, import our codebase with the following command.

```bash
git clone http://10.10.20.24:3000/test/idpw
```

* Now follow the instructor (a.k.a JockDaRock) above to edit our CICD pipeline code and repository information for the pipeline build.

...
...
...
...
...

* On the terminal window change directories into our code repo folder

```
cd idpw
```

* Use git to add our user name and e-mail

```
git config --global user.email test@devnet.org

git config --global user.name test
```

* Run the following commands to push up our code.

```
git add --all

git commit -m "CICD Let's GO!!!"

git push origin master
```

The screen prompt will ask for username and password.  You will use the same test/test credentials you have been using for Gogs and Drone.

* Go back to then drone tab in your browser and view the build.

Now we will make a few changes to our code base to show how we can update our app.

If you want to give it another try after this workshop... visit the online DevNet Learning Lab for CICD w/ IOx apps.

https://developer.cisco.com/learning/tracks/iot/cicd-iox/iox-app-building-cicd/step/1

Also, below are are the code repos we used in the lab that you might find useful for your own automations.

https://github.com/CiscoDevNet/cicd-idpw-sample-code




