<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution </h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2)

<h2>Ticket Lifcycle Stages</h2>

- Stage 1
- Stage 2
- Stage 3
- Stage 4
- Stage 5

(Images going from left to right)
<h2>Installation Steps</h2>

Stage 1
<p>
<img width="1385" alt="Screenshot 2023-09-27 at 4 38 37 PM" src="https://github.com/lucasfregoso/ticket-lifecycle/assets/144977615/66d3b0ad-6a7b-4ac5-8b49-fe500cc79816">
</p>
<p>
After the previous parts of our lab, we are finally ready to simulate a day to day example of a help desk professional and now we are going to make up some tickts as a user with common issues that may occur within their company, business, etc. We do this through Support Center and create a few tickets and put them into their respective category giving us (the ones doing the lab) to be able to differentiate which department and who is responsible for taking care of these tickets. 
</p>
<br />

Stage 2
<p>
<img width="964" alt="Screenshot 2023-09-27 at 4 50 06 PM" src="https://github.com/lucasfregoso/ticket-lifecycle/assets/144977615/b0f34ed4-9a2f-4986-be40-183685bb9604">
</p>
<p>
So we've created our list of tickets and have them all ready to be taken care of. Usually a manager or maybe a lead will assign such tickets, but as our lab is an example/practice for real world issues we will be the 'manager' and assign them to our users or our admin. So, this ticket was assigned to Jane Doe (the system administrator) and the issue was that 'most of her department was having issues with their current tablets' and their question was when are they going to get a hardware refresh? After seeing this, we can determine that this a low priority as it falls under gereral inquiry, which wouldn't severely impact business in this case. Also, for the SLA Plan we could put this as SEV C and this is our longest timeframe to complete this ticket showing us that this again is not our top priority. However, we solved this problem by replying that they are scheduled for a refresh in Q1 and we let them know as well that they could email us if they have any questions.
</p>
<br />

Step 3
<p>
<img width="1631" alt="Screenshot 2023-09-25 at 10 43 42 PM" src="https://github.com/lucasfregoso/osticket-prereqs/assets/144977615/fc8f877c-09a6-4215-9a72-c84d62105201">
</p>
<p>
For the next part, we will install a few key requirements for out osTicketing System to function properly. So, from our instruction list we will install Rewrite Module by clicking on the link provided, go to 'downloads'in our files, open it up, agree to the terms/conditions, and install it. Then, we make a folder called 'PHP' on our c: drive, download 'PHP 7.3.8', onced it's downloaded we extract it into our PHP folder, and everything will get dumped into there. After this, we install both C++ Redistributable and MySQL Server.
</p>
<br />

Step 4
<p>
<img width="1631" alt="Screenshot 2023-09-25 at 11 37 12 PM" src="https://github.com/lucasfregoso/osticket-prereqs/assets/144977615/90859a89-c128-4aa0-b50b-c11c82a4eeb5">
</p>
<p>
Now, we open up IIS as an admin, register PHP from within the the IIS, restart it to make sure that it is registered, and then download the osTicket file from our list of instructions. Next, we extracted and copied the 'upload' (which came from the osTickett file we downloaded) folder into c:\inetpub\www.root and then renamed the 'upload' file to 'osTicket.' After this, we go back to IIS and go to sites-->Default-->osTicket and towards the very right we click 'Browse*:80', which will bring us to the 'osTicket installer' website and means we are on the right path. After this, we go back to IIS to enable some extensions since a couple of them will not be enabled at first. So, we go back to IIS and head to sites-->Default-->osTicket and double click on PHP Manager and enable the following: php_imap.dll, php_intl.dll, php_opcache.dll. 
</p>
<br />

Step 5
<p>
<img width="771" alt="Screenshot 2023-09-26 at 12 13 47 AM" src="https://github.com/lucasfregoso/osticket-prereqs/assets/144977615/07fc8e46-c92f-4750-9e52-0ba8dac20dc5">
</p>
<p>
Finally, we rename our root file to ost-config.php and assign permissions on this file so that everyone is able to do anything to this file since the osTicket installer needs to interact and maanipulate with this file. To do this we go properties from this file, go to security, then to advanced, disable inheritance, and remove all permissions. Afterwards, we add new permissions and allow 'everyone' to have full control. Then, we continue setting up osTicket and install Heidi SQL, which will allow us to connect the MySQL server that we installed earlier and set up a database that the osTicket is going to use. We create the database in Heidi SQL once it's downloaded and call it 'osTicket' and fill out the remaaining info on the osTicket installer website. Lastly, we'll get a 'congratulations' text if we did it right and after this we do a clean up to make everything comes full circle and login to make that works too.
</p>
<br />
Step 5 Continued
<img width="1525" alt="Screenshot 2023-09-26 at 12 14 57 AM" src="https://github.com/lucasfregoso/osticket-prereqs/assets/144977615/08c20dd6-774c-4f87-a5bf-7a208a784696">
