<div id="top"></div>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/TomProgrammingStudios/Remote_Admin">
    <img src="logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Remote Admin</h3>

  <p align="center">
    Easily control your Minecraft Server with this tool!
    <br />
    version 1.0.1
    <br />
    <br />
    <a href="https://github.com/TomProgrammingStudios/Remote_Admin">View Demo</a>
    ·
    <a href="https://github.com/TomProgrammingStudios/Remote_Admin/issues">Report Bug</a>
    ·
    <a href="https://github.com/TomProgrammingStudios/Remote_Admin/issues">Request Feature</a>
  </p>
</div>




<!-- ABOUT THE PROJECT -->
## About Remote Admin

I always dreamed of a simple and easy way to let my friends control my Minecraft Server, but without giving them access to Rcon. And with Remote Admin, you can do that too!

Here's why:
* Permission based system, to allow for different degrees of personalized access.
* Multiple user support, to have separate permissions for your Moderator.
* Easy to Use
* Featuring Secure SHA-256 encryption
* Support for Automatic server Boot/Shutdown
* Completely Free!

Now, let's talk a bit on how it works, shall we?

<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

This section should list any major frameworks/libraries used to bootstrap your project. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* Python 3
* Pyinstaller
* threading lirary
* pyaes library
* termcolor library
* pbkdf2 library
* pywinauto library
* some more libraries already included with python

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

The setup process for Remote Admin is quite simple, but it can get confusing. Let's walk you through slowly.

## Installation

1. Download the Remote Admin Server and Remote Admin Client folders.
2. Start the Remote_Admin_Server.exe file in the Remote Admin Server folder.
3. Once remote admin boots, it will fail to POST because no users have been set up.
4. You will be prompted to enter information by the line
   ```
   [User Setup] Please enter the minecraft username of this user:
   ```
5. Enter the username (using the minecraft ones is recommended) of the account you want to set up. After the configuration, you will be able to set up more.
   ```
   test_minecraft_username
   ```
6. You will now be prompted to enter a password for your user. He will use this password to access Remote Admin.
7. You will now be prompted to choose the permission nodes assigned to this user, explained now.

### Permission Nodes
1. "monitor": the user will se the server status (online, offline, shutting down); the player count (example 0/7)
2. "post_to_chat": the user can post messages to the Minecraft chat with his username, but he cannot perform commands.
3. "start_stop": the user can start and stop the server. Attention: in case of a server shutdown Abort, request will be denied if the user sending the Abort command does NOT have this permission.
4. "force_stop": the normal server shutdown has a built-in 60 seconds countdown to warn your users in the Minecraft Server. Grant this permission to bypass the sequence and shutdown the server immediatly.
5. "auto_start_stop": this permission allows the user to modify the server automatic start/stop times. If enabled, the Remote Admin Server instance will shutdown the server at a certain time and boot it up again at another time automatically. If automatic start/stop is not enabled, this permission will give the power to do so.
6. "console": BEWARE this permission gives full access to Minecraft Server Console commands, with no limitation. Do NOT give to everyone. By "no limitation" i mean that commands are executed as OP, not as that user's minecraft permission. Commands like "list" have no feedback.
7. "backups": this permission allows the user to make a backup of the server and save it in the server's directory. User will NOT have access to the file.
8. "backup_restore": this permission allows the user to reboot the server with a backup already made of the Minecraft Server.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTINUE SETUP -->
8. Remote Admin will ask you to review the user you just created, enter 'y' to confirm.
9. Some lines will appear, the Encryption Utility kicked in. It shows you some randomly generated encryption data, and asks for a password. This will NOT be seen by the users, and will secure the connection between the Remote Admin Server and the Remote Admin Clients over a network.
10. The encyption information will be saved, but Remote Admin won't start successfully because of a PORT error. Let's fix that.
11. Open the config file named 'config.txt' in the Remote Admin Server directory. In here, enter the port that you want to use Remote Admin on. DO NOT use <1024, 25565 or >65535. Also, while you're in here, paste the path to your server directory (something like C:/users/tom/dekstop/my_server) in the PATH= zone. The auto start and auto stop entries don't need many words, write an hour (24h format) or blank to turn off. example (auto_start=19:30)
12. Save and close the file.
13. Start Remote Admin Server again.
14. Start Remote Admin Client.
15. Remote Admin Client will enter the Configuration Mode automatically. Please wait 20 seconds. When prompted, enter the password that you used in step 9.
16. If you can, enter the encryption salt (from the server config file) or just write anything and change that in the config file.
17. If you can, enter the encryption iv (from the server config file) or just write some numbers and change that in the config file.
18. Enter the server IP of the Remote Admin Server (depends on how you connect, ngrok recommended. Check how to use ngrok on my youtube channel Tom's Corner.)
19. Enter the server PORT
20. Remote Admin client boots, connects to the server and prompts you to login with a valid account. Setup complete.
21. Give your moderators the Remote Admin Client folder, or the configuration file client_config.txt, they won't be able to communicate otherwise.

Video instructions on https://www.youtube.com/channel/UCsS7xRYQ9wPDH_3YmabLVKw/


<!-- USAGE EXAMPLES -->
## Usage

1. Start Remote Admin Server
2. Start Remote Admin Client
3. Login with Remote Admin Client

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better pen an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Tommaso Brignoli (Tom's Corner) - tommaso07brignoli@gmail.com

Project Link: [https://github.com/TomProgrammingStudios/Remote_Admin](https://github.com/TomProgrammingStudios/Remote_Admin)

<p align="right">(<a href="#top">back to top</a>)</p>
