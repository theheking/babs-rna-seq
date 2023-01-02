---
layout: page
title: Week 1B Intro to Shell - Setting Up on Katana
---

Setting Up on Katana
=====================
# 2.The BABS teaching UNIX server

In this prac, we are going to work how many "real" bioinformaticians actually work: we are going to use a remote server for the computationally intensive bits and a user-friendly machine (Windows or Mac) to visualise and analyse the results downstream. We have a UNIX server set up for the prac:

babsteaching01.babs.unsw.edu.au

For many of you, this is your first time using UNIX. Fear not! You will pick up the important commands as you go. As with all bioinformatics, the best way to learn is by trial and error. There is little that you can do wrong, with one important caveat:

**READ THIS IF YOU DON'T READ ANYTHING ELSE!**
 Unix has  **no undo**  function. If you  **delete or overwrite**  a file, it will be gone forever! As a result, you should:
 1.    Keep  **backup copies**  of important files.
 2.    Be  **very careful**  with the command rm ("remove", i.e. delete) and any commands to move/create files that might over-write something important (mv, cp and redirecting output with \> and \>\>).
 3.    Use  **rm -i**  to provide an additional safety check against rogue deletion.
 4.     **Make sure that you keep good notes. ** Ultimately, it should be fairly straight-forward to regenerate anything from the starting data, provided you have adequate records of how you made it in the first place. This is one of the primary goals of keeping a lab book.

## 2.1.Setting up the UNSW VPN

To access the servers off-campus, you will need to set up the UNSW Virtual Private Network (VPN), which gives you access to University resources off-campus as if you were on-campus. Details to set this up can be found here: [https://www.myit.unsw.edu.au/services/students/remote-access-vpn](https://www.myit.unsw.edu.au/services/students/remote-access-vpn). Please contact UNSW IT if you have questions or experience problems with the VPN. If you have recurring issues, please let the course coordinator know. You do not need the VPN if using a UNSW machine on campus. (Recommended where possible.)

**Using private computers.**
It is not possible to write this handbook with clear instructions for all combinations of computers and software. As such, the handbook will be written as if you are using a UNSW desktop computer, and tested with off-campus Windows and Mac computers. Please let us know if you are experiencing technical issues through the prac chat channels and we will try to help where we can. However, it is ultimately the responsibility of the student to ensure access to a fit-for-purpose computer.

**The importance of windows real estate.**
 One thing you will quickly learn is the importance of being able to see clearly what you are doing. This generally means making the Putty/Terminal window much bigger than it opens by default. Ideally, you want it wide enough to avoid long commands and/or screen output wrapping onto multiple lines. You also want to see as many lines as possible to keep track of the context of what you are doing, and to make sure that important messages (particularly errors) do not disappear off the top of the screen. The precise way to resize your window will depend on your computer/software combination, but seek some advice during a prac session if you cannot find out how to do it.

**NOTE:** You will also find life easier with a bigger monitor – use the biggest screen/resolution that you can, especially when working with anything graphical.

## 2.2.Logging on to the system

You log on to the server using your **zID** and **zPass** and a program that lets you connect via a "secure shell (SSH)". On UNSW machines, we use a program called **Putty**. It's a free, standalone executable that you can download from https://www.putty.org/, or copy a downloaded version onto a windows computer and it should run fine. You If you use a Mac, you simply need to open the **Terminal**. Terminal is generally found in the "Other" folder in Launchpad, or just search for "Terminal" with Spotlight. Once open, **Keep in Dock** for handy future access.

### 2.2.1.Logging on the server with putty

On a UNSW machine, Putty is available from the start menu under PuTTY. This will open up the main putty window. In the **Host Name** box type: babsteaching.babs.unsw.edu.au. To save yourself having to type this again, you can **Save** the session as BABS3291 and later **Load** it. (If you change terminal settings, you can save these too.)

![](RackMultipart20230102-1-ssjimi_html_7d841837563056e4.png) ![](RackMultipart20230102-1-ssjimi_html_c7999a4b536a5c4b.png)

(NB. The screenshot shows connection to backup edwardsstudents01.babs.unsw.edu.au server and saves the session as BABS3151 for a different course.)

Hit **Open** and putty will try to connect to the server. The first time you try this, it will recognise the server as a new connection and check that you are sure (precise details may vary):

![](RackMultipart20230102-1-ssjimi_html_9058d0d57391a4b6.png)

Click **Yes**. The main terminal window will now open, prompting you to login as: . Enter your **zID** and (press **ENTER** ) then enter your **zPass** when prompted. (If this does not work, check your VPN is working.)

**NOTE:** For security reasons, you will not see anything appear on-screen when typing your password. Trust that it is registering and hit **ENTER** when complete.

### 2.2.2.Logging off

To log off the server, simply close the Putty window or type:

$ exit

### 2.2.3.Logging on from Mac OSX

To log on from Mac OSX (or a UNIX machine), open the Terminal and type at the prompt (replacing zID with your own **zID** ):

$ ssh zID@babsteaching.babs.unsw.edu.au

Enter your **zPass** when prompted. (If it doesn't work, check that you replaced zID with your own **zID**!)

**Logging on from outside UNSW.**
 Remember that to log on from outside UNSW, you will need to connect to the university virtual private network (VPN). See https://www.myit.unsw.edu.au/services/students/remote-access-vpn for more information.

### 2.2.4. What happens if the server fails?

Whenever working with servers, there is always the risk that something will go wrong. Fear not! We have contingencies (and back up data) in place in case something goes wrong. Please alert the course convenor and/or demonstrators if you start getting unexpected behaviour from the server.

**Saving your session and sanity with screen.**
 Whenever doing anything that will take a while, it is recommended that you use a utility called "screen", which will maintain an active session even if you log out or your connection to the server is dropped. You can read more about screen in the **Using screen (Advanced)** section after UNIX basics. The core elements are:

1. To start a new screen called "myscreen": screen -S myname

2. To "detach" the screen so you can re-attach it later and pick up where you left off: ctrl+a » d

3. To re-attached the screen "myname" after logging back on: screen -dr myname

## 2.3.Getting to grips with UNIX

This section will walk you through the basics of using UNIX and provide some sources for additional help. If you are already familiar with UNIX, feel free to skim through this section without doing all the exercises. However, you should still set up your home directory as directed. We'll worry about getting data on/off the server later.

### 2.3.1.Setting up the your home directory

The first task is to familiarise yourself with the system and to create a good directory structure to organise your work. For some of you, this will be easy and straight-forward. For others, you will be learning your first UNIX and it will take longer. Don't worry: there is plenty of time over the nine weeks.

When you first log on to the system, you will have an empty home directory. Use the command ls ("list") to see what is in there. (It should not return anything.) We will use your home directory as the primary place for generating new data, unless it's going to be big. Then we use scratch/, which we'll visit later.

**The command prompt.**
Remember that $ is the "command prompt" and we are using it to distinguish commands you type from "standard output" printed to the screen. If you include the $ when running a command, you will get an error like this:

bash: $: command not found

First, make sure that you are in your home directory. You can do this simply from anywhere with the cd ("change directory") command, without any additional arguments:

$ cd

This is the directory that you will be in when first logging on. You can check where you are with pwd ("path to working directory"):

$ pwd

/home/zID/

**NOTE:** This should show your zID, not literally "zID".

**zID and $USER**
 On the server, your username is your zID. A handy shortcut to this is the UNIX environment variable $USER. Where you see "zID" or "$USER" in commands and outputs throughout this manual, remember that this will be your zID when you run the commands. If a command fails, check you've not left a generic "zID" in there!

Now create a BABS3291-Jun22/ directory using  **mkdir**  ("make directory"):

$ mkdir BABS3291-Jun22

Note how this is named to match your Lab Book folder in LabArchives. Check that it is there with the "list" command  **ls**. You can see what is in it by giving the path to the same command:

$ ls BABS3291-Jun22/

Nothing should happen, as it should be empty! Also try:

$ ls babs3291-Jun22/

This time, you should get an error:

ls: cannot access babs3291-Jun22/: No such file or directory

UNIX is  **case-sensitive**. This is  **very**  important. Most bioinformatics programs are also case-sensitive. Indeed, case is sometimes used to convey extra information. If a command or program is not working for you, always check that you have no typos, including incorrect case.

**What the font?**
 Along with copy-and-paste auto-correct issues, you also need to be wary for characters that look very similar, e.g.

0 1 2 1 0

k l m N O

Within your **BABS3291-Jun22** directory, you now want to make analysis, code, data, docs and temp directories. You can either do that from your home directory:

$ mkdir BABS3291-Jun22/code

Or change your working directory first:

$ cd BABS3291-Jun22
$ mkdir docs

Using the full path (see below) enables you to do such things from anywhere, e.g.:

$ mkdir /home/$USER/BABS3291-Jun22/analysis

Now make the remaining data/ and temp/ directories. (We will cover how these directories will be used later.)
