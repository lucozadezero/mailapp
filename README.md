# MailApp

### Deployment Instructions
**1. log into your webserver using the following command <br />**
  &nbsp; `ssh <your-username>@<your-ip>`<br />
  &nbsp; for example if your server credentials are <br />
  ```
    username: root
    ip: 192.76.54.155
    password: abc123
  ```
  &nbsp; Then you enter `ssh root@192.76.54.155` and press enter. <br />
  &nbsp; &nbsp; &nbsp; &nbsp; If it asks to add fingerprint, just press enter. <br />
  &nbsp; &nbsp; &nbsp; &nbsp;  When it asks for password, enter your password <br />
  &nbsp; &nbsp; &nbsp; &nbsp; **Note: characters entered are not visible on screen when entering password. But do not worry, they are still being entered**
  
<br />
<br />
    
    
**2. Once you are logged in, enter the following command<br />**
  &nbsp;  `apt install unzip` <br />
  &nbsp;  this will be used to unzip the deppolyment package<br />
  
<br />
<br />

**3. Clone the repo using the following command<br />**
  &nbsp;  `git clone https://github.com/zrdplpst/mailapp.git`
  
  &nbsp;&nbsp; you will need to enter *your own* github username and password to clone this repo
 
<br />
<br />

**4. Run the following commands**<br />
&nbsp;  `cd mailapp`<br />
&nbsp;  `unzip deployment_package.zip`<br />
  
<br />
<br />

**5. Once the unzip is complete, run the following commands to set up your webserver**<br />
&nbsp;  `cd installer_script`<br />
&nbsp;  `chmod +x ./install.sh`<br />
&nbsp;  `./install.sh | tee out.txt`<br />

 &nbsp;&nbsp;   **Note: This will take a while and server will shut down once this is compplete.** <br />
 &nbsp;&nbsp;   **You need to wait ~1 minute after this is complete and log in again like you did at step 1**
 
 <br />
 <br />
 
 **6. Once you are logged in again, run the following commands**<br />
 ```
 cd mailapp/installer_script
 `chmod +x ./postinstall.sh`<br />
 ./postinstall.sh | tee postinstall.txt
 ```
 &nbsp;&nbsp;   **Note: at the end of this command, you will be given your email and password to login.**<br />
 &nbsp;&nbsp;   **Please remember these credentials as you will need these to login**<br />
 
 ### 🎉🎉You can now open your webserver IP in browser and log in🎉🎉
