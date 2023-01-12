# Platform : VPS/VM (GroomIDE) | Free Deployment
This repository contains instructions for deploying the Queen Amdi userbot in groomIDE.

- First of all you have to edit <b>.env-example</b> file like this.<br><br>
<img src="https://i.ibb.co/16xKy1m/image.png"><br><br>
- Then create an account on <a href="https://ide.goorm.io/">GroomIDE.</a> Then follow the steps; <br><br>
<img src="https://i.ibb.co/1rLZCBt/image.png"><br>
<img src="https://i.ibb.co/jg8z5xS/image.png"><br><br>
<b>Don't forget to check the availability of your repo</b><br><br>
<img src="https://i.ibb.co/1Jcwrqz/image.png"><br>
<img src="https://i.ibb.co/wCtfkZJ/image.png"><br><br>
- Now create your container. After the process done, Click on the <b>Run terminal</b> icon.<br><br>
<img src="https://i.ibb.co/CWnhY3g/image.png"><br><br>
# Now copy and paste this commands in your terminal.
   1. Install git ffmpeg curl 
      ```
       apt -y update &&  apt -y upgrade 
       apt install ffmpeg -y
      ```
      
   2. Install yarn
      ```
      curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - 
      echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
      apt -y update && apt -y install yarn
      apt install --no-install-recommends yarn
      ```
      
   3. Clone Repo and install required packages
      ```
      git clone *Your Github Clone repo link*
      cd QueenAmdi
      npm install
      npm run package
      npm run pm-run
      ```
      
- Scan and Connect your bot.<br><br>
- If you're facing any connecting problem after scanning the QR code, Use this commands to restart your bot.<br>
  ```
  cd QueenAmdi 
  pm2 restart QueenAmdiMD
  ```

