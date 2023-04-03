Remote Access Services are used to access a system through internet without any physical access to it. Using Protocols like SSH (Secure Shell), VNC (Virtual Network Computing) , RDP (Remote Desktop Protocol).

**SSH** stands for **Secure Shell**. It was initially used in Unix-like systems for remote login. It provides the user with a command-line interface (CLI) that can be used to execute commands.

**RDP** stands for **Remote Desktop Protocol**; it is also known as Remote Desktop Connection (RDC) or simply Remote Desktop (RD). It provides a graphical user interface (GUI) to access an MS Windows system. When using Remote Desktop, the user can see their desktop and use the keyboard and mouse as if sitting at the computer.

**VNC** stands for **Virtual Network Computing**. It provides access to a graphical interface which allows the user to view the desktop and (optionally) control the mouse and keyboard. VNC is available for any system with a graphical interface, including MS Windows, Linux, and even macOS, Android and Raspberry Pi.

## Authentication

Authentication refers to the process where a system validates your identity. The process starts with the user claiming a specific unique identity, such as claiming to be the owner of a particular username. Furthermore, the user needs to prove their identity. This process is usually achieved by one, or more, of the following:

1.  **Something you know** refers, in general, to something you can memorize, such as a password or a PIN (Personal Identification Number).
2.  **Something you have** refers to something you own, hardware or software, such as a security token, a mobile phone, or a key file. The security token is a physical device that displays a number that changes periodically.
3.  **Something you are** refers to biometric authentication, such as when using a fingerprint reader or a retina scan.

Back to remote access services, we usually use passwords or private key files for authentication. Using a password is the default method for authentication and requires the least amount of steps to set up. Unfortunately, passwords are prone to a myriad of attacks.

## Attacking Passwords

Passwords are the most commonly used authentication methods. Unfortunately, they are exposed to a variety of attacks. Some attacks don’t require any technical skills, such as shoulder surfing or password guessing. Other attacks require the use of automated tools.

The following are some of the ways used in attacks against passwords:

1.  **Shoulder Surfing:** Looking over the victim’s shoulder might reveal the pattern they use to unlock their phone or the PIN code to use the ATM. This attack requires the least technical knowledge.
2.  **Password Guessing:** Without proper cyber security awareness, some users might be inclined to use personal details, such as birth date or daughter’s name, as these are easiest to remember. Guessing the password of such users requires some knowledge of the target’s personal details; their birth year might end up as their ATM PIN code.
3.  **Dictionary Attack:** This approach expands on password guessing and attempts to include all valid words in a dictionary or a word list.
4.  **Brute Force Attack:** This attack is the most exhaustive and time-consuming, where an attacker can try all possible character combinations.

Let’s focus on dictionary attacks. Over time, hackers have compiled one list after another of passwords leaked from data breaches. One example is RockYou’s list of breached passwords, which you can find on the AttackBox at `/usr/share/wordlists/rockyou.txt`. The choice of the word list should depend on your knowledge of the target. For instance, a French user might use a French word instead of an English one. Consequently, a French word list might be more promising.

RockYou’s word list contains more than 14 million unique passwords. Even if we want to try the top 5%, that’s still more than half a million. We need to find an automated way.

