 //////////////////////////////////////////
  
  Rocket Chat Server
  
  URL - https://purplecheque.ga
  
  Email - rocket@gazzelle.onmicrosoft.com
  
  Username - rocket
  
  password - Rocketchat
  
  /////////////////////////////////////////
  

<b>INSTALLED ROCKET CHAT USING DIGITAL OCEAN (STEPS BELOW)</b>

-Log into the Digital Ocean platform; Go to the Market place and search for Rocket chat droplet

-Click on create rocket chat droplet  

-You would be redirected to a configuration page to specify the resources for the Rocket chat droplet. 

-You also have the option of choosing either to access your droplet using SSH keys or a password. 

-Choose a hostname and deploy

-Once deployed completely you would be provided with a Droplet IP to access your rocket chat server. Rocket chat works on port on 3000, So droplet-ip:3000 would give access to the server

-Fill up the Admin, Organization and Server info 

-------------------------------------------------------------------------------------------------------------

  <b>INTEGRATED GITHUB TO ROCKET CHAT</b>

-Open up the administration panel. 

-Click on the Integration tab and click new to create

-Add script on Integration tab to send notifications to the Github_updates channel. 

The script added will generate notifications for the following repository events, Issue events (create, edit, close, reopen, assign, label, etc), Issue comment events, Push events (singular and multiple commits

-------------------------------------------------------------------------------------------------------------

<b>INTEGRATED DOMAIN AND LET'S ENCRYPT SSL CERTIFICATE</b>
  
  -On Digital Ocean portal, Add a domain to the Rocket chat droplet
  
  -Log into Domain Portal and change A records to droplet-ip, change nameservers to nameservers specified in Digital oceaan
  
  -Add lets encrypt SSL certificate to domain using rocketchatctl configure --lets-encrypt --root-url=https://chat.yourcompany.com --letsencrypt-email=admin@yourcompany.com
  
  ------------------------------------------------------------------------------------------------------------
  
  <b>ROCKET CHAT API TEST</b>
  
  <b>Create a new user via an API endpoint</b>
  
  -To create a new user, you have to Login(Authenticate). You can also specify an Environment where https://purplecheque.ga the BASE_URL
  
  -Using Postman, To login perform a Post https://purplecheque.ga/api/v1/login request with a content type of application/json and username and password specified in the body
![image](https://user-images.githubusercontent.com/85682126/125151397-af958b00-e13d-11eb-8004-f41ac3303755.png)

  -Grab the User-ID and token, specify these as X-User-Id and X-Auth-Token. Then perform a Post https://purplecheque.ga/api/v1/user.create request, specifying the user details in the body tab as shown in the screenshot. The reponse file has also been uploaded as create_user_response
  ![image](https://user-images.githubusercontent.com/85682126/125151817-d4d7c880-e140-11eb-9251-24bb21c8c7a6.png)

  
   <b>Get the room information via an API endpoint</b>
  
  -Perform a Get api/v1/rooms.info request using ?roomName=general as params as we are getting information from the Rocket chat server. The response file has been uploaded as get_room_response
  ![image](https://user-images.githubusercontent.com/85682126/125151549-e3bd7b80-e13e-11eb-8c12-8fc9d064ce3a.png)

   <b>Get a list of all user roles in the system via an API endpoint</b>
  
  -We perform a Get /api/v1/roles.list request. This provides list of users alongside their roles from the server. The response file as been uploaded as get_role_response
  ![image](https://user-images.githubusercontent.com/85682126/125151453-1e72e400-e13e-11eb-9b65-c96f17140a2d.png)


