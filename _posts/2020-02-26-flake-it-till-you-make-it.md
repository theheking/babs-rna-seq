###

| ![](RackMultipart20230102-1-ssjimi_html_2a17415f52006587.gif) |

 |
 |
| --- | --- | --- |

# Practical Handbook

Version 1.0

![Picture 8](RackMultipart20230102-1-ssjimi_html_e621248dcdc98f56.gif) ![](RackMultipart20230102-1-ssjimi_html_2e1d749d9fea873a.png) ![](RackMultipart20230102-1-ssjimi_html_75ac7f7a5a74c474.gif) ![](RackMultipart20230102-1-ssjimi_html_d30b0067d12711e1.png)

TERM 1, 2022

FACULTY OF SCIENCE

School of Biotechnology and Biomolecular Sciences

![](RackMultipart20230102-1-ssjimi_html_2e49155b3f5ba289.png)

Welcome to the bioinformatics practical for BABS3291 Genes, Genome and Evolution. The material in this handbook is designed to help guide you through the prac. However, as will quickly become apparent, it is impossible to be comprehensive and so you should complement this handout with the resources provided through Teams/Moodle, online help, and any other source of inspiration/advice that works for you.

As much as possible, I shall try to make a clear distinction between explanatory text (this) and text to be typed at the command prompt etc. Command prompt text and program options (also called 'command-line parameters') including file names will be highlighted fixed-width font to make the distinction clearer:

$ Command-line examples will be given in their own boxes, starting with "$". Like this!
 $ Optional parameters will be given [in square brackets].

Terminal output will be in the same format, without the leading $.

The use of the $ for command prompts is to be consistent with the companion text, Unix and Perl Primer for Biologists by Keith Bradnam & Ian Korf ([http://korflab.ucdavis.edu/Unix\_and\_Perl/index.html](http://korflab.ucdavis.edu/Unix_and_Perl/index.html)).

**NOTE:**  It is recommended that you also use a fixed width font (e.g. Consolas) and colour formatting when documenting code in your own lab books to help it stand out from other thoughts/instructions.

**Questions.**  You will find questions and extra activities scattered throughout the instructions. These are not assessed but will help you to understand the processes and associated theory lectures.

**Information boxes.**
 You will also find information boxes like this scattered throughout the manual. These contain general reusable hints and tips rather than specific topic commands etc. These will generally be repeated in the  **Tricks and**** Tips** section of the handbook and/or course site.

**Challenge:**  Some of the activities with have  **Challenge**  boxes. These are not assessed and are entirely optional but their completion will teach/reinforce new skills and/or improve your understanding of the science behind the activities. If you get stuck, we will give hints and/or answers through the course Teams site.

**Advanced activities.** Do not be daunted by the length of this prac manual! This is partly due to detailed walkthroughs of some sections, and partly due to the inclusion of several "Advanced" topics for those with more experience to attempt. Advanced topics will be helpful for getting the top marks, but are not required to complete the assignments.

**Contents**

**1. Prac Overview 6**

**1.1. Aims 6**

**1.2. Research Aims 6**

**1.3. Prac Timeline 7**

**1.4. Assessment 7**

1.4.1. Submission 7

**1.5. Electronic Lab Books 7**

1.5.1. Lab Archives 8

**2. The BABS teaching UNIX server 9**

**2.1. Setting up the UNSW VPN 9**

**2.2. Logging on to the system 9**

2.2.1. Logging on the server with putty 10

2.2.2. Logging off 10

2.2.3. Logging on from Mac OSX 10

2.2.4. What happens if the server fails? 11

**2.3. Getting to grips with UNIX 11**

2.3.1. Setting up the your home directory 11

2.3.2. Navigating the UNIX file system 13

2.3.3. UNIX file basics 13

2.3.4. Using temporary 'scratch' space 13

2.3.5. What to do when things go wrong 13

2.3.6. Harnessing the UNIX history 14

2.3.7. Using screen (Advanced) 15

2.3.8. Other UNIX tricks (Advanced) 15

**2.4. Copying data on/off the server with Filezilla 16**

**3. File naming and organisation 16**

**3.1. Project-level directories 17**

**3.2. Main directories 17**

**3.3. Subdirectories 17**

**3.4. File naming 18**

**4. BUSCO Gene Annotation 20**

**4.1. Fasta formats 20**

**4.2. Working with text files in UNIX 21**

**4.3. Exploring /share/data/ (Optional) 21**

**5. Homology Searching 22**

**5.1. Uniprot protein BLAST searches 22**

5.1.1. Making sense of the results 22

5.1.2. Getting more details 23

**5.2. Downloading proteins 25**

5.2.1. Why download sequences? 25

5.2.2. Adding fish 25

5.2.3. Download and save 26

5.2.4. Emergency files 26

**6. Multiple Sequence Alignment 27**

**6.1. Making a Multiple Sequence Alignment (MSA) 27**

**7. Visualising, editing, and realigning with AliView 27**

**7.1. Visualising the MSA 27**

**7.2. Editing the MSA with AliView 28**

**8. Orthologue prediction and alignment 29**

**8.1. SLiMSuite format fasta files 29**

**8.2. Using command line tools for orthologue prediction and alignment 30**

8.2.1. Using different alignment algorithms 31

**8.3. Converting Uniprot to SLiMSuite format (optional) 32**

**9. MSA using command line tools (Advanced) 33**

**9.1. Multiple sequence alignment on the BABS Teaching server 33**

9.1.1. Multiple sequence alignment tools on the BABS Teaching server 33

9.1.2. Reformatting Uniprot files to SLiMSuite format 33

9.1.3. Generating multiple sequence alignments 34

**10. Filtering sequences with command line tools (Advanced) 35**

**10.1. E-value filtering (BLAST/GABLAM) 35**

**10.2. Top Hit filtering (GOPHER) 37**

**10.3. GOPHER Results 38**

**10.4. Species filtering (SeqSuite) 39**

**10.5. Non-redundancy filtering (GABLAM) 40**

**10.6. Species-independent identity filtering 41**

**10.7. %identity filtering (GABLAM) 41**

**11. Basic nucleotide analysis with MEGA 42**

**11.1. Accessing MEGA 42**

**11.2. Opening a coding sequence alignment with MEGA 43**

**11.3. Exploring Sequence Data 44**

11.3.1. Sequence variation 45

11.3.2. Alignment quality 45

11.3.3. Fixing the alignment 46

11.3.4. Sequence variation revisited 47

11.3.5. Sequence composition 47

**12. Evolutionary models 48**

**12.1. Picking an appropriate model of evolution 48**

**12.2. Maximum likelihood model fitting 49**

12.2.1. Testing a range of substitution models using BIC 49

**13. Testing for deviations from neutrality 51**

**13.1. Testing the molecular clock using a relative-rates test 51**

13.1.1. Making a phylogenetic tree 51

13.1.2. Performing Tajima's Relative Rate Test 53

**13.2. Testing the molecular clock using the Maximum Likelihood method 53**

**13.3. Testing for selection using dN/dS 54**

**14. Basic phylogenetic analysis with MEGA 56**

**14.1. Getting data into MEGA 56**

**14.2. Making a phylogenetic tree with MEGA 57**

14.2.1. Constructing phylogenies 57

14.2.2. Testing for biased multiple sequence alignment data 58

**14.3. Visualising and manipulating phylogenies 58**

14.3.1. Comparing and contrasting trees 59

14.3.2. The impact of multiple sequence alignment on phylogenetics 59

14.3.3. Midpoint rooting and outgroup rooting 59

**15. Making a good phylogenetic tree figure with MEGA 61**

**15.1. General tips 61**

**15.2. Subtrees 62**

15.2.1. Formatting subtrees 62

15.2.2. Nesting subtrees 63

**15.3. Citing MEGA and its methods 63**

**16. Protein Family Analysis 64**

**16.1. HAQESAC – Generating alignments and trees of protein families 64**

**16.2. Visualising and improving the HAQESAC tree 64**

**16.3. Orthology and Protein Family Analysis 66**

**17. HAQESAC (Advanced) 67**

**17.1. Advanced filtering with HAQESAC 67**

**17.2. Running HAQESAC 68**

**17.3. HAQESAC alignments and trees 68**

17.3.1. HAQESAC output 68

17.3.2. HAQESAC Run Details 69

**17.4. Using MultiHAQ for protein family analysis using local BLAST databases 75**

17.4.1. Extracting our query sequence 75

17.4.2. Running multiple BLASTs with MultiHAQ 75

**17.5. Running HAQESAC interactively 76**

17.5.1. Subfamily grouping 77

17.5.2. Manual Group Review 79

17.5.3. Sequence variant removal 81

17.5.4. HAQESAC Cycles and final subgrouping 83

**17.6. Combining interactive and non-interactive HAQESAC runs 83**

**18. Snake Protein Annotation 85**

**18.1. Candidate Protein Selection 85**

**18.2. Setting up your workspace 85**

**18.3. Choosing a BUSCO genes to work on 86**

18.3.1. Picking a candidate 86

**18.4. Choosing a transcript ORF to annotate 87**

18.4.1. Example ORF sequence to annotate 88

**18.5. Choosing a GeMoMa prediction to search against 88**

**18.6. Updated protein search databases 88**

18.6.1. Snake species in snake\_proteomes.2020-07-16.fas 89

**18.7. Optional: using HAQESAC for a first pass annotation 90**

**19. Annotating a snake transcript (Advanced) 91**

**19.1. Using BLASTX to help choose a transcript 91**

**20. Sequence searches of snake genomes 92**

**20.1. Protein sequence searches 93**

**20.2. Transcript searches 94**

**20.3. Server outputs 95**

**20.4. Checking Hit Quality 96**

**20.5. Retrieving predicted protein sequences 97**

**21. Analysing genome and gene prediction quality 98**

**21.1. Opening results in the Apollo Genome browser 98**

**21.2. Importing annotation 100**

**22. BABS3291 Prac Assignment 102**

**22.1. Assignment submission 102**

22.1.1. Word limits and penalties 102

**22.2. Project write up 102**

22.2.1. Report structure 102

22.2.2. Writing methods 103

22.2.3. Appendix 104

**22.3. Assessment criteria 104**

22.3.1. Research question assessment 104

**23. Gene Annotation Workflow 105**

**23.1. Predicted snake protein sequence [\*compulsory] 105**

**23.2. Functional protein assignment/annotation [\*compulsory] 105**

23.2.1. Multiple Sequence Alignment 106

23.2.2. Phylogenetic tree 106

23.2.3. Domain composition 106

23.2.4. Gene duplications and protein families 106

**23.3. Evolutionary conservation analysis 106**

23.3.1. Snake proteins 106

23.3.2. Orthologue annotation 107

23.3.3. Inferred protein evolution 107

**23.4. Phylogenetic analysis 107**

23.4.1. Phylogenetic robustness 107

23.4.2. Alignment quality 107

23.4.3. Molecular clock analysis 108

**23.5. Protein family analysis 108**

**23.6. Genome integrity, quality and evidence 108**

23.6.1. Gene/genome integrity 108

23.6.2. Sequence/assembly accuracy 108

23.6.3. Supporting evidence 109

23.6.4. Gene structure 109

**23.7. Custom research question 109**

**24. Appendix 110**

**24.1. Tricks and Tips 110**

24.1.1. Using the UNIX server 110

24.1.2. LabArchives and lab books 112

24.1.3. Text file manipulation 112

24.1.4. Homology searching & sequence alignment 112

24.1.5. Using SLiMSuite 113

![](RackMultipart20230102-1-ssjimi_html_1894c1ad710f9d90.gif)

# 1.Prac Overview

## 1.1.Aims

The main aim of this prac is to turn you into a bioinformatician! What does this mean? You are  **not**  going to learn all of the tools and skills that a full-time bioinformatician has. This would (a) take years, and (b) is different for every bioinformatician. Furthermore, some of you will already have some of these skills, making it difficult and/or boring to teach them to everyone. Instead, you are going to be exposed to some general principles and learn some core skills, including:

- Working across multiple systems including command line programs.
- Correct file organisation and documentation.
- The importance of accuracy and attention to detail.
- Teaching yourself how to do things using trial-and-error.
- Harnessing laziness and boredom to achieve greatness.
- Worrying more about the "what" and "why" than the "how" to do things.
- What computers are (not) good at.

As you progress through the pracs, a couple of things will start happening: (1) the instructions will become less verbose and specific; (2) you will have increasing freedom over making decisions. This is deliberate. The goal of these pracs is to bring you to a point where you can direct and execute your own bioinformatics research, not simply follow instructions. This is more challenging – for both teachers and students – but hopefully you will find it more rewarding. Don't panic though! If your sole goal is to pass the course, you can get by with just following the instructions.

## 1.2.Research Aims

We will be analysing draft genome assemblies of the mainland tiger snake and eastern brown snake. The practical is designed conceptually in three sections:

**Part 1 - core bioinformatics & molecular evolution.**  In weeks 1-5 of the prac, you will be guided through a molecular analysis of some predicted genes and proteins from the tiger snake and eastern brown snake. These pracs will use real data to reinforce and test key learning from lectures. The emphasis is providing you with the theoretical and practical knowledge required for the final part of the prac.

**Part 2 - gene annotation.**  The final four weeks of the practical are designed to be a real (albeit very small!) research project. As such, you will be analysing data and asking questions that have not been looked at before. The main task is to use multiple sequence alignment, molecular phylogenetics and an online genome browser to annotate a predicted transcript or protein of your choice. You will be given some core analyses to perform and questions to answer, but also given the opportunity to expand your analysis further for additional credit. Candidate genes for study will be loosely categorised by difficulty. The simplest analysis will be sufficient for a pass or credit grade. More advanced analysis will be required for top marks. (See the Prac Report section, or ask if something is not clear.)

## 1.3.Prac Timeline

The prac is designed to be completed with flexible timing. The following is a guide to keep you on track:

PART 1

- Week 1. Prac Intro, server setup and core bioinformatics
- Week 2. Homology searching
- Week 2. Multiple sequence alignment
- Week 4. Molecular evolution with MEGA
- Week 5. Molecular phylogenetics with MEGA
- Week 6. Flexibility week.

PART 2

- Week 7. Ramaciotti Tour & Part 2 Intro
- Week 8. BABS Genome protein annotation.
- Week 9. Web Apollo gene finding and annotation.
- Week 10. Work on prac report & submission.

**NOTE: ** You will find that the speed of your progress depends on your level of skill and experience. The practical is set up to allow you to work on it outside of designated prac sessions, so...

1. Make sure you catch up if you cannot complete the week's activities during the lab. If you find yourself falling behind, seek help sooner rather than later. Hopefully, it should be possible for everyone to get through the core material each week, with a bunch of optional and/or open-ended tasks available for those with more time, experience and/or interest in the material. It is not always possible to get this balance right, so if you are really struggling, please let us know!
2. If you find yourself flying through the material, feel free to continue on to the next prac(s). The later pracs also have a number of optional advanced exercises, which will let you get deeper into the material and can help get a top grade for the assignment (advanced activities are not required to pass the course.)

## 1.4.Assessment

Part 1 of the prac will be assessed via Teams assignments and online quizzes, due for completion in Week 5. Together, these will form **20% of the course grade**.

Part 2 will be assessed by a second short report, due in Week 10. Marks will be awarded for presentation, adherence to formatting instructions, clarity and precision of methods, quality of figures, and scientific insight. Instructions and further details will be posted on Moodle. This report is worth **30% of the course grade**.

### 1.4.1.Submission

Online tasks will be submitted through  **Moodle**.  **Submission deadline:**  **Friday 18**** th **** March @ 1400****.**

The research report will be submitted through  **Moodle**  and must be in MS Word or PDF format.  **Submission deadline:**  **Friday 22**** nd **** April @ 1400****.**

## 1.5.Electronic Lab Books

We will be performing many steps of analysis on different data. Some of these steps will be purely exploratory and subsequently discarded. Some will be crucial for your final report. You will not always know which is which at the time! It is therefore imperative that you take clear, consistent notes of what you have done. Because you will be using a lot of computer commands, it is often helpful with bioinformatics to keep records in an electronic lab book rather than a physical notebook. Copying and pasting output from your terminal can be useful for finding errors later (or redirect output to a file, if you know how).

Some of the programs we will use will generate log files and/or have configuration files with settings that will permit repeat runs. Others - particularly anything that you do manually - will not have such records. It is especially important to record these "hidden" steps. Remember: the goal is to make any work repeatable, by you or someone else. It should be possible to trace every file back to its source using your notes.

There are several additional benefits of an electronic lab book over traditional paper lab books:

- all the entries are automatically time-stamped
- corrections can be made easily and changes are tracked
- pages can be of indefinite length and added to over multiple days, making it easier to organise lab notes effectively
- full text searching makes it easier to find things
- data and reference materials can be directly attached to lab book entries
- entries can be reviewed and edited at home without needing to take the lab book out of the lab

**NOTE:**  Unlike a Methods section in a report/paper, your lab book should also include failed attempts and notes explaining what went wrong, why and what was done about it. (Use some common sense here: there is no need to note every time a command failed because of a typo. However, should you later discover a typo that caused something to run incorrectly, this should be recorded.)

**The curse of autocorrect.**
 If you are using a "clever" office tool, such Word, OneNote or Evernote, it - or even your OS itself - will probably include an oh-so-helpful autocorrect function. This can be a real pain when trying to make notes about bioinformatics (or course documentation), as it will do helpful things like turn "zID" into "aid". Keep an eye your notes! Computers are dumb when it comes to typos, so an autocorrect-induced mistake in your recorded command will render it useless - or worse! A particular issue is the replacement of hyphens – which Word will often replace with a "dash" like it did just then. -n might be a valid program option but –n will not be! Spot the difference?

### 1.5.1.Lab Archives

Lab Archives is designed to be intuitive and easy to use. If you get stuck, you can access some help and video tutorials via the i button at the top right of the window. If these don't help, ask and we'll do our best. Generally speaking, you will probably want to stick to Rich Text entries and attaching files for your lab book but feel free to experiment with other entry types. (Adding PubMed References is a good way of keeping track of the original research papers that you want to cite in your report.)

For an overview of how LabArchives works, please see the student perspective videos:

- Brief version: [https://www.youtube.com/watch?v=YdDRhh3RqI8](https://www.youtube.com/watch?v=YdDRhh3RqI8)
- Extended version: [https://www.youtube.com/watch?v=YcHy-5PRknU](https://www.youtube.com/watch?v=YcHy-5PRknU)

**NOTE:** We are using LabArchives primarily as a Lab book, with MS Teams as the primary source of documentation and help. As a consequence, some of the LabArchives features highlighted in these videos may not be used.

**Lab book or Lab notebook?**
 You might have spotted that you have LabArchives "Notebook" whereas I keep referring to a "Lab Book". What's the difference? Not much. Your LabArchives Notebook is a general notebook where you can document and collect all manner of thoughts, activities and reference materials. A _Lab Book_ is specifically for recording what you have done in the lab. (Remember this is a "computer lab".) Hence your Notebook has a **Lab Book** folder for logging all your experimental activity. It is important that you keep accurate records of what you actually did, not simply what you intended to do, as this will help track down problems later. (Its mostly semantics.)

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

**Directories, folders and paths.**
 Don't get confused if you see "directories" and "folders" referred to in various places with respect to file locations. These are the same thing. A "path" is just the full address of that file/folder/directory. Type pwd ("path of working directory") to see the path for the directory you are currently in - this is the same as would appear in the "address bar" in Windows or the "path bar" in OSX. The "full path" includes the leading / that marks the root of the directory structure, and every single directory level, e.g. /home/$USER/BABS3291-Jun22/analysis/. A relative path does not have the leading / and will be interpreted relative to the current working directory. This is explained more in the Unix and Perl Primer.

### 2.3.2.Navigating the UNIX file system

Work through sections U2-U10 of the Unix and Perl Primer for Biologists to learn the basics of UNIX and navigating its file system. You can find the primer on the course Teams site and in the Reference Materials section of your LabArchives Notebook.

**Unix and Perl Primer data.**
 When you are working through sections from Unix and Perl Primer for Biologists, it will refer to data in /Volumes/USB/ as it assumes that you are working off a USB drive. We have created an equivalent directory on the server. However, you will _not_ have write permissions for this directory. If you want to work through other exercises in your own time, you will need to copy the data into your own directory. Ask if you need help with this.

### 2.3.3.UNIX file basics

You do not have permission to edit the contents of the /Volumes/USB/Unix\_and\_Perl\_course/ directory ("write access"), so you will need to make your own directory for learning how to manipulate files in a safe space. Return to your home directory and then create and enter Unix\_and\_Perl\_course/:

$ cd
 $ mkdir Unix\_and\_Perl\_course
 $ cd /home/$USER/Unix\_and\_Perl\_course/

Now work through sections U11-U25 of _Unix and Perl Primer for Biologists_. Remember to use to /home/$USER/Unix\_and\_Perl\_course/ in place of /Volumes/USB/Unix\_and\_Perl\_course/.

**NOTE:** Some of the text assumes you are in /Volumes/USB/Unix\_and\_Perl\_course/. You may want to **cd** to this directory for U19 and U20 before returning to ~/Unix\_and\_Perl\_course/ for U21-24.

**File permissions.**
 Files and directories have three types of access permission: read, write and execute (rwx). We won't worry much more about these now other than to say that if the instructions tell you to do something and you get a file permission error, please let Rich know. It probably just means that the permissions need to be changed to let you read that file or write to that directory.

### 2.3.4.Using temporary 'scratch' space

It is not uncommon to have limited /home/ space on a server. Most servers also have a 'scratch' directory that has a lot more space available but is _not_ backed up. Only you (and the system administrator) should have write access to the data you create in here. (Unless you change the file permissions.) However, others will probably be able to see the contents by default. Although /home/$USER/ and /scratch/$USER/ will have different contents, you should use a consistent naming and directory structure. These should be unified in your Lab Book structure and compiled in your backups off the server.

**Challenge:** Create yourself a /scratch/$USER/ directory and set up a BABS3291-Jun22/ directory within it with data/ and analysis/ directories as before.

**NOTE:** On the backup server, this space is /share/students/.

### 2.3.5.What to do when things go wrong

A major part of bioinformatics is finding and fixing errors that prevent things from working as planned. Solving problems yourself is one of the best ways to learn new things – and is very satisfying! If you try to run a command and it does not work, the general bug-fixing process is as follows:

1. Look at the error message. (If there is one!) This will often tell you if the command is invalid or a path is wrong.
2. Check all paths for programs, input and output files. Use ls [PATH] to verify that a file or program is where you think it is.
3. Check carefully for whitespace in the wrong place.
4. Check for missing or corrupted hyphens.
5. Check that all dependencies (e.g. loaded modules) are in place. (This is not always easy.)

If all else fails then type the command again carefully, using  **TAB**  to autocomplete file names etc. Finally, if that still doesn't work, seek help!

**NOTE:**  If a command is running but the program is unhappy and/or does not generate the desired output then there might be a problem with the format of an input file. Check the documentation, Google the error message and/or problem, and seek advice if you cannot solve it.

**Autocomplete: tab is your friend.**
 One of the most useful keyboard shortcuts on the terminal is the use of TAB to autocomplete file/directory names. Simply start typing a name and hit TAB and it will autocomplete until it reaches a point of ambiguity. For example, if you have example.txt and example.fas in the directory, ex + TAB will stop at example. – just type t or f and hit TAB again. Not only does this save time, it is a great way of checking that files are located and named the way you think.

### 2.3.6.Harnessing the UNIX history

When making records of what you have been doing, it is important to keep an accurate note of the commands used in addition to keep log files etc. This can be done by copying and pasting the commands directly from the terminal.

**Copying and pasting in Putty.**
 Copying and pasting in Putty is easy but can also be a bit frustrating. To copy text to the clipboard, simply highlight with your mouse. Highlighted text can now be pasted in the usual fashion. To paste text in Putty, simply  **right click**  the mouse.
**WARNING: ** Any text that you paste into Putty in this fashion at the command prompt will be interpreted and executed as a list of commands!

An alternative is to put your command history into a text file that you can then edit or copy and paste from in Windows. history will show the commands that you have typed along with a line number that can be used to easily repeat commands. Running history with a number will return only that number of commands, _e.g._

$ history 1

This will return just the last command, which was the history 1 command itself! (For me, this was command 133. You will almost certainly have a different line number.)

  133  history 1

This can then be repeated by using !N where N is the line number, e.g.

$ !133

  133  history 1

(Note that this does not add the repeated command to the history if it was the last command. Try history 2 and then the previous !N again to see what happens.)

You can instead direct your history into a text file, using the redirect character \>. Make and enter BABS3291-Jun22/docs/unix/ and then run:

$ history \> history.txt

$ less history.txt

The relevant commands can then be copied into your lab book.

**NOTE:**  You can also easily recall earlier commands by using the  **UP**  and  **DOWN**  arrow keys.

**Mastering commands with man pages. And Google.**
 Want to know more about a command and its options? The man ("manual") command can be used to access documentation about UNIX commands (including man itself):

 $ man man

Use up and down arrows to scroll through text, or "q" to quit. Other UNIX programs will normally have documentation that is accessed by running that program with --help or -h.

Manuals and help output for commands can be quite long. It is often easier to Google "UNIX" and the command in question. Or: "How do I … in UNIX?"

### 2.3.7.Using screen (Advanced)

When logging on from home, it is recommended to use  **screen**  to keep a session active if your internet connection (or the VPN) gets dropped for a moment. You can get a bit more information on  **screen**  here: [https://kb.iu.edu/d/acuy](https://kb.iu.edu/d/acuy). Or Google it!

In brief, start a screen with -S to give it a name:

$ screen -S screenname

This lets you easily have more than one screen running and remember which is which. (Otherwise, you have to use the number screen gives you.)

You can now pretty much do everything you would normally do. If you finish completely and want to kill the screen, type:

$ exit

On the other hand, to log out of katana but pick up where you left off,  **detach**  the screen with ctrl+a d. (i.e. ctrl+a together, followed by d.) You can then log out of the server (or attach a different screen and work on something else). When you want to resume, type:

$ screen -r screenname

You are now right back where you were, complete with history etc. Anything you left running when you detached will have continued running in your absence. If your connection was killed by losing WiFi etc. - or you left a terminal running somewhere else connected to the screen you want - you will need to detach and reattach the screen at the same time with **-dr** (else get a notification that the screen is "Attached"):

$ screen -dr screenname

**NOTE:**  screen uses ctrl+a to trigger functions, so ctrl+a will no longer jump to the start of the line: use ctrl+a a. To scroll through your terminal buffer, use ctrl+a ESC and then press ESC to exit the scrolling. See the link above for more functions.

### 2.3.8.Other UNIX tricks (Advanced)

Sections U26-U32 of the _Unix and Perl Primer for Biologists_ contain some additional tricks and tips for working in a UNIX environment. None of these are essential for this prac, but you might find them useful as you work through later command line exercises.

**NOTE:** If you want to set up your own .profile file in section U28, you _can_ put it in your home directory (/home/$USER/) and it should be there – and therefore applied – every time you log on.

## 2.4.Copying data on/off the server with Filezilla

The easiest way to copy data on/off the server is via FileZilla. FileZilla is a Windows or Mac OSX utility for copying files on/off the server in a user-friendly fashion. You connect in a similar fashion to putty (i.e. the same babsteaching.babs.unsw.edu.au server address, using your zID and zPass) but using a protocol called "SFTP" rather than "SSH". ("SSH File Transfer Protocol".)

Open FileZilla and select **File » Site Manager**. Click **N**** ew Site **and fill in the server name in the** H ****ost** box. The **Pro**** t ****ocol** should be SFTP and **L**** ogon Type **Normal. Enter your zID as the** U ****ser** and zPass as the **Pass**** w ****ord**. Lastly **R**** ename **the connection for future re-use. Hit** C ****onnect**. Trust the host and carry on.

![](RackMultipart20230102-1-ssjimi_html_60929b4ab63080da.png) ![](RackMultipart20230102-1-ssjimi_html_899ee6aeb77e2eca.png)

You should now have your computer on the left and the server on the right. Just drag files from one to the other to copy on/off the server. You can even use this to copy directly on/off an external drive.

![](RackMultipart20230102-1-ssjimi_html_3abf58b786f2f655.png)

# 3.File naming and organisation

There are many ways to organise files and projects. There is no single "best" way but there are good practices that should be followed and bad practices that should be avoided. In this practical, we will be using a system loosely based on the system that is used be the Edwards lab. This works on the principle of a hierarchical organisation scheme (explained below), which is mirrored by the organisation of your electronic lab book (i.e. one page per directory). This has pros and cons over some competing systems, such as using version control for everything. We can discuss these in the pracs if you like.

## 3.1.Project-level directories

It is best to keep all the files and data associated with a specific research project/question in a single directory. I generally find this best with a short informative prefix and a date. For this prac, we are using **BABS3291-Jun22** as the project directory.

## 3.2.Main directories

In this prac, you should use the following top-level directories, which were created on the server:

- **analysis/**. This is where your analysis directories will be created.
- **code/**. Use this directory for storing code, such as R scripts or small shell scripts. (You may not make any of these.)
- **data/**. Similar to analysis but for directories that primarily contain (or create) data to be analysed.
- **docs/**. Use this directory for various documentation, including notes for your lab books that are not associated with a specific directory, and feedback/answers from demonstrators _etc._
- **temp/**. A temporary directory that contains nothing important. Good for trying out UNIX commands, for example. Anything which is not small and quick should have a fully documented directory and lab book entry: otherwise, you might forget what it was doing and/or what you ran. (Especially if the system crashes or you lose connection.)

Update your **Lab Book in Lab Archives** to have a folder for each top-level directory.

To make a new Folder, click on  **+ New...**  and then click  **Add New Folder**. Use the LabArchives help if stuck - or seek help on Teams if really stuck!

**NOTE:** You may choose to have additional top-level directories for improved organisation as the prac progresses. For example, you may want a different directory for each candidate gene that you analyse in detail for Part 2 of the prac. Just make sure that you Lab Book and directory structures match each other.

## 3.3.Subdirectories

When performing a new step of the analysis, repeating a previous step, or creating a new dataset, it is a good idea to create a new directory. Although your code and docs directories may have a more flexible organisation, keeping a strict directory naming protocol for analysis, data and temp will make it much easier to document and keep track of runs. Here, we will use the convention used In my lab, where all analysis and data subdirectories have the same format:

**YYYY-MM-DD.ShortName/**

where  **YYYY-MM-DD**  is the date, and  **ShortName**  is a short but recognisable description of the content. (See the next section for some examples.)

The reason for including the date in the directory name is threefold:

1. It allows you to more easily find the right directory if you know when you performed the analysis or downloaded/created.
2. If you repeat the same analysis several times (due to errors or new data/settings), you can easily differentiate between these runs whilst keeping the same basic name.
3. By placing the date at the start of the name, your directories will automatically be sorted in date order when sorted by name (see ISO 8601 Dates).

**NOTE:** LabArchives will not sort folders and pages alphabetically, but it is recommended that you manually sort them to match.

**ISO 8601 Dates.**
 Despite adopting a common calendar, humanity has failed to use a common date format. Americans, for example, favour MM/DD/YY, whilst Aussies have DD/MM/YY (or YYYY). In addition to the confusion of month/day order, / is a path separator and so cannot be used in names. Although not widely used, humanity has actually agreed on a common date format: ISO 8601, YYYY-MM-DD. The beauty of this format is that alphabetical order and date order match perfectly, so sorting issues are a thing of the past. Use it!

## 3.4.File naming

Where possible, files should also be named in a consistent fashion. As we will see, this is a bit harder as different programs and labs tend to have their own ways of naming output files, or expecting input files to be named. Even in these cases, judicious use of the move ( **mv** ) or ( **cp** ) command can make later life easier.

The main thing is to try and avoid having files named something like  **reads.fastq**  or, even worse,  **reads**. At least  **reads.fastq**  indicates what kind of file this is – a fastq sequence file – but the  **reads**  part tells you very little. Presumably, it is some kind of sequencing read. But what species? Or technology? Which sequencing run, if you have more than one? The hope is generally that the parent directory of the file will be enough to provide context. This can work but it is better and clearer to have file names that are informative if they end up being viewed without that context. For example, you might accidentally move a file to the wrong place. (It happens to the best of us!) Worse, if your computer dies and you have to get the data recovered, it sometimes loses its parent directory information.

To this end, all files should be named along the lines of:

**base[.date][.info].ext**

where:

- **base**  is a prefix used to group all files belonging to a certain set of data. For example, you might have a bunch of files relating to the pax6 gene, which all start  **pax6** , and another set of files relating to pax8 that start  **pax8**.
- **date**  is the date in  **YYYY-MM-DD**  format. (Or possibly just YYYY or YYYY-MM.) For one-off analyses, the date is not really required but it is useful if you are likely to end up repeating an analysis over time.
- **info**  is some optional text that differentiates between different types of data of the same basic format, _e.g._ . **aln**  to indicate that it is an alignment, or a number if the data is spread over several files.
- **ext**  indicates the format of the file. You will already be familiar with this in Windows, for example, where  **.docx**  indicates a Word document. (Windows explorer often hides the extensions by default, but this can be changed in the options.) In bioinformatics, most files are actually plain text from the computer's perspective, but it would not be very helpful to have all files named  **\*.txt**. Instead, there are distinct formats of plain text, such as fasta, fastq, newick etc., which have common file extensions. Unfortunately, there are often multiple extensions for the same format, such as  **.fas** ,  **.fsa**  and  **.fasta**  for fasta format. For your own files, it is best to pick one and stick to it, unless you need to use a program that is fussy.

For example, if our reads file contained all the tiger snake pacbio subreads downloaded on 12th July 2017, we might call it:

**tigersnake.pbreads.2017-07-12.all.fastq**

Later, we might extract all the reads at least 10kb in length into a similarly-named file:

**tigersnake.pbreads.2017-07-12.10kb.fastq**

Even without the corresponding Lab Book documentation, I can make an educated guess about the contents of this file. (This provides additional protection against mistakes – it is _not_ a replacement for lab book documentation!)

Make sure that your file naming convention is documented, with consistent use of prefixes, extensions and info text. That way, you will not have to individually document/remember the content of every single file.

**NOTE:**  Do-as-I-say-not-do-as-I-do. For some of the examples and exercises in the lab manual, I might use file names that are fairly generic and non-descript (except for the extensions). This is to keep the commands simple and easier to read/copy. Imagine doing the same exercise with additional data from different individuals/species and think about what changes you might want to make to the file names!

**Why no whitespace?**
 Observant ones among you will have noticed that none of the directories or files we are using contain whitespace, i.e. **base[.date][.info].ext**, rather than  **base date info.ext**. UNIX can handle whitespace but it is a real pain, and not all programs will cope with it, so it's best avoided altogether. Use a period  **.** , hyphen  **-**  or underscore  **\_**  instead.

![](RackMultipart20230102-1-ssjimi_html_ba39574831b06ce.gif)

**NOTE: This prac uses a live sequence database, Uniprot. It is very likely that Uniprot will have additional sequences in it by the time you work through the prac. As a result, some of the details of your results may differ from those shown. Don't worry - this should not affect your ability to complete the activity. If you get stuck/confused, please post a question in the prac channel on Teams.**

# 4.BUSCO Gene Annotation

There are two main approaches to annotating protein-coding sequences from a genome:

1. Running gene annotation pipelines on the genome assembly and then annotating the predicted protein sequence.

2. Candidate gene searches, where a protein sequence from another source (even another species) is used to search the assembly for that specific gene and/or its relatives.

When you identify a putative candidate gene, you generally need to run it through the same annotation process as for protein sequences predicted by annotation pipelines. For this reason, we are going to start with annotating a predicted protein sequence.

We have not yet performed full annotation of the genome assembly, so instead we will be using the protein sequences identified as part of the BUSCO assessment process, which are found here:

/share/data/babsgenome/busco/run\_ts\_mother.Q25k81L500.busco/single\_copy\_busco\_sequences

For this example, we will analyse  **EOG090701X7**. (EOG = Eukaryotic Orthologous Group.) Feel free to explore some others.

**Why EOG090701X7?**
 As well as being single copy, this particular gene is encoded in a single exon, which will make some of the later stages easier. A list of single exon BUSCO genes will be posted in case you want to try another one. If you feel confident with some of the later stages, you might want to try with a multi-exon gene.

## 4.1.Fasta formats

This is a good time to introduce "fasta" format, which is a commonly used plain text format with the basic structure:

\>Name1 [Description]
SEQUENCE
[SEQUENCE…]
\>Name2 [Description]
SEQUENCE
[SEQUENCE…]
…

The core features are that each  **Name**  must be unique and that each  **SEQUENCE**  only contains IUPAC sequence letters and whitespace. The SEQUENCE can be on one line, or split over several. It can be upper, lower or mixed case. Sequences can be nucleotide or protein. A Description for each sequence is optional.

Often, the sequence name encodes additional information. This can be useful, but it can also cause issues when programs try to parse expected data from the wrong format, or sequence names with punctuation are used in filenames etc. The BUSCO genes provide a good example of this:

$ ls EOG090701X7.\*
EOG090701X7.faa  EOG090701X7.fna

$ more EOG090701X7.faa
\>EOG090701X7:ts\_mother.Q25k81L500.fasta:11599273:5156-9185
MEMNLTTIPSGIPNTTQTLDLSFNPLKTLHSNYFSAVFALRFLDLARCHLWKIEDNAFMGLNSLSVLILTGNPLQILGLRAFHGLPSLQRFVAVETNLFSLGTLPIGHLTSLQELNLSHNHIDSLKLPGYFSYLISLQHLNFQ
LNKISSISVGDLDALASPNLTLVLSRNDIKHIERKAFAGLHFQQLALRGCFEDKVIMQASIQNMSGLHVNSLLLGDYRDISKVESIDQSLLNVLCDLYLQELTVIEMDSLETGSTLSPCLNNISRVRVIHTYFGEDFMFPSNS
NISHLEFKNCGLDAVPAQNLPSLTKLRVLQITHTKYLRDFEKYFEGLQNLETLDLSVNRLDTHLSWVELLEGTPNLKHLNLSFNTKIRLEIECNGPGKLEYLDFQHTALASPGTVPSFFCLNHLIYLDISYTDTTVISQCSFC
GLHSLRVLKMAGNCFANNQLVDNFRNLTKLHFLDISNCQLKYISLSSLTSLHELRLLNVSHNKLLGLHPETYMNFPLLTTLDFHNNQLAALTEEDLKNLPASLKHVDLSANLFDCSCDHAHFLRWVKNSSALLRNVQNMVCYS
PSDLKNVQVMDFVLASCEISTTTVAVSVTVVLVLIVILILCYKYYFYLYYIMVLFLGNKFSEEKETVYDAFVIFSSKDQEWVKQELQQPLEEELPYFHLCLFYRDFIPGVSIITNIIKEGFQSSRKVIAVVSDHFLESRWCNF
ELEVAQSWQLVESKASLILVVLDGVDKAALHHKLGLFRYLRRNTFLTWKDRDLSRHVFLRQLRSALLEGKTWTEDELKLMLKNG

**Question:**  What's in the EOG090701X7.fna file?

**Question:**  What information do you think is encoded in the sequence name EOG090701X7:ts\_mother.Q25k81L500.fasta:11599273:5156-9185? Hint: the name given to ABySS scaffolds is a simple number.

## 4.2.Working with text files in UNIX

Work through Part 2 (U33-U37) of the _Unix and Perl Primer for Biologists_. This will give you a basic introduction into some useful UNIX commands:

grep | head

You should also try out **tail** , which is like **head** , but for the ends of files.

If you are having fun, work through sections U38-U45 too (and sections U26-U32 from Part 1 if you skipped **Section 2.3.8** )but these are not essential for the rest of the prac.

## 4.3.Exploring /share/data/ (Optional)

The data for the rest of the prac will be added to /share/data/. Some of it is there now and more will be added in time. If you are feeling brave, feel free to use your UNIX skills to explore what's there. Some of the commands you might want to use are:

ls -lrth, more, less, head, tail, grep, wc

**Unpublished data.**
Unless otherwise directed by the lab manual, please check with me before copying data en masse off the server - it is unpublished!

# 5.Homology Searching

## 5.1.Uniprot protein BLAST searches

Make an **analysis/YYYY-MM-DD.UniprotBLAST/**  directory and matching Lab Book page (using the actual date!) and copy the EOG090701X7.faa file into it on your Windows/Mac machine (e.g. with Filezilla).

Open the file in a text editor. I recommend  **Notepad++**  for Windows or  **BBEdit**  for a Mac. These both have good find and replace functions, decent handling of line ending encoding, and multitab capability, among other functions. You can now copy and paste it onto the clipboard easily.

**What the CRLF?**
 Windows, UNIX and Mac OSX all use different line ending encodings, in their infinite wisdom. There are two "hidden" characters: Carriage Return (CR) and Line Feed (LF). Windows uses CRLF. Linux only uses LF. Mac OSX used to only use CR, though I think modern Macs now use LF too. If you are getting odd behaviour when loading a file or running it with a Linux program, open it up in a good text editor and check the line endings!

Now visit the Uniprot BLAST site: [http://www.uniprot.org/blast/](http://www.uniprot.org/blast/). I am assuming that everyone knows about BLAST but you can watch an introductory video if you've not used this service before: [https://www.youtube.com/watch?v=UPaConHNP7E](https://www.youtube.com/watch?v=UPaConHNP7E).

Paste your protein sequence into the sequence window. It will accept FASTA format, or you can just paste the protein sequence without the name. (Make sure you get it all!) Make sure that the **Target database** is **UniProtKB** , the  **E-Threshold**  is set to  **0.0001 ** and ** Hits**  is set to  **250.**  Check the  **Run BLAST in a separate window**  box and then  **Run BLAST**. (Running in a separate window makes it easier to re-run with different settings later - or double-check that you had the right sequence if the results look odd.)

This will now open a new tab (or window) and the search will run. It shouldn't take too long and you can use the time to read on and see where this is going.

**NOTE: ** Jobs are stored for 7 days. If you are running this at home, you can always copy the link to your job and then come back and resume later.

**The importance of E.**
 For some reason, BLAST websites often have a default e-value threshold of 10. This means that you expect to see 10 hits _purely by chance_ given your search parameters! I think they do this because people get upset when they get no results but it can catch out the unwary. Generally speaking, real BLAST hits will have very low e-values, so set this to 0.0001 (1e-4). You only need to use bigger e-values when searching very short sequences or for very distant homology. When looking for close homologues of genes or proteins, you will often want an even more stringent e-value that this, which can be done using local BLAST searches (as we will see later).

### 5.1.1.Making sense of the results

The top panel gives a graphical overview of the hits:

- Entry = Uniprot accession number (unique identifier)
- Protein names = Text description, species in brackets
- Match hit = Graphical overview of sequence positions of BLAST hits relative to query
- Identity = Percentage identity of the hit region

![](RackMultipart20230102-1-ssjimi_html_fa84561ea6499dd0.png)

**Question:**  can you guess which gene EOG090701X7 is?! You won't always be so lucky!

As you can see the percentage identity decreases as you work through the list.

**NOTE:**  It's actually sorted by BLAST score, not identity. Often, identity and score will correlate but longer, lower identity matches can have higher scores than short, high identity matches.

### 5.1.2.Getting more details

The lower panel gives more details and is the more useful table to look at:

![](RackMultipart20230102-1-ssjimi_html_5c979c8f292b980c.png)

Mouse over the species and you should get more information, including (usually) the common name as well as the latin name. In the example above, the first hit is _ **Ophiophagus hannah** _** (King cobra) (**_ **Naja hannah** _**)**. A snake - this is reassuring! (You might find something even closer if they update Uniprot!)

**Trust No One**
 The golden rule in bioinformatics (and science generally) is that trust needs to be _earnt_, it should not be given blindly. It may seem like a trivial result that our top hit comes from another snake but this is actually an important finding as it gives us confidence that we really are looking at the tiger snake genome. Whilst hopefully unlikely, sample mixups etc. can occur and so having some "positive control" sanity checks is always a good idea.

The columns of this table can be customised. See if you can add  **Length**  to the table. (You might need to reload the page to get it to appear.) This is always useful as it can help identify splice variants, incomplete sequences and/or hits to different proteins that share a short region of homology (e.g. a protein domain).

You can also dig deeper into the individual hits. Visualising data like this is always a good idea, at least for a few results, as it is the best way to spot odd things that might indicate a mistake has been made. Click on "View alignment" for the King cobra hit:

![](RackMultipart20230102-1-ssjimi_html_9a58dedb44d5e3dc.png)

This gives a few more details on the sequence match. Below this are the aligned regions themselves. The  **+**  characters in the central "match" sequence in the alignment are amino acid pairs with positive BLOSUM matrix scores - these are substitutions with a high probability that positively contribute to alignment scores. The " **Positives**" statistic is the sum of these plus the exact matches (" **Ident.**" or  **Identities** ).

**Local or Global?**
 This match has 92.7% identity. But 92.7% of what? The query sequence? The hit sequence? (These are different lengths.) Or the matching region? I don't think this is explicitly stated anywhere but this is the  **local percentage identity,**  meaning that it refers only to the hit region. (The  **L**  in  **BLAST**  stands for local.) A  **global**  alignment or statistic deals with the full-length of the sequence. Note that these percentage identities can be very misleading as a result. What would you rather have, a 90% match to 10% of the sequence or an 80% match to 100% of the sequence?

**NOTE:**  If you are unsure, you can work it out from the raw numbers. In this case, we have 26 "+" characters (use find in your browser for a quick count), so the difference between Ident and Positives is from 26 positions. 96.2%-92.7% = 3.5%. The query protein length is 799 aa and the match length is 741 aa. 26/799 = 3.25% whereas 26/741 = 3.51%.

![](RackMultipart20230102-1-ssjimi_html_e9827976037fba0f.png)

In this case, we have a single aligned chunk. Sometimes, you will have multiple aligned chunks. These will appear in order of score (best to worst), NOT position, so you might have to do some mental rearranging. It is generally easier to just download and align the sequences, which we will do next.

## 5.2.Downloading proteins

The hits that you will get will vary from protein to protein. As you scroll further down the list, you will see that there are many hits to some species that all say  **Toll-like receptor 4** , e.g. chicken (Gallus gallus). These might represent splice isoforms, paralogues (different members of a gene family), or multiple redundant entries that have been entered into Uniprot. Eventually, redundant entries should get curated into a single  **Reviewed**  entry but most of the protein sequences in the database are derived from translated nucleotide sequences ( **TrEMBL = "Translated EMBL"** ) that have not undergone any manual checks or curation.

Because of this, it is generally not a good idea to simply select the top X hits and align them without having a little look at the species distribution. Instead, you will get a much more informative alignment and tree if you can select sequences from a range of organisms.

Select some sequences from this table by clicking the check boxes in the table. Make sure that you include the  **Green sea-turtle**  sequence (M7CBL4) - I'll refer to it later. For annotation purposes, we are selecting some sequences to make an alignment and a tree. We don't want too many or too few sequences for this. Too few and we won't have enough information. Too many and things will take a long time and be difficult to look at.

**CHALLENGE:**  10-20 sequences is good for a first look. In this instance, try to select 3-5 each of reptiles, birds, mammals and fish. (Read on if you get stuck!)

What's the problem with this? There are no fish in the top 250 BLAST hits! We'll come back to this in a minute.

**NOTE:** If you _did_ find fish, you might have searched "UniProtKB reference proteomes plus Swiss-Prot" as the **Target database** by mistake!

### 5.2.1.Why download sequences?

You might have noticed the option to directly align the sequences that you have selected. This is convenient but there are a few problems with this approach:

1. You have to get it right first time.

2. It can be a pain to get the raw unaligned sequences, which are useful if you want to try a different alignment program later.

3. Whilst this will align the selected hits, it will not include your original sequence. This is not helpful when trying to annotate that sequence!

An alternative is to  **Download**  the sequences. This gets around problem (2) and (3) but you still have problem (1). Instead, it is better to  **Add to basket**. This can be done in chunks, allowing you to focus on one task (e.g. getting some birds) before moving on. You can also err on the side of adding too many sequences as you can also delete some of them again later.

### 5.2.2.Adding fish

The basket can also be used to get around the problem identified above regarding the lack of fish. Once you have added your other sequences of choice to the basket, click back into your original  **BLAST**  window, which should still be open (as you ran in a new window). Increase the number of  **Hits**  to 1000 and set running again. Once the new run has finished, click on the drop-down taxonomy selection below  **Popular Organisms**  in the  **Filter By**  menu on the left-hand side:

![](RackMultipart20230102-1-ssjimi_html_c3c8565d7eb823d6.png) ![Shape1](RackMultipart20230102-1-ssjimi_html_49ac0cb03196381.gif)

(You should now have 11 zebrafish sequences in there, which are not there if you look in your original BLAST.)

Click on  **Teleostei**  and select a few fish sequences then  **Add to basket**  again. You can now see that your  **Basket**  has updated with your original sequences plus the new ones.

### 5.2.3.Download and save

The next step is to download your sequences to a fasta file. This avoids the need to re-run the BLAST later should the next steps take longer than anticipated.  **Make sure you document your search and the reasons for your selection in your lab book.****  **

Save the sequences as an  **uncompressed fasta file**. Give it a sensible name, not the default on given, e.g.

tlr4\_hits.select20.YYYY-MM-DD.fasta

(See the  **File naming**  section if you have forgotten how to name files.) It is also a good idea to  **Download**  as a tab delimited text or Excel file with the same file prefix. This not only makes your documentation easier by removing the need to manually document your selection, it will make the generation of a table of sequences easier later. There is no harm also pasting the contents of this table file into your LabArchives entry for easy reference and additional annotation as you make observations in future.

Before leaving the BLASTP results, switch back to  **Show all results**  to clear the teleost filter and then download the full set to a fasta file: **Download » Download all (1000)**.  **You might use this for one of the optional activities later, so make sure you have documented its file name in your lab book.**

**Compressed or uncompressed?**
If you know how to unzip files, feel free to download the compressed version of these files. For small fasta files like this, it won't make much difference. If downloading full Uniprot flat files for many sequences, compression with save disk space and ease bandwidth.

### 5.2.4.Emergency files

If you experience problems with the searches and/or downloads (such as the search taking too long), you can access pre-generated versions of these files for the next step of the prac from MS Teams or LabArchives:

|
- **tlr4\_hits.select20.fasta (18.5 KB):** Selected 20 hits from a Uniprot BLAST search using a tiger snake TLR4 BUSCO prediction for the query.
- **tlr4\_hits.full1000.fasta (852 KB):** Top 1000 hits from a Uniprot BLAST search using a tiger snake TLR4 BUSCO prediction for the query.
 |
| --- |

![](RackMultipart20230102-1-ssjimi_html_dc0d717d5d82a8c4.gif)

# 6.Multiple Sequence Alignment

Pairwise local alignments from BLAST searches are useful but can only tell us so much. It is more informative to look at a full-length (global) alignment of our predicted protein against a representative set of homologues.

**NOTE: ** For this exercise, we will be using the two fasta files that you saved as part of **Prac 2** , so make sure you have done this before proceeding!

- File 1: BUSCO protein prediction,_ e.g._ EOG090701X7.faa
- File 2: Twenty selected BLAST hits from Uniprot,_ e.g. _tlr4\_hits.select20.fasta

## 6.1.Making a Multiple Sequence Alignment (MSA)

The simplest thing to do is to align the sequences at the Uniprot site, which uses one of the best multiple sequence alignment programs, Clustal Omega: [http://www.uniprot.org/align/](http://www.uniprot.org/align/). Copy and paste the original BUSCO prediction (EOG090701X7.faa) into the alignment window. Open your downloaded sequences up in a text editor (tlr4\_hits.select20.fasta, or whatever you named this file). I recommend  **Notepad++**  for Windows or  **BBEdit**  for a Mac. Copy and paste these sequences into the alignment window after the BUSCO sequence and click  **Align**.

When it has run,  **Download**  the alignment as an  **uncompressed fasta ** file, which can then be used in other programs.  **NOTE:**  If it just opens in your browser, copy and paste it into your text editor and save it from there.

**NOTE:**  Now is a good time to review and note your file naming strategy and then use it consistently. (See  **File Organisation**  section from **Prac 1**.)

# 7.Visualising, editing, and realigning with AliView

## 7.1.Visualising the MSA

Open up the alignment in the program  **AliView**  for a look. (You can download this here: [http://ormbunkar.se/aliview/downloads/](http://ormbunkar.se/aliview/downloads/), or access it via [UNSW MyAccess](https://www.myaccess.unsw.edu.au/applications/aliview)).

You'll probably notice a couple of things straight away:

1. The sequence names are not particularly helpful, being just the uniprot accession numbers. This is where the table you downloaded can be helpful! We will see later how to use a command line tool on the server to help solve this problem.

2. One or more of the sequences has a long N-terminal relative to your sequence. (The  **Green sea-turtle**  sequence (M7CBL4), if nothing else.) Other might have some additional chunks later in the sequence and/or be missing regions of your query. One of the challenges (we won't worry about here) is trying to work out whether your sequence is complete and whether these differences reflect splice isoforms or poor annotation in the other species. This is not always easy! The only definitive way is with proteomics data, which we generally don't have - and can't afford right now for our snakes!

Experiment with the different visualisation shading options, using the buttons in the top left of the window:

![](RackMultipart20230102-1-ssjimi_html_9b4c1461d47a0992.png)

The default (and with no buttons pressed) is to colour the amino acids according to their type. (There are different colour schemes in  **View » Colors**.) The first three options will be of most use:

1. Highlight differences relative to a "trace" sequence. This will enable you to select your snake sequence as the "target" and highlight sequences that differ from it - quite powerful for determining where your specific sequence is similar or different to its homologues. If you arrange the sequences appropriately, it can also be used to spot snake-specific conservation etc.

2. Highlight differences from majority rule consensus. This is generally useful for identifying sequences that are very diverged and/or have aligned badly.

3. Highlight majority rule consensus characters. This is the recommended view to use at first, as it gives a good visual overview of the general quality of your alignment and whether there are regions of the protein that are particularly well or poorly aligned/conserved.  **This is the view you will use for the submitted Task**.

Try each view and save it to a PNG image using  **File » Export alignment as image**. Make sure you use an appropriate filename. Add these images to your lab book entry for this activity as Attachments.

**Challenge**
 Create a blank PowerPoint presentation and import your three alignment images, stacking them on top of each other so that you can see all three visualisations at once. Think about what sorts of patterns might indicate regions of your snake protein that warrant further attention, either as possible errors or possible interesting biology. Experiment with the drawing tools in PowerPoint to annotate your images, e.g. drawing boxes around well-conserved regions or pointing out interesting regions with arrows. You can then export your annotated figure as an image or PDF and attach that to your lab book page too. (You might want to try this after removing some sequences, regions, as described below.)

## 7.2.Editing the MSA with AliView

You can also use AliView to edit the alignment. Sequence can be edited or whole sequences can be deleted. You can also use AliView to perform the alignment itself. Select  **Edit » Delete all gaps in all sequences**  and then  **Align » Realign everything**. This will use MUSCLE by default, which is another recommended alignment program. You can change this to MAAFT (a third recommended program) using  **Align » Change default aligner program**.

Re-align with MUSCLE and  **Save as fasta**  with a new filename then reopen your Clustal Omega alignment and compare the two. Are they the same? Which do you think is better? (Note that the sequence order might now be different, so you may need to rearrange the sequences to make a good comparison.)

**Question: ** Are there any sequences that seem to be causing issues? Try deleting them and realigning with MUSCLE. Does this make things better? You can keep deleting and realigning until you are happy with the alignment. Just remember not to save over your original alignment file and then you can always go back if you make a mistake!

**Which aligner should I use?**
 There is no such thing as the best multiple sequence alignment program. The three mentioned above - Clustal Omega, MUSCLE and MAAFT - are all good and will have similar performance overall. One might do better with one set of sequences and a different program might do better with another. When the alignment is important to you, you should always look at it. Where it really matters, you might want to try two or three different programs and see which looks better - or perform downstream analyses with both if you can't decide, and see how much difference the alignment makes to your final results, e.g. the phylogenetic tree produced.

**NOTE: ** For your final gene annotation, you can choose which alignment algorithm you use and how you access it. We will use the command line next but feel free to use AliView, Uniprot, or anything else you feel more comfortable with. The important thing is that you clearly document what you have done.

# 8.Orthologue prediction and alignment

Up to this point, we have been looking for/at **homologues** : sequences that share common evolutionary ancestry with our protein of interest. For many evolutionary analyses – including annotating new protein sequences – we are usually most interested in **orthologues** : sequences representing the "same" gene/protein in another species, not simply a gene/protein from the same gene family. In this section, we will use a tool for predicting and aligning a set of protein orthologues, saving us a lot of time and manual processing.

## 8.1.SLiMSuite format fasta files

We've already come across fasta files and some of the inconsistencies of sequence name formats from different sources, e.g.:

\>tr|M7CBL4|M7CBL4\_CHEMY Toll-like receptor 4 OS=Chelonia mydas GN=TLR4 PE=3 SV=1

\>EOG090701X7:ts\_mother.Q25k81L500.fasta:11599273:5156-9185?

In each case, a program that "knows" the format can potentially extract extra information. The Uniprot sequence name identifies the database (tr for TrEMBL, as opposed to sp for Swissprot), the accession number (M7CBL4) and the Uniprot ID (M7CBL4\_CHEMY), which includes the species code (CHEMY, short for Chelonia mydas). The BUSCO name contains information about which EOG it's from, which file was searched, and which scaffold and position was hit.

As you have seen with your AliView alignments, however, this does not translate into something that is useful in all programs. In addition, the problem with complex formats containing special characters that mean things on the command line (|, :, / etc.) is that they can make it hard for programs to consistently process fasta files. It can also cause issues when one format that looks a bit like another gets read as the wrong type and extracts the wrong part for the unique identifier, for example.

To get around this, we will be largely sticking to the naming convention used by SLiMSuite and its sequence utility SeqSuite. This is partly because we will be using some programs for this package but also because it is a clean format with several advantages. The key features of [SLiMSuite fasta format](http://slimsuite.blogspot.com.au/2015/10/file-format-fasta-seqfile-fasfile.html) sequence files are:

1. Sequence names take the form: **\>gene\_SPECIES\_\_AccNum [Description]**, where  **gene**  is a simple text identifier to help human recognition,  **SPECIES**  is a Uniprot species code,  **AccNum**  is a  **unique**  identifier for that sequence and  **Description**  is optional. This gives a sequence name that is (a) unique, (b) human-readable, (c) easily parsed to extract species code and accession number, and (d) simple text thus able to be used directly in filenames and unlikely to break _any_ bioinformatics programs. (I've not found any yet, at least!) Note the **double underscore** between **SPECIES**  and  **AccNum**.
2. Sequences are stored as a single string, all on one line. This enables the useful UNIX tool  **grep**  (globally search for a regular expression and print matching lines) to be used to directly extract sequences based on their names ( **grep -A 1** ) or sequence patterns ( **grep -B 1** ). We will come across **grep** later in the prac, but feel free to look it up now or pause to work through the **Advanced UNIX** section of the _UNIX and Perl Primer_ – it's a _very_ useful UNIX tool.

In this activity, we will be using a program from the SLiMSuite package that predicts orthologues. To do this, it needs to identify the species of the protein sequence. To do _this_, it needs to have the sequence names in SLiMSuite format. We will see how to reformat Uniprot sequences later. For now, we will just rename our BUSCO sequence manually. One option is to edit it in a text editor and shuttle it back and forth with FileZilla. Here, we will use cat to copy and paste it into a file on the command line. **NOTE: ** If you struggle with using cat, skip this part and use a text editor on your desktop/laptop and copy it over.

This approach uses three common UNIX functions and is a good shortcut to creating a text file quickly on a UNIX system. First, we will use **cat** - short for "concantenate". This will either concatenate file contents or, if no files are given, standard input a.k.a. **stdin** (what you type) and copy the contents to standard output a.k.a. **stdout** (i.e. the screen). For example:

$ cat /share/data/babsgenome/busco/run\_ts\_mother.Q25k81L500.busco/single\_copy\_busco\_seque
 nces/EOG090701X7.faa

\>EOG090701X7:ts\_mother.Q25k81L500.fasta:11599273:5156-9185
MEMNLTTIPSGIPNTTQTLDLSFNPLKTLHSNYFSAVFALRFLDLARCHLWKIEDNAFMGLNSLSVLILTGNPLQILGLRAFHGLPSLQRFVAVETNLFSLGTLPIGHLTSLQELNLSHNHIDSLKLPGYFSYLISLQHLNFQLNKISSISVGDLDALASPNLTLVLSRNDIKHIERKAFAGLHFQQLALRGCFEDKVIMQASIQNMSGLHVNSLLLGDYRDISKVESIDQSLLNVLCDLYLQELTVIEMDSLETGSTLSPCLNNISRVRVIHTYFGEDFMFPSNSNISHLEFKNCGLDAVPAQNLPSLTKLRVLQITHTKYLRDFEKYFEGLQNLETLDLSVNRLDTHLSWVELLEGTPNLKHLNLSFNTKIRLEIECNGPGKLEYLDFQHTALASPGTVPSFFCLNHLIYLDISYTDTTVISQCSFCGLHSLRVLKMAGNCFANNQLVDNFRNLTKLHFLDISNCQLKYISLSSLTSLHELRLLNVSHNKLLGLHPETYMNFPLLTTLDFHNNQLAALTEEDLKNLPASLKHVDLSANLFDCSCDHAHFLRWVKNSSALLRNVQNMVCYSPSDLKNVQVMDFVLASCEISTTTVAVSVTVVLVLIVILILCYKYYFYLYYIMVLFLGNKFSEEKETVYDAFVIFSSKDQEWVKQELQQPLEEELPYFHLCLFYRDFIPGVSIITNIIKEGFQSSRKVIAVVSDHFLESRWCNFELEVAQSWQLVESKASLILVVLDGVDKAALHHKLGLFRYLRRNTFLTWKDRDLSRHVFLRQLRSALLEGKTWTEDELKLMLKNG

The second element is the ability of UNIX to redirect stdout into a file using the " **\>**" symbol (or **\>\>** to append rather than replace a file). When we put these together, we can redirect cat into an empty file and then type/paste in its contents:

$ cat \> NSCUK81EOG090701X7.fas

This should now be waiting for **stdin**. (If it says "Permission denied" then check you are where you think you are on the server – see **Section 2.3.5**.) Copy the sequence above, changing the name to SLiMSuite format, and then paste the sequence that you want to be in the file:

\>eog\_NOTSC\_\_NSCUK81EOG090701X7 EOG090701X7:ts\_mother.Q25k81L500.fasta:11599273:5156-9185
MEMNLTTIPSGIPNTTQTLDLSFNPLKTLHSNYFSAVFALRFLDLARCHLWKIEDNAFMGLNSLSVLILTGNPLQILGLRAFHGLPSLQRFVAVETNLFSLGTLPIGHLTSLQELNLSHNHIDSLKLPGYFSYLISLQHLNFQLNKISSISVGDLDALASPNLTLVLSRNDIKHIERKAFAGLHFQQLALRGCFEDKVIMQASIQNMSGLHVNSLLLGDYRDISKVESIDQSLLNVLCDLYLQELTVIEMDSLETGSTLSPCLNNISRVRVIHTYFGEDFMFPSNSNISHLEFKNCGLDAVPAQNLPSLTKLRVLQITHTKYLRDFEKYFEGLQNLETLDLSVNRLDTHLSWVELLEGTPNLKHLNLSFNTKIRLEIECNGPGKLEYLDFQHTALASPGTVPSFFCLNHLIYLDISYTDTTVISQCSFCGLHSLRVLKMAGNCFANNQLVDNFRNLTKLHFLDISNCQLKYISLSSLTSLHELRLLNVSHNKLLGLHPETYMNFPLLTTLDFHNNQLAALTEEDLKNLPASLKHVDLSANLFDCSCDHAHFLRWVKNSSALLRNVQNMVCYSPSDLKNVQVMDFVLASCEISTTTVAVSVTVVLVLIVILILCYKYYFYLYYIMVLFLGNKFSEEKETVYDAFVIFSSKDQEWVKQELQQPLEEELPYFHLCLFYRDFIPGVSIITNIIKEGFQSSRKVIAVVSDHFLESRWCNFELEVAQSWQLVESKASLILVVLDGVDKAALHHKLGLFRYLRRNTFLTWKDRDLSRHVFLRQLRSALLEGKTWTEDELKLMLKNG

Hit **\<ENTER\>** to go onto a new line if your pasted text did not include this. Now, we just need to close the file. To do this, we use the universal UNIX kill command **CTRL+C** (pressed together). This will kill  **cat**  and close the file.

Use **cat** , **less** or **more**  to look at the contents of the file - it should contain the above sequence that you pasted in.

**NOTE:**  If your file is empty, this will cause issues later! Make sure that you pasted in the sequence before closing the file. Make sure you also hit \<ENTER\> after the end of the sequence. (If you didn't, the command prompt will appear right next to the sequence when you look at it:

…LRSALLEGKTWTEDELKLMLKNG[zID@babsteaching01 directory]$

**QUESTION:**  What is the NOTSC is the new sequence name? (Hint: [http://www.uniprot.org/taxonomy/](http://www.uniprot.org/taxonomy/))

**QUESTION:**  Why do you think I added something to EOG090701X7 to use as the unique identifier?

**CHALLENGE:**  Can you rename the sequence from the original file using  **sed**. Don't try this unless you are feeling confident with UNIX tools.

## 8.2.Using command line tools for orthologue prediction and alignment

We are now going to see how using a command line tool can be much more convenient that online tools as it can automate a lot of the steps for you. In this case, we will use [GOPHER](http://rest.slimsuite.unsw.edu.au/gopher) (Generation of Orthologous Proteins from Homology-based Estimation of Relationships), which is a program I made some years ago for making automated alignments of homologous proteins that are predicted orthologues. (Orthology will be covered in Lecture Topic 3 if you are unfamiliar with the concept.)

GOPHER first performs a BLAST search of each query against a database of potential orthologues - ideally whole proteomes for organisms of interest. Next, it filters hits to the best hit from each species. Then is assigns homology on the basis of an adaptation of the "mutual best hit" approach that accounts for many-to-many orthology relationships. In essence, GOPHER checks that each hit does not have a closer hit in the query species that is not itself more closely related to the query protein. (You can look at the GOPHER manual if you want more details.) Finally, GOPHER calls multiple sequence alignment and phylogenetic inference software.

We will run GOPHER on the same BUSCO protein as used for the Uniprot search. First, the relevant modules need to be loaded on the server. Then the GOPHER command line call needs to be made, with a number of parameter settings to define the search:

$ module add blast+ clustalw clustalo R/3.4.0
$ python /share/apps/slimsuite/tools/gopher.py -seqin NSCUK81EOG090701X7.fas
 -orthdb /share/data/babsgenome/gopherdb/orthdb.2017-09.fas -bootstraps 1000
 -treeformats nwk,text,png

where:

- -seqin NSCUK81EOG090701X7.fas sets the input query proteins. In this case, we have only one, but GOPHER will work through all proteins in the input.
- -orthdb /share/data/babsgenome/gopherdb/orthdb.2017-09.fas defines the protein database that GOPHER uses for the BLAST search. We are using a combined filed of "Quest for Orthologues" proteomes, (four) published snake proteomes, and the BUSCO protein predictions from the initial 10X Genomics assembly of each snake.
- -bootstraps 1000 sets the number of bootstraps for the phylogenetic tree.
- -treeformats nwk,text,png sets the output options for the phylogenetic tree.

This should generate a nested directory structure named after the orthologue database and then the query species. Within this will be subdirectories containing the outputs for each query protein:

./orthdb.2017-09/NOTSC:
BLAST  clustaloALN  clustaloTREE ORTH  PARA

For details, see the GOPHER documentation. We will worry about the tree output in the next prac. For now, we are interested in the clustaloALN directory, which contains our MSA:

orthdb.2017-09/NOTSC/clustaloALN/NSCUK81EOG090701X7.orthaln.fas

Copy this file across to your computer and view it in AliView.

**QUESTION:** Does this alignment look better or worse than the alignment you did last week?

**What species is that?**
 As explained above, the five letter uppercase code in the sequence names is the Uniprot species code. Some of them are obvious (e.g. HUMAN for human), while many are the concatenation of the start of the genus and species (e.g. _Canis familiaris_ becomes CANFA). In time, you will get to recognise some (e.g. NOTSC for the tiger snake). Any that you are not sure about can be looked up at [https://www.uniprot.org/taxonomy/](https://www.uniprot.org/taxonomy/).

### 8.2.1.Using different alignment algorithms

The teaching server also has MUSCLE and MAFFT installed. These can be added with the relevant module add command, e.g.

$ module add muscle

To run GOPHER with a different alignment tool, use the -alnprog parameter:

$ python /share/apps/slimsuite/tools/gopher.py -seqin NSCUK81EOG090701X7.fas
 -orthdb /share/data/babsgenome/gopherdb/orthdb.2017-09.fas -alnprog muscle

This will output alignments and trees to the muscleALN and muscleTREE subdirectories of the GOPHER output.

**Challenge**
 See if you can run GOPHER with MAFFT.

## 8.3.Converting Uniprot to SLiMSuite format (optional)

Happily, SeqSuite itself can be used to reformat many different sequence files into the right format, including downloads from Uniprot. This can be useful even if you are not using GOPHER for orthologue prediction.

Create a new  **analysis/**  folder for making alignments on the server and copy your fasta file for alignment downloaded from uniprot. Then run the  **seq**  tool of SeqSuite with the  **gnspacc=T**  option as follows:

$ python /share/apps/slimsuite/tools/seqsuite.py seq -seqin \<INFILE\> -gnspacc T -seqout tlr4.uniprot.2017-08-28.fas

You will need to replace \<INFILE\> with your filename. Feel free to use something other than tlr4.uniprot.2017-08-28.fas for your new file (change the date at least!) and _make sure you document it in your lab book_. Now look at it with  **more** :

$ more tlr4.uniprot.2017-08-28.fas

\>tr\_OPHHA\_\_V8PDU2 Toll-like receptor 4 (Fragment) OS=Ophiophagus hannah GN=TLR4 PE=3 SV=1
MGLNSLSVLILTGNPLQILGLRAFHGLPSLERFVAVETNLFSLATLPIGHLTSLQELNLSHNHISSLKLPGYFSYLIFLQHLSFQLNKISSVSVGDLDALASRNLTLVLSRNDIKHVERNAFAGLHLQQLVLRGCFEDSVIMQ
ASIQNMSGLHVNSLLLGEYRDISEVESIDQSLLNVLCDLHLQELTVIEMDSLETGSTLSPCLNNISRVRVVHTYVREDCMFPSNSNISHLEFKDCRLDMVPAQNLSSLTKLRELHITHTKHLRYFDKYFEGLQNLETLDLSIN
SLVTHLSWVKLLEGAPNLKYLNLSFNTQITLNIECNGPGKLEYLDFQHTALASPGTVPSFFCLNHLIYLDISYTDTTVISQCSFCGLHSLRVLKMAGNCFANNQLVDNFRNLTKLHFLDISNCQLKYISLSSLTSLHELRLLN
VSHNKLLGLHPETYVHLPLLTTLDFHNNQLAALTEEDLKNLPASLKHLDLSENLFDCSCNHTHFLRWVKNSSALLRNVQNMLCYSPSDLKNVQVMDFVLVSCEINTTTVAVSVTVILVLIVILILCYKYYFYLYYIMVLFIGN
RFSEEKETVYDAFVIFSSKDQEWVKQELQQPLEEELPYFHLCLFYRDFIPGVSIITNIIKEGFQTSRKVIAVVSDHFLESHWCNFELEVAQSWQLVESKASLILVVLDGVDKAALHRKLGLFRYLRRNTFLTWKDRDLSRHVF
LRQLKSALLEGKTWTEDELKLMLKNG
\>tr\_ANOCA\_\_H9GKF0 Toll-like receptor 4 OS=Anolis carolinensis GN=TLR4 PE=3 SV=2
MPGGGVLYPQMFFPLLVLFWSQWRTRGLIPCVEVIPGSIYRCMELNLSGIPPGIPNTTENLDLSFNLLKNLTFNYFSLVPALRFLDLTRCGIQRIEDNAFMGLYNLSVLILTANPIQFLGPRAFHDLMSLQKLIAVETNISRL
DSLPIGHLTALQELNLSNNHINSLRLPEYFSQLIALRFMSFQSNKISAISAGDLDGFQSRNLTLVLSKNIIKYIELNSFSGVYFQELSLRGCFETSAHMQTSLQNLSGLHANRLVLGAYRNADRLEDFSKDHLDGLCHMCLQE
IALVQISSLYRTDSLSDCLNNIHSVRLVNTDIEQVSPFPENSSIHHLEINNCRLRGVPAESLSSLKELRVLRITKSGRFLTRFAEDFNGPPNLEILDLSENSLVVSFAWSSLMEGLPNLKHLNLSFNSKITFPPECSGVSKLE
YLDLRHTNLGNTGALPSFLCLGNLVYLDISHTRIHIVTECSFCGLDNLRVLKMAGNTFEGHELAGNFKNLTKLHILDISSCQVKHVTPVALAHLRDLRELNISHNNLLSLDAEFFMHLRALTTLDLHSNQLATLTEQVLENLP
TSLKYLDLSWNLFDCSCVHLVFLRWTKKQKDLLQHVRYMVCHSPVDLKDTHLINFDLSYCQVSKTTVAVSVTTFLVLVLFVVLVYKYYFYLYYMVVLLSRDQVSTEKENIYDAFVIYSSEDQEWVTRELEETLEVGVPRFRLC
LYYRDFVPGVSIITNIIKEGFQSSRKVIAVVSPHFLESRWCNFELEVAQSWQLLDSKASLVLVVLEGVDNAVVRQKLGLFRYLRRNTYLVWRDRELNRHMFLRQLKSALLEGKTWTEEELKLMLTN
...

(The sequences only look like they are on multiple lines because they are wrapping.) Note that the Uniprot elements we previously identified have been parsed and replaced, but the description remains unchanged.

# 9.MSA using command line tools (Advanced)

## 9.1.Multiple sequence alignment on the BABS Teaching server

### 9.1.1.Multiple sequence alignment tools on the BABS Teaching server

You can also run these alignment tools via the command line on the BABS teaching server. The module avail command shows what software packages are available:

$ module avail

-------------------------------- /share/apps/modules ---------------------------bbmap/37.02        bowtie/1.2.0       clustalw/2.1       java/8u121
 bedtools/2.26.0    bowtie/2.3.2       fastqc/0.11.5      jellyfish/2.2.6
 blast+/2.6.0       bwa/0.7.15         hisat2/2.0.5       mafft/7.310
 boost/1.63.0       clustalo/1.2.4     java/7u51          muscle/3.8.31
 ----------------------------------

phyml/3.3.20170326 samtools/1.3.1     velvet/1.2.10
phylip/3.696       samtools/0.1.19    trinity/2.4.0
python/2.7.13      tophat/2.1.1
R/3.4.0            trimmomatic/0.36

The three alignment algorithms mentioned above have been highlighted in yellow. You can add them with the module add command:

$ module add clustalo/1.2.4 mafft/7.310 muscle/3.8.31

Each has a slightly different way of calling the program and specifying input/output formats. Rather than worrying about this, we will use a program as part of the SLiMSuite package from the Edwards lab, which acts as a "wrapper" for these tools. SLiMSuite has a number of other tools and functions that can be useful, which we will explore along the way.

### 9.1.2.Reformatting Uniprot files to SLiMSuite format

For this exercise, you will need the reformatted Uniprot file from the previous section:

tlr4.uniprot.2017-08-28.fas

If you have already made it, copy across your  **NSCUK81EOG090701X7.fas**  file in SLiMSuite format. Otherwise, create this file containing our BUSCO protein with the SLiMSuite name format (see  **SLiMSuite format fasta files** for details):

\>eog\_NOTSC\_\_NSCUK81EOG090701X7 EOG090701X7:ts\_mother.Q25k81L500.fasta:11599273:5156-9185
MEMNLTTIPSGIPNTTQTLDLSFNPLKTLHSNYFSAVFALRFLDLARCHLWKIEDNAFMGLNSLSVLILTGNPLQILGLRAFHGLPSLQRFVAVETNLFSLGTLPIGHLTSLQELNLSHNHIDSLKLPGYFSYLISLQHLNFQLNKISSISVGDLDALASPNLTLVLSRNDIKHIERKAFAGLHFQQLALRGCFEDKVIMQASIQNMSGLHVNSLLLGDYRDISKVESIDQSLLNVLCDLYLQELTVIEMDSLETGSTLSPCLNNISRVRVIHTYFGEDFMFPSNSNISHLEFKNCGLDAVPAQNLPSLTKLRVLQITHTKYLRDFEKYFEGLQNLETLDLSVNRLDTHLSWVELLEGTPNLKHLNLSFNTKIRLEIECNGPGKLEYLDFQHTALASPGTVPSFFCLNHLIYLDISYTDTTVISQCSFCGLHSLRVLKMAGNCFANNQLVDNFRNLTKLHFLDISNCQLKYISLSSLTSLHELRLLNVSHNKLLGLHPETYMNFPLLTTLDFHNNQLAALTEEDLKNLPASLKHVDLSANLFDCSCDHAHFLRWVKNSSALLRNVQNMVCYSPSDLKNVQVMDFVLASCEISTTTVAVSVTVVLVLIVILILCYKYYFYLYYIMVLFLGNKFSEEKETVYDAFVIFSSKDQEWVKQELQQPLEEELPYFHLCLFYRDFIPGVSIITNIIKEGFQSSRKVIAVVSDHFLESRWCNFELEVAQSWQLVESKASLILVVLDGVDKAALHHKLGLFRYLRRNTFLTWKDRDLSRHVFLRQLRSALLEGKTWTEDELKLMLKNG

Finally, we need to put our BUSCO protein and the Uniprot proteins in the same file to align. Again, we can use  **cat**  for this and redirect the output into a new file with  **\>** :

$ cat NSCUK81EOG090701X7.fas tlr4.uniprot.2017-08-28.fas \> tlr4.2017-08-28.unaligned.fas

Notice how we are beginning to accumulate multiple files with similar names: this is why lab book documentation is so important to keep a clear record of what is what!

### 9.1.3.Generating multiple sequence alignments

We can now use SeqSuite seq again to "wrap" our aligners and make alignments:

$ module add clustalo/1.2.4 mafft/7.310 muscle/3.8.31

$ python /share/apps/slimsuite/tools/seqsuite.py seq -seqin tlr4.2017-08-28.unaligned.fas -align -alnprog clustalo -seqout tlr4.2017-08-28.clustalo.fas

$ python /share/apps/slimsuite/tools/seqsuite.py seq -seqin tlr4.2017-08-28.unaligned.fas -align -alnprog muscle -seqout tlr4.2017-08-28.muscle.fas

$ python /share/apps/slimsuite/tools/seqsuite.py seq -seqin tlr4.2017-08-28.unaligned.fas -align -alnprog mafft -seqout tlr4.2017-08-28.mafft.fas

Now copy these onto your computer and look at them in AliView. Did it work?

**CHALLENGE:**  Now see if you can go through the whole process with a different BUSCO gene of your choice.

# 10.Filtering sequences with command line tools (Advanced)

We have already seen how it is possible to use online tools to select sets of proteins to look at. This is perfectly sufficient for your prac reports and so you can stick with this approach if you like. However, there are some drawbacks with doing it this way.

The main problem is one of documenting and reproducing methods. Although you can (i.e. MUST) document the rationale behind your selection of proteins, it will not always be possible to do this in a way that would guarantee the same outcome should you repeat the exercise. For example, selecting "5 birds" is a valid motive but which 5 birds do you pick? Next time, you might pick a different five. Using command line rules-based filtering enforces a certain clarity of the rules and should enable the same filtering to be performed consistently.

Another big advantage is that once you have picked up the commands, it can be a lot quicker, especially if you want to run on multiple sets of data.

We are going to look at six main filtering strategies:

1. E-value filtering (BLAST/GABLAM)
2. Top Hit filtering (GOPHER)
3. Species filtering (SeqSuite)
4. Non-redundancy filtering (GABLAM)
5. %identity filtering (GABLAM)

For this, we are going to use the ** full file of 1000 BLASTP hits ** you downloaded from Uniprot during  **Section 5**. Make yourself a new  **analysis/**  directory (and Lab Book page), e.g.  **2017-08-28.Filtering/** , and copy that file ( **tlr4\_hits.full1000.fasta** ) into it.

Before going further, we will reformat the sequence names as described in  **Section 8.3** :

$ python /share/apps/slimsuite/tools/seqsuite.py seq -seqin tlr4\_hits.full1000.fasta -gnspacc -seqout tlr4\_hits.full1000.fas

We will also want the reformatted BUSCO protein from earlier, so copy that over too, e.g.

$ cp ../2018-08-27.TLR4/NSCUK81EOG090701X7.fas .

**NOTE:**  Your path and/or file names might be different. But that's OK because you've documented it in LabArchives, right?

## 10.1.E-value filtering (BLAST/GABLAM)

SLiMSuite contains a useful wrapper for BLAST called GABLAM (Global Analysis of BLAST Local AlignMents): [http://rest.slimsuite.unsw.edu.au/gablam](http://rest.slimsuite.unsw.edu.au/gablam).

This can be used to pull BLAST hits directly into a fasta file ( **fasout=T** ), applying some filters along the way. The easiest filter to play with is the BLAST e-value. As we discussed before, this is not very stringently applied to Uniprot BLAST searches. We could instead choose to be super-strict with an e-value of 1e-100 **(blaste=1e-100**):

$ module add blast+/2.6.0

$ python /share/apps/slimsuite/tools/gablam.py -seqin NSCUK81EOG090701X7.fas -searchdb tlr4\_hits.full1000.fas fasout=T fasdir=EFILTER blaste=1e-100 basefile=efilter

You should get output to the screen that looks something like this:

Append file: /home/z3452659/babs3291/analysis/2017-08-28.Filtering/efilter.log

GABLAM V2.28.1 run: Fri Aug 25 16:33:20 2017

  ###########################################################################################################
  #|#\> GABLAM version 2.28.1 : Global Analysis of BLAST Local AlignMents                                 \<#|#
  #|#\> ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ \<#|#
  #|#\> Copyright (c) 2006 Dr Richard J. Edwards. \<#~#\> Last Modified: July 2017                          \<#|#
  #|#\> ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ \<#|#
  #|#\> Disclaimer: GABLAM comes with ABSOLUTELY NO WARRANTY;                                             \<#|#
  #|#\>   This is free software, and you are welcome to redistribute it;                                  \<#|#
  #|#\>   For details see attached license file (gnu\_general\_public\_license.txt)                          \<#|#
  #|#\>   or http://www.gnu.org/copyleft/gpl.html.                                                        \<#|#
  #|#\> ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ \<#|#
  #|#\> Please cite: Davey, Shields & Edwards (2006), Nucleic Acids Res. 34(12):3546-54. [PMID: 16855291] \<#|#
  ###########################################################################################################

Append file: /home/z3452659/babs3291/analysis/2017-08-28.Filtering/efilter.log

#VIO     00:00:00    Verbosity: 1; Interactivity: 0.
#NCBI    00:00:00    Installation of BLAST+ detected. Path not required.
#MODE    00:00:00    FullBLAST=True; KeepBLAST=True.
#LOAD    00:00:00    Load sequences from tlr4\_hits.full1000.fas
#SEQ     00:00:00    1,000 of 1,000 sequences loaded from tlr4\_hits.full1000.fas.index (Format: index).
#LOAD    00:00:00    Load sequences from NSCUK81EOG090701X7.fas
#SEQ     00:00:00    1 of 1 sequences loaded from NSCUK81EOG090701X7.fas.index (Format: index).
#IO     00:00:00    QueryDB=NSCUK81EOG090701X7.fas; SearchDB=tlr4\_hits.full1000.fas; BLASTRes=None.
#NCBI    00:00:00    Installation of BLAST+ detected. Path not required.
#PROG    00:00:00    BLAST Program OK (blastp): protein vs protein
#DB     00:00:00        makeblastdb -in "tlr4\_hits.full1000.fas" -out "tlr4\_hits.full1000.fas" -title "/home/z3452659/babs3291/analysis/2017-08-28.Filtering/tlr4\_hits.full1000.fas" -parse\_seqids -dbtype prot
#LOAD    00:00:00    Load sequences from NSCUK81EOG090701X7.fas
#SEQ     00:00:00    1 of 1 sequences loaded from NSCUK81EOG090701X7.fas.index (Format: index).
#FILT    00:00:00    1 of 1 sequences retained.
#DIS     00:00:00    QueryDB and SearchDB differ: no Distance Matrix output. Setting dismat=F.
#NCBI    00:00:00    Installation of BLAST+ detected. Path not required.
#SYS     00:00:00    blastp -query NSCUK81EOG090701X7.acc.fas -db tlr4\_hits.full1000.fas -out efilter.blast -seg no -comp\_based\_stats F -soft\_masking true -evalue 1.000000e-100 -num\_descriptions 1000 -num\_alignments 1000
#RES     00:00:01    Generating GABLAM output from full BLAST results: efilter.blast
#NCBI    00:00:01    Installation of BLAST+ detected. Path not required.
#BLAST   00:00:03    Reading efilter.blast blastp BLAST results complete: 1 searches; 435 hits (vs 1,000 Seq; 767,236 letters)
#FORMAT  00:00:03    Reformatting Run complete: 0 format errors
#FORMAT  00:00:03    Reformatting Search complete: 0 format errors
#FORMAT  00:00:03    Reformatting Hit complete: 0 format errors
#FORMAT  00:00:03    Reformatting Local complete: 0 format errors
#FORMAT  00:00:03    Reformatting GABLAM complete: 0 format errors
#GABLAM  00:00:03    Executing multiGABLAM extraction of full BLAST results.
#TABLE   00:00:03    Empty Table "Full" added: 27 fields; 0 entries.
#GABLAM  00:00:03    Processing GABLAM Data complete.
#SAVE    00:00:03    Table "Full" saved to "efilter.gablam.tdt": 435 entries.
#INFO    00:00:03    BLAST Local Hit Length Cutoff: 0
#INFO    00:00:03    BLAST Local Hit %ID Cutoff: 0.0%
#FIELD   00:00:03    Field "Query" renamed "Qry" in table "Local" (0 entries w/o data)
#Key     00:00:03    Key updated ("Query" renamed "Qry") in table "Local".
#FIELD   00:00:03    Field "AlnID" renamed "AlnNum" in table "Local" (0 entries w/o data)
#Key     00:00:03    Key updated ("AlnID" renamed "AlnNum") in table "Local".
#FIELD   00:00:03    Field "QrySeq" removed from table "Local"
#FIELD   00:00:03    Field "SbjSeq" removed from table "Local"
#FIELD   00:00:03    Field "AlnSeq" removed from table "Local"
#DROP   00:00:03    15 Local fields reduced to 12 fields
#SAVE    00:00:03    Table "Local" saved to "efilter.local.tdt": 435 entries.
#LOAD    00:00:03    Load sequences from NSCUK81EOG090701X7.fas
#SEQ     00:00:03    1 of 1 sequences loaded from NSCUK81EOG090701X7.fas.index (Format: index).
#FIELD   00:00:03    Added field "HitNum" to table "HitSum"
#JOIN    00:00:03    New field "TempCompressFieldIndex" (Qry) generated for "HitSum"
#INDEX   00:00:03    Indexed "HitSum" on "TempCompressFieldIndex": 1 unique; 0 missing entries
#FIELD   00:00:03    Field "TempCompressFieldIndex" removed from table "HitSum"
#KEY     00:00:03    Keys remade for 1 HitSum table entries.
#CMPRSS  00:00:03    Compressed table "HitSum": 5 fields; 1 entries
#FIELD   00:00:03    Added field "Description" to table "HitSum"
#FIELD   00:00:03    Field "Hit" removed from table "HitSum"
#FIELD   00:00:03    Field "Score" renamed "MaxScore" in table "HitSum" (0 entries w/o data)
#NULL    00:00:03    0 BLAST searches w/o hits added to HitSum.
#SAVE   00:00:03    Table "HitSum" saved to "efilter.hitsum.tdt": 1 entries.
#LOAD    00:00:03    Load sequences from tlr4\_hits.full1000.fas
#SEQ     00:00:03    1,000 of 1,000 sequences loaded from tlr4\_hits.full1000.fas.index (Format: index).
#INDEX   00:00:03    Indexed "Hit" on "Query": 1 unique; 0 missing entries
#OUT     00:00:04    435 Sequences output to EFILTER/NSCUK81EOG090701X7.fas
#LOG     00:00:04    GABLAM V2.28.1 End: Fri Aug 25 16:33:24 2017

This output has also gone into  **efilter.log**. A bunch of other  **efilter.\***  files have been created:

efilter.blast  efilter.gablam.tdt  efilter.hitsum.tdt  efilter.local.tdt  efilter.log

We'll explore some of these later. (You can look at the GABLAM manual if you are curious in the meantime, although it's a little out of date.) In addition, there is now an EFILTER/ directory. This contains the file of filtered output sequences from our original set of 1000 sequences:

$ ls EFILTER/
NSCUK81EOG090701X7.fas

These output names were set with the  **fasout=T fasdir=EFILTER**  and  **basefile=efilter**  settings given to GABLAM.

**The log file**
 Every SLiMSuite program generates a \*.log file with key details of the run. The name of this file is either set with log=FILE or basefile=PREFIX (as above). The latter also sets the prefix for results files, depending on the program. By default, the log is named after the program run. (Look in the directory you used for sequence renaming and aligning in Task 9.) Changing the name makes it easier to keep logs associated with the actual task being performed, in addition to having multiple separate logs of different runs in the same directory.

**Question: ** Look through the log file and see if you can identify key details from the run:

Can you identify the BLAST command that was run by GABLAM?

Can you identify the  **makedb**  command used to format the database for BLAST searching? (NOTE: If the search database has already been formatted, this will be reported in place of the makedb command.)

How many sequences passing the e-value filter were output into the NSCUK81EOG090701X7.fas file?

**Question:**  Which command line options set (a) the BLAST query file? (b) the search database file?

**NOTE: ** E-values are dependent on the size of the BLAST search database, so you will get different e-values for this BLAST search than you did for the same sequence when it was in the Uniprot database. This is one reason why e-value cut-offs are not useful for anything beyond crude filtering.

**CHALLENGE:**  See if you can repeat the exercise against a file of chordate Uniprot proteins that has been dowloaded onto the server. Make sure that you give it different output filenames and fasta directory with the fasdir=EFILTER and basefile=efilter settings. The Uniprot sequences can be found here:

/share/data/babsgenome/uniprot/uniprot.chordata.2017-07-27\_all.fas

**Question: ** If you performed the search against uniprot.chordata.2017-07-27\_all.fas, did you get the same number of hits with e \<= 1e-100? What might be the cause of any difference?

**CHALLENGE:**  GABLAM can be used for multiple query sequences. See if you can make a new query file with a couple of different BUSCO protein sequences. (Make sure they are named correctly, as in Task 9.) Try searching this against the Uniprot file above. How many files do you now get in your fasout=PATH directory?

## 10.2.Top Hit filtering (GOPHER)

As we have seen, filtering by e-value has limited value. It is good at ruling out rubbish but not good at producing a definitive list. You will also see if you look at the filtered sequence file ( **grep '\>'** ) that we still have multiple sequences from the same species, which may just reflect sequence variants.

An alternative approach is to limit ourselves to the best hit from each species based on global percentage identity. This can be done quite easily with the program GOPHER. GOPER will also make an alignment, so we need to add our multiple sequence alignment modules if they are not already loaded.

$ module add clustalw clustalo muscle mafft
$ python /share/apps/slimsuite/tools/gopher.py -seqin NSCUK81EOG090701X7.fas -orthdb tlr4\_hits.full1000.fas basefile=tlr\_gopher orthalign

Note that the command line options are slightly different to GABLAM.  **seqin**  stays the same for the query but we now use  **orthdb**  rather than  **searchdb**  for the database of potential orthologues.

**NOTE: ** This is where the sequence naming format begins to become important. GOPHER parses out the Uniprot species codes from the sequence names. If it cannot correctly assign species, it will be unable to pick the top hits.

Because it is doing the alignment, GOPHER will take a bit longer to run than GABLAM did. If we omit the orthalign command, it will also make a crude tree, which will take even longer. This is not recommended during the prac, when the server is probably quite busy, but you can always try a different time if you are curious.

## 10.3.GOPHER Results

GOPHER is designed to run on multiple proteins and re-use results when they are found. As such, it organises its output in a very controlled way. You should now have a directory named after your orthdb file, in which there is a NOTSC/ subdirectory (where GOPHER will store results for all tiger snake queries run against this database), in which are subdirectories of output files:

$ ls -R tlr4\_hits.full1000/

tlr4\_hits.full1000/:
NOTSC

tlr4\_hits.full1000/NOTSC:
BLAST  clustaloALN  ORTH  PARA

tlr4\_hits.full1000/NOTSC/BLAST:
NSCUK81EOG090701X7.blast  NSCUK81EOG090701X7.blast.id  NSCUK81EOG090701X7.qry

tlr4\_hits.full1000/NOTSC/clustaloALN:
NSCUK81EOG090701X7.orthaln.fas

tlr4\_hits.full1000/NOTSC/ORTH:
NSCUK81EOG090701X7.orth.fas  NSCUK81EOG090701X7.orth.id

tlr4\_hits.full1000/NOTSC/PARA:
NSCUK81EOG090701X7.closepara.id

You can look up the GOPHER manual if you want more information on these output files. The key ones for this exercise are:

- **tlr4\_hits.full1000/NOTSC/ORTH/NSCUK81EOG090701X7.orth.fas**  = the fasta file of species top hits
- **tlr4\_hits.full1000/NOTSC/clustaloALN/NSCUK81EOG090701X7.orthaln.fas**  = the same set of sequences aligned with Clustal Omega.

**CHALLENGE:**  Note that the alignment program is part of the ALN/ directory name. Try re-running with  **alnprog=muscle**  and see what happens.

Now try running on the Uniprot file:

$ python /share/apps/slimsuite/tools/gopher.py -seqin NSCUK81EOG090701X7.fas -orthdb /share/data/babsgenome/uniprot/uniprot.chordata.2017-07-27\_all.fas basefile=chordate\_gopher orthalign

You will get another directory,  **uniprot.chordata.2017-07-27\_all/** , in which these results go.

**CHALLENGE:**  See what happens if you give GOPHER a  **seqin**  file with multiple BUSCO query sequences. (Make sure they have the right name format!)

## 10.4.Species filtering (SeqSuite)

As you will have seen, we are still getting a lot of proteins, even when picking only the top hit for each species. This is because TLR4 is an important and interesting protein, which has been sequenced in many organisms. When selecting a subset of proteins from Uniprot, we used the species as a guide for picking some phylogenetically distinct sequences. We can do a similar thing using SeqSuite. Again, the advantage here is that it will be quicker and easier if we ever need to consistently repeat this filtering.

For this, we can use the SeqSuite seq function again, this time with countspec=T to get counts of the number of sequences for each species code:

$ python /share/apps/slimsuite/tools/seqsuite.py seq -seqin tlr4\_hits.full1000.fas countspec=T -basefile tlr4\_hits.full1000.spec

The tlr4\_hits.full1000.spec.log file produced now contains a list of all the species codes found in the file and the number of sequences for each one. You can use this in conjunction with the table of hits you downloaded from Uniprot to pick some species for further analysis. You can also look up species codes at [http://www.uniprot.org/taxonomy/](http://www.uniprot.org/taxonomy/). This can be used to find the species for a species code, or vice versa.

A little quicker is to use the Uniprot species list file that has been download onto the server:

/share/data/babsgenome/taxonomy/speclist.2017-08-25.txt

Use  **more**  to take a look at the general structure of this file. This can be used with grep to find species or decode species codes. The -A flag will return a number of lines after the matched pattern, allowing you to pull out the common name using a species code:

$ grep -A 2 OPHHA /share/data/babsgenome/taxonomy/speclist.2017-08-25.txt

OPHHA E    8665: N=Ophiophagus hannah
                 C=King cobra

Similarly, the -B flag pulls out lines before the match, allowing species codes to be found for species of interest:

$ grep -B 1 -i "tiger snake" /share/data/babsgenome/taxonomy/speclist.2017-08-25.txt

MYRMA E  391189: N=Myrichthys maculosus
                 C=Tiger snake eel
--
NOTAT E  111176: N=Notechis ater
                 C=Black tiger snake
--
NOTSC E   70142: N=Notechis scutatus scutatus
                 C=Mainland tiger snake
                 S=Common tiger snake
--
NOTSN E 1027870: N=Notechis scutatus niger
                 C=Peninsula tiger snake

For convenience here, I am going to make a file that contains the species codes of the TLR4 proteins I selected from Uniprot in  **Section 5** :

$ cat \> wanted.spec

OPHHA
ANOCA
ALLMI
STRCA
CALAN
TAEGU
CHEMY
CHICK
ORNAN
MONDO
AILME
PIG
BOVIN
HUMAN
MEGAM
DANRE
ASTMX
TAKRU

**Remember: ** CTRL+C will kill this "interactive" cat and close the file.

This species code list can then be used by SeqSuite to extract a subset of sequences from a file:

$ python /share/apps/slimsuite/tools/seqsuite.py -seqin tlr4\_hits.full1000.fas -goodspec wanted.spec -seqout tlr4\_hits.wanted.fas -basefile specfilter

...
#LOAD   00:00:00        Load sequences from tlr4\_hits.full1000.fas
#FILT   00:00:00        Filter on GoodSpec: 18 Spec
#SEQ    00:00:00        1,000 of 1,000 sequences loaded from tlr4\_hits.full1000.fas.index (Format: index).
#FILT   00:00:00        198 of 1,000 sequences retained.
#FILT   00:00:00        802 sequences filtered on GoodSpec
#OUT    00:00:00        198 Sequences output to tlr4\_hits.wanted.fas

My list included a few model organisms, which might explain why we still have, on average, more than 10 hits per species! Clearly, more filtering needs to be done...

## 10.5.Non-redundancy filtering (GABLAM)

Using GOPHER is a convenient way to quickly generate alignments against single top hits from different species. However, this glosses over the fact that there may be multiple genuine hits from the same species that are of interest. This is particularly likely when looking at a protein from a gene family. (BUSCO genes are meant to be single copy, so the danger is quite low for these.)

An alternative approach, we can filter sequences based on their similarity to each other. The aim here is to remove sequences that are probable variants but leave more diverse sequences that might represent different members of a gene family.

GABLAM can also be run to BLAST a sequence file against itself and perform this redundancy filter by omitting the  **searchdb=FILE**  command and running with  **nrseq=T** :

$ python /share/apps/slimsuite/tools/gablam.py -seqin tlr4\_hits.wanted.fas nrseq=T nrcut=99.0 nrsamespec=T -basefile tlr4\_hits.wanted.nrspec

This will take a few minutes to run. (You can make it run faster by choosing fewer species and/or species with fewer sequences in the step above.)

The  **nrcut=X**  setting determines the cut-off for the non-redundancy filter. In this case, we have set it to 99%, meaning that pairs of sequences with \>=99% redundancy will be reduced to a single representative.

...
#REJ    00:00:07        tr\_BOVIN\_\_Q6WCD4 (99.6%) vs tr\_BOVIN\_\_Q6WCD5 (99.6%): Q6WCD4 rejected - 839 vs 841 non-X positions
#REJ    00:00:07        tr\_BOVIN\_\_Q6WCD5 (99.8%) vs tr\_BOVIN\_\_Q8SQ55 (99.8%): Q8SQ55 rejected - Decision based on accnum sorting
#REJ    00:00:07        tr\_BOVIN\_\_Q6WCD5 (99.9%) vs TLR4\_BOVIN\_\_Q9GL65 (99.9%): Q6WCD5 rejected - Swissprot vs non Swissprot
#NR     00:00:07        GABLAM NR filter, OrderedAlnID \>= 99.0%: 129 of 198 sequences rejected.
#FILT   00:00:07        129 sequences filtered on BadAcc
#OUT    00:00:12        69 Sequences output overwriting tlr4\_hits.wanted.nrspec.nr99.fas
#LOG    00:00:12        GABLAM V2.28.1 End: Fri Aug 25 22:52:05 2017

This will preferentially retain SwissProt (curated) sequences over others, and then choose the sequence with the most defined (non-X) amino acids. In the case of a tie, the alphabetically first sequence is kept.

Note how the percentage identity of the NR filter is now in the output name, e.g.  **\*.nr99.fas**. You can re-run with a different nrcut=X value and it will re-use the same BLAST and GABLAM results, making the filtering quicker. This way, you can experiment with different values.

**What makes a good redundancy cut-off?**
 Every protein is different - both in terms of functional constraint (and thus evolutionary rate) but also in terms of how well it has been sampled from different species. It is therefore tricky to come up with a one-size-fits all solution. Generally speaking, 95% is probably good for most annotation/phylogeny analyses but when you have lots of sequences you might even want to go lower.

## 10.6.Species-independent identity filtering

You might have noticed the nrsamespec=T setting. This restricts the filtering to pairs of sequences from the same species. This can be switched off to eliminate even more sequences in the situation where you have a lot of closely related species:

$ python /share/apps/slimsuite/tools/gablam.py -seqin tlr4\_hits.wanted.fas nrseq=T nrcut=95.0 nrsamespec=F -basefile tlr4\_hits.wanted.nr

You can even set the order of preference of species to keep with  **nrspec=LIST** , which will be applied when sequences are otherwise just as good as each other. This allows you to favour model organisms, for example, and get more consistent species selections over multiple datasets.

## 10.7.%identity filtering (GABLAM)

We have already seen how GABLAM can take an e-value cutoff value and that it is not particularly helpful. More usefully, GABLAM can also apply a minimum GLOBAL percentage identity for hits versus the query protein, set by  **gablamcut=X**. e.g. to keep sequences with 40%+ global identity to our BUSCO protein:

$ python /share/apps/slimsuite/tools/gablam.py -seqin NSCUK81EOG090701X7.fas -searchdb tlr4\_hits.full1000.fas fasout=T fasdir=GLOB40 gablamcut=40 basefile=glob40

**NOTE:**  GOPHER, by default, also imposes a 40% minimum global similarity ("Positives") filter. This can be changed with  **minsim=X**. It can also take a list of desired species with  **goodspec=LIST**.

![](RackMultipart20230102-1-ssjimi_html_c1fddc204e4a99af.gif)

MEGA (Molecular Evolutionary Genetics Analysis) is a widely used GUI-driven application for phylogenetics and molecular evolutionary analyses. MEGA has extensive online documentation (see the MEGA homepage at [http://www.megasoftware.net/](http://www.megasoftware.net/)), papers and even a book! The purpose of this handout is _not_ to replace any of this documentation. MEGA has many functions and options and this handout is designed to focus your attention some of the key analysis and phylogenetics options. Feel free to explore the other functions, and even use them in your final report if you like.

**NOTE:** Questions in yellow can be answered collaboratively and will have answers provided. "Tasks" form part of the assessable activities to be submitted through the Part 1 assignment. Feel free to discuss these with your peers, but **you must complete the submissions independently**.

# 11.Basic nucleotide analysis with MEGA

This first section will introduce the basics of getting your data into MEGA and generating some basic summary statistics using the different analysis tools that come with the program.

## 11.1.Accessing MEGA

M ![](RackMultipart20230102-1-ssjimi_html_875b6f6224f9312.png) EGA is free to download from [http://www.megasoftware.net/](http://www.megasoftware.net/). It works very well in Windows, but the Mac OSX version is not as good prior to MEGAX. We have therefore made MEGA7 available through **UNSW myAccess** ([https://www.myaccess.unsw.edu.au/](https://www.myaccess.unsw.edu.au/)). If you have not used **myAccess** before, follow the onscreen instructions to get set up and then **Open** the **MEGA7** app (right) from the list of available applications. This should open up the main MEGA window (below).

**NOTE:** In this handout, we will be using **MEGA7** for consistency with UNSW machines but most of the functions should be the same in other versions of MEGA. Please contact UNSW IT for support if you have any trouble using **myAccess**.

![](RackMultipart20230102-1-ssjimi_html_e3a64d200a8cc1dc.png)

**N ![](RackMultipart20230102-1-ssjimi_html_e88e4671f5cecb39.png) OTE:** If using MEGA7 through **myAccess** , make sure that you give the application **Read & Write** access.

It is easiest to use your **hdrive** for getting data in and out of **myAccess** applications. (You can also use this drive analysis using a local MEGA installation.) See Lab Archives for details.

## 11.2.Opening a coding sequence alignment with MEGA

For this prac, we have provided an alignment of a coding DNA sequence from five snakes: our two "BABS Genome" species and three other snake species for which data was available. The coding sequence selected is (predicted) for the melanocortin 1 receptor (MC1R), which you might remember from year 2 genetics lectures. MC1R is a G protein-couple receptor, which sits on the surface of melanocytes and is involved in the regulation of producing the pigment melanin. MC1R is therefore a key protein in body colouration, frequently mutated in "melanic" (black) colour morphs in mammals. Tiger snakes are known to have different skin pigmentation in different populations. More generally, body colouration is a common (and obvious) target for natural selection. It therefore makes an interesting gene to look at.

- Open the **mc1r\_snake\_CDS.nocodons.fas** file by selecting **File » Open A File/Session …** and finding the file in the dialogue box.

![](RackMultipart20230102-1-ssjimi_html_66e1fe95cae8a0e6.png) ![](RackMultipart20230102-1-ssjimi_html_7f3edce97f2f847e.png)

- T ![](RackMultipart20230102-1-ssjimi_html_c14e52eeb7801da6.png) his file has already been aligned, so you want to **Analyze** it. (We will look at making FASTA files and multiple sequence alignments later in the prac.)

- Inform MEGA that these are **Protein-coding Nucleotide Sequences** with a **Standard Genetic Code**.

![](RackMultipart20230102-1-ssjimi_html_c417753273a1e476.png) ![](RackMultipart20230102-1-ssjimi_html_7ee81561b7728ce4.png)

![](RackMultipart20230102-1-ssjimi_html_8d90bc07e20b96e3.png)

You should now see additional buttons in your MEGA workspace: one that opens your data to look at, and one to **Close Data**.

![](RackMultipart20230102-1-ssjimi_html_c79977623ce61d77.png)

- Click on the **TA** button, which will open the sequences in the **Sequence Data Explorer**.

![](RackMultipart20230102-1-ssjimi_html_847c59d13dd36271.png)

You are now ready to explore your data.

## 11.3.Exploring Sequence Data

The first step in any analysis is to familiarise yourself with your data and perform appropriate quality control. (The number one mantra of all bioinformatics is: "Junk in, junk out!") In this case, we think we are working with an **aligned protein-coding sequence**. We therefore want to examine the alignment for evidence that (a) it really is protein-coding, and (b) it is aligned correctly.

- From the **Display** menu, select **Color cells**. This will make each nucleotide a different colour, which will make it easier to see conserved blocks, and differences.
- Make the window wider so that you can see more of the alignment at once, if your screen is big enough. Select **Display » Show Summary View** to show where you are in the alignment at the bottom of the window.

![](RackMultipart20230102-1-ssjimi_html_c66ff09ade0910d3.png)

### 11.3.1.Sequence variation

In this section, we will use the different highlighting buttons, **TA** , **C** , **V** , **Pi** , **S** , **0** , **2** and **4**.

![](RackMultipart20230102-1-ssjimi_html_5a3e710e5a8e9fe9.png)

- When you **Highlight** different positions, the **Color cells** view is disabled. To make differences easier to see when highlighting data, click on **TA** to **Use identical symbol**. This will put the tiger snake (_Notechis scutatus_) sequence above the alignment and change the rest of the sequence to be a **.** when the sequence is the same, or the nucleotide where it is different to the snake sequence.

![](RackMultipart20230102-1-ssjimi_html_329c1d049931750e.png)

- Now look at **C** , **V** , **Pi** , **S** , **0** , **2** and **4**. Mouseover each button to see what it does and then click on it and see how the highlighting changes. See how the information in the bottom status bar also changes.

**Q.** How many conserved (invariant) sites are there?

**Q.** What makes a site "Parsimony informative"? (HINT: look at the numbers for **V** , **Pi** and **S**.)

- **Mark-0-fold degenerate sites** and scroll to the region around position 300. As you scroll, you should see a pattern in the highlighting, with a tendency to have two highlighted positions followed by one non-highlighted one.

**Q.** What causes this pattern?

**Q.** What do the 3bp boxes above the alignment represent?

**Q.** Do the variable positions in this region tend to be highlighted or not highlighted? What does this tell you about the functional constraint on the protein in this region?

### 11.3.2.Alignment quality

- Now scroll back to region 70-90. The dashes are "gaps" in some of the sequences, which are inserted to make the right nucleotides line up.

**Q.** Provide three (or more) possible explanations for the gaps in a sequence.

**Q.** Can you spot anything odd about the pattern of the gaps in the alignment?

**HINT:** Look at the 3bp boxes identified in the previous selection.

The answer to the previous question is actually easier to spot in **Alignment** mode.

- Close the **Sequence Data Explorer** and then **Close Data** in the main window. (There is no need to save the view.)
- Open **mc1r\_snake\_CDS.nocodons.fas** with alignment mode by returning to the main MEGA window and selecting **File » Open A File/Session …** again, but this time selecting **Align** rather than **Analyze**.
- Click the **Translated Protein Sequences** tab (using the Standard Genetic Code) and look at positions 25, 28 and 29.

![](RackMultipart20230102-1-ssjimi_html_17f233e0ec970640.png)

**Q.** What do the question marks represent?

### 11.3.3.Fixing the alignment

Because some of sequences contains partial codons flanking the gap, the translation tool in MEGA cannot assign amino acids unambiguously.

- Toggle back to the **DNA sequences** and count the number of gapped positions the _Chionactis occipitalis_ (Western shovelnose snake) sequence in the region 70-90 that you were looking at before.

**Q.** How many codons should this represent? How many amino acid positions seem to be affected when viewing the protein sequence? What might be the cause of this?

The alignment you have been using so far was a default MUSCLE alignment of the coding sequences. MEGA also has an option to align the sequences, explicitly using the information that these are coding sequences.

- Realign the sequences using: **Alignment » MUSCLE – codons**. When asked, remove all the existing gaps prior to realignment. Ignore the reported stop codons – these are at the end of the coding sequence.
- Now translate to protein and look at region 70-90 again. How many ambiguous amino acids are there now? How many amino acids are affected by the indel?
- Save the alignment in FASTA format ( **Data » Export Alignment » FASTA format** ). Before saving, you might want to edit the sequence names to make them more human-friendly. You can do this by double-clicking on a sequence name and then editing.

**NOTE:** If you have problems saving your alignment, and/or you are running low on time, you can use the provided **mc1r\_snake\_CDS.codons-edit.fas** file, which has the realigned sequences with edited sequence names.

- Now close the alignment window and open the new alignment file to **Analyze** as before.

### 11.3.4.Sequence variation revisited

**TASK.** Using the codon-corrected alignment, fill in Table 1 and calculate the % variable sites for each category. Based on these numbers, do you think the MC1R protein is predominantly evolving: (a) neutrally, (b) adaptively, or (c) under functional constraint?

Table 1. Variant sites in MC1R alignment.

| **Site type** | **Variable** | **Total** | **% Variable** |
| --- | --- | --- | --- |
| **Nucleotide** |
 |
 |
 |
| --- | --- | --- | --- |
| **Protein** |
 |
 |
 |
| **4-fold degen** |
 |
 |
 |
| --- | --- | --- | --- |
| **2-fold degen** |
 |
 |
 |
| **0-fold degen** |
 |
 |
 |

**NOTE:** Not all positions can be unambiguously assigned as 0-, 2- or 4-fold degenerate, so the numbers from the bottom half of the table will not add up to the total nucleotide variation. (If you select a subset of the sequences, you will see these numbers change.)

### 11.3.5.Sequence composition

- Use the " **Statistics » Nucleotide composition**" function to calculate the average nucleotide proportions over the eight species.

**TASK.** Fill in Table 2:

Table 2. Nucleotide composition of MC1R alignment.

| **%nt** | _ **3 H-bond** _ | _ **2 H-bond** _ | _ **Total** _ |
| --- | --- | --- | --- |
| _**Purine (Heavy)**_ | **G:** | **A:** |
 |
| --- | --- | --- | --- |
| _**Pyrimidine (Light)**_ | **C:** | **T(U):** |
 |
| _ **Total** _ |
 |
 |
 |
| --- | --- | --- | --- |

- Use the " **Statistics » Nucleotide Pair Frequencies » Unidirectional**" function to calculate the average nucleotide difference over the eight species:

**TASK.** What is the average transition/transversion ratio (R)?

# 12.Evolutionary models

Now that you have a high-quality alignment and some basic statistics regarding nucleotide statistics etc., we will use MEGA to explore different models of evolution.

## 12.1.Picking an appropriate model of evolution

It should be quite apparent from your analysis in the previous section that there are some biases in the way that nucleotides are used, and replace each other, in the MC1R coding sequence. The purpose of an evolutionary model is to capture these biases in order to improve the way that distances are estimated.

There are many different models of nucleotide evolution. First, we will use a simplified decision tree to decide which of five models of increasing complexity we think best fits the data.

- Use your data from Table 2 to work through the decision tree below.

**Q.** Why don't we automatically apply the most complex model we can derive?

**Q.** Which model do you think is most appropriate for the MC1R data?

**Q.** How can you decide whether a bias is strong enough to answer "Yes" or "No" to the bias questions?

![](RackMultipart20230102-1-ssjimi_html_d9ac70f788f9fa5c.png)

By default, these models are applied equally to all positions in the alignment.

**Q.** Look back at your answers in section 11.3.4. Do you think all the positions are evolving with the same rates and biases? If not, why not?

## 12.2.Maximum likelihood model fitting

MEGA provides a maximum likelihood model fitting function, so you don't need to make these calculations manually. The pattern of substitutions in a phylogeny can be modelled in a large number of ways, including a wide variety of assumptions about the underlying evolutionary processes.

MEGA includes six different models, with the following core assumptions:

- Jukes, Cantor (JC): equal base frequencies, one substitution rate
- Kimura 2-parameter (K2): equal base frequencies, transition and transversion rates differ.
- Tamura 1992 (T92): K2 with GC bias in base frequencies.
- Hasegawa, Kishino, Yano 1985 (HKY): K2 but with unequal base frequencies.
- Tamura and Nei 1993 (TN93): unequal base frequencies, 2 transition rates and 1 transversion rate.
- Generalised time-reversible (GTR): unequal base frequencies, each pair of bases has its own rate parameter.

Differences in rates across positions can also be accounted for with two additional assumptions:

- Substitution rates vary across sites according to a Gamma distribution (+G)
- A fraction of sites are invariant (+I), meaning they do not evolve.

The last two assumptions can be combined (together or separately) with one of the six models above to generate further models.

**Q.** What does "TN93+I" mean?

**Q.** What is likely to be responsible for differences in substitutions rates across sites (+G)?

**Q.** What kind of selection is acting at invariant sites (+I)?

### 12.2.1.Testing a range of substitution models using BIC

MEGA can be used to explore many alternative models using a statistical approach called model selection using the Bayesian Information Criterion (BIC). This BIC quantity is computed for each model and the model with the lowest BIC is the one best able to describe the data. In this methodology, models that fit the data well have a lower BIC as do models with fewer parameters.

- Use the Models function in MEGA (select "**Find best DNA/Protein models (ML)**") to investigate the data and range of models.

**Q.** What are the 13 parameters in the Jukes-Cantor (JC) model?

- Export the models to Excel and plot **lnL** versus **#Param**. (The highest lnL is best.)
- Now plot **BIC** against **#Param**.

**Q.** Compare and contrast the relationships you have just plotted. Why do think BIC is favoured over lnL?

**TASK.** Answer the following:

1. Out of JC, K2, T92 and TN93 (section 12.1), which did you identify as the best model and why? Do the BIC scores confirm or reject your conclusion?

1. You have been assigned a set of assumptions on Teams. Using all the assumptions you have been assigned, identify the most appropriate model (give its abbreviation - for example, Jukes-Cantor without invariant sites but with gamma distributed rates is JC+G).

1. What is the BIC support for that model?

1. What model has the best support? What's the numerical difference between your model and the best BIC?

1. What model has the lowest support? What's the numerical difference between your model and the worst BIC?

1. Why doesn't the model selection analysis using BIC favour the most complicated model?

1. Do the results support different rates across sites? If so, do you think it is necessary to invoke both a Gamma distribution of varying rates and a fraction of invariant sites? Explain your answer.

# 13.Testing for deviations from neutrality

Once we have established suitable models of evolution, we typically want to interrogate substitutions for any signs that the sequences are not evolving consistently and neutrally. There are two tests that are commonly applied: (1) testing for deviations from a molecular clock, and (2) testing for signs of selection.

## 13.1.Testing the molecular clock using a relative-rates test

One of the big predictions of predictions of the Neutral Theory is the molecular clock. It is therefore of interest to ask whether the molecular clock seems to be operating for the genes and species of interest in a given analysis. Alternatively, does the rate of substitution vary from one branch to another?

We can investigate this by considering patterns of substitution in a phylogeny. Suppose we have a phylogenetic tree of three species as below.

![](RackMultipart20230102-1-ssjimi_html_9256a79e37dade3c.png)

We want to know if the rate of evolution is the same from ancestor A to descendants 1 and 2. In other words, is the average number of substitutions per site along the A-1 branch (_d__1_) equal to that along A-2 (_d__2_)?

**Q.** Why does a distance matrix of 1, 2 and 3 not directly provide these numbers?

The outgroup 3 can help compare the rates. A few different methods exist to do this. We will look at one particular method due to Tajima.

Let _m __1_ be the number of sites whose nucleotide in sequence 1 differs from those in sequences 2 and 3. Similarly, let _m__ 2_ be the number of sites whose nucleotide in sequence 2 differs from those in sequences 1 and 3. These are sites that are likely to have evolved after the internal node at ancestor A.

Is _m __1_ significantly different from _m__ 2_? The expected number of differing sites per branch is (_m __1_+ _m__ 2_)/2. We can test whether the observations are close to expectations using a chi-squared test with test statistic

(_m __1_ – _m__ 2_)2 / (_m __1_ + _m__ 2_)

As you can see, this is large when the difference between the two _m_ values is large.

### 13.1.1.Making a phylogenetic tree

The relative rates test requires use of three species, one of which is the **outgroup**. This in turn requires a phylogenetic tree of the species involved. This could be derived from the known taxonomy. If this is controversial or unknown, the tree itself can be derived from the data. Next week will focus on using MEGA for phylogenetic inference in protein sequences. For now, we are going to infer a phylogenetic tree to use for our neutrality and molecular clock tests.

**N ![](RackMultipart20230102-1-ssjimi_html_81daab467a59c292.png) OTE:** This section assumes basic knowledge of phylogenetic trees from Year 2 Genetics. If the terminology and concepts are unfamiliar to you, it is recommended that you revise the supporting material on Moodle.

- From the main MEGA window, select **Phylogeny » Construct/Test Maximum Likelihood Tree…**
- Select the HKY+G model (+defaults) using **Model/Method** and **Rates Among Sites** options. Then hit **Compute**.

![](RackMultipart20230102-1-ssjimi_html_c0ac8444e0b9638d.png)

- By default, your tree will be midpoint rooted. We will look more at rooting in the next prac, but for now you want to outgroup root your tree on the Burmese python, which should be basal with respect to the other snakes:

![](RackMultipart20230102-1-ssjimi_html_dd8fd92251114e46.png)

**NOTE:** The precise numbers on your tree may differ. This is because there are random elements to both the likelihood inference method that sets the branch lengths and the bootstrapping of branch confidence.

- Export this tree to a Newick format file. (**File » Export Current Tree (Newick)** then **Export** then **File » Save**. Give your file a **\*.nwk** extension when you save it.

### 13.1.2.Performing Tajima's Relative Rate Test

**You have been assigned three species on Teams** to use for a Tajima's Relative Rate Test.

- Use the tree from section 13.1.1 to identify which of your three species is the outgroup. For example, if given the Burmese python, mainland tiger snake and eastern brown snake, the python would be the outgroup.

- In MEGA, under the **Clocks** menu, use the **Tajima's Relative Rate Test** option to test whether the molecular clock applies to your species. Remember to select the appropriate outgroup.

Table 3. Tajima's Relative Rate Test.

| **Species A** | **Species B** | **Outgroup** | **_P-_value** | **Sig. Faster** |
| --- | --- | --- | --- | --- |
| Mainland tiger snake | Eastern brown snake | Burmese python | 0.366 | n/a |
|
 |
 |
 |
 |
 |

**TASK.** Record your results in Table 3 and post it in the Google Doc for the class. Give the P value (reported in the legend) to 3 d.p. If the result is significant at P \< 0.05 then also record which species is evolving faster.Is there any evidence for deviations from uniform rates between your two species?

Looking at the results for the whole class, do you think any species or lineages are deviating from the molecular clock?

## 13.2.Testing the molecular clock using the Maximum Likelihood method

T ![](RackMultipart20230102-1-ssjimi_html_a9c01d8c7f2e573e.png) ajima's Relative Rate Test is a nice introduction to testing for the molecular clock because it is quite easy to understand, and even calculate by hand if required. However, it makes some simplifying assumptions about patterns of substitution, namely that all substitutions are equal, and that "multiple hits" (two substitutions at the same site) do not happen. As we have seen, biases in nucleotide composition, mutation frequencies and differences in rates of evolution between sites, mean that more sophisticated models of evolution are required to best capture evolutionary distance. MEGA has another molecular clock test that makes use of these evolutionary models.

- Select **Clocks » Test Molecular Clock (ML).** For the evolutionary model and rates among sites,select **HKY+G**. For the **Tree to Use** , select the Newick file you saved in 13.1.1.
- The first time you try this, you will be asked to choose an outgroup. Put the Burmese python into the **Taxa in Outgroup** box and click **Save**.

**Q.** Is the null hypothesis of equal evolutionary rates throughout the tree rejected at P \< 0.05?

- Now repeat the test, but this time select **Use Topology Editor** for the tree and then select **Random Tree From Active Data**. Accept the tree generated.

**Q.** Is the null hypothesis of equal evolutionary rates throughout the tree rejected at P \< 0.05 now? Why do you think this is? What does this tell you about the importance of getting the phylogeny right?

## 13.3.Testing for selection using dN/dS

Although a neutrally evolving sequence should follow the molecular clock, it does not follow that a sequence with clock-like evolution is evolving neutrally. If the functional constraint on the sequence is constant throughout the tree, we would still expect evolution to be clock-like. It is therefore of interest to directly test for selection.

When examining nucleotide sequence evolution in protein-coding genes, we can distinguish between substitutions that change the amino acid sequence in the protein (non-synonymous substitutions) and those that do not change the amino acid sequence in the protein (synonymous substitutions). By considering the genetic code – that is, the translation table – and applying appropriate normalisations, the evolutionary distance can be estimated for each type of change: let _dN_ be the nonsynonymous distance and _dS_ be the synonymous distance between two sequences.

Because synonymous changes do not change the protein product, they are usually selectively neutral (or nearly neutral since codon usage is under weak selection). Therefore, by comparing _dN_ and _dS_ for the same coding sequence we can evaluate whether that sequence is under selection. The ratio _dN_/_dS_ is computed for this purpose. If this ratio is near 1, there is no evidence for selection. If the ratio is under 1, nonsynonymous substitutions are relatively rare, and this is a sign of purifying selection. If the ratio is over 1, nonsynonymous substitutions are relatively abundant, and this is a sign that positive selection has driven these changes.

**TASK.** Based on your results from 11.3.4, do you predict dN/dS to be greater than, less than, or approx. equal to 1? Explain your answer.

To evaluate these hypotheses statistically we test whether the difference _dN_ - _dS_ is significantly different from zero. To do this, we must have the variance of estimators of this difference under some model.

- Back in the main MEGA window, test the hypothesis that _dN_ - _dS_ = 0 using the **Nei-Gojobori method (Proportion)** using **Selection** » **Codon-based Z-test of Selection**.

![](RackMultipart20230102-1-ssjimi_html_d9c4697fc9c4f7be.png)

**TASK.** Describe and interpret your results.

From these data, what kind of selection (if any) do you think MC1R is experiencing? Compare and contrast with your analysis in section 11.3.4.

Do any pairs of sequences go against the general trend? What might be the explanation for this observation?

![](RackMultipart20230102-1-ssjimi_html_a48a2329a794d885.gif)

For this exercise, you will use a multiple sequence alignments generated by GOPHER in **Section 8**. Hopefully, you are familiar with the basics of rooting a phylogenetic tree from Year 2. If not, refresh your memory by reading the PDF provided on MS Teams:

- **Edwards RJ****  (2019):** [Phylogenetic Tree Rooting](https://www.sciencedirect.com/science/article/pii/B9780128096338202586), In _Encyclopedia of Bioinformatics and Computational Biology_, **Elsevier** Volume 2, Pages 727-735.

This primer also gives an introduction to some other key phylogenetic concepts, including topology, branch lengths and recognising molecular clocks.

# 14.Basic phylogenetic analysis with MEGA

We are now going to switch attention to phylogenetic analysis using protein sequences. Whilst nucleotide sequences are very good for analysis of molecular evolution over relatively short timescales (in evolutionary terms), protein sequences are often more useful for the annotation and analysis of protein-coding genes.

**Q.** Can you think of any reasons why protein sequences might be better than nucleotide sequences for phylogenetics over longer timescales?

## 14.1.Getting data into MEGA

If you are running MEGA locally, the easiest way to get data into it is to simply open the program and drag either a \*.fas or \*.nwk tree file onto the main window. Alternatively, you can open a protein alignment file as described above for the MC1R data. Note that you can also make a tree using an external tool (_e.g._ HAQESAC) and open it in MEGA, using **User Tree » Diplay Newick Trees**.

![](RackMultipart20230102-1-ssjimi_html_6eadb20e63ac5d1.png)

This will open up the **Tree Explorer** (see 14.3Visualising and manipulating phylogenies). For more information on Newick Format, see here: [http://evolution.genetics.washington.edu/phylip/newicktree.html](http://evolution.genetics.washington.edu/phylip/newicktree.html).

- Open the provided NSCUK81EOG090701X7.orthaln.fas alignmentfile to **Analyze**. (Remember to tell MEGA these are **Protein sequences**!)

If you click on the **TA** button it will open the alignment for viewing and calculating some evolutionary statistics as before. This is most useful for exploring DNA evolution – **AliView** is better for general alignment viewing and manipulation.

**Q.** How many positions are there in the alignment?

**Q.** How many invariant sites are there in the alignment?

## 14.2.Making a phylogenetic tree with MEGA

### 14.2.1.Constructing phylogenies

- Close your data (if open) and click on the **Phylogeny** menu item. This will give a choice of several tree types:

![](RackMultipart20230102-1-ssjimi_html_c507336e2fd2d577.png)

Explore these at your leisure but make sure that you construct at least one of each type of tree from the same alignment data to compare. Think about the different core principles of these methods from your lectures and see if you can infer anything about your data from any (lack of) differences between methods. For now, we will just construct a Neighbour-Joining tree.

- C ![](RackMultipart20230102-1-ssjimi_html_37d6907020c49bf4.png) lick **Neighbor-Joining**. It will ask if you want to use the currently active data, which is the alignment that you have loaded. You do.
- This will open up an **Analysis Preferences** dialogue box. Options are highlighted in yellow and vary from method to method. Feel free to explore these (or not) but there are a couple that you should definitely always consider. (Later, you might want to test the data for the best evolutionary model – this will take a while, so stick with a **Poisson model** and **Gamma Distributed (G) Rates** for now.)

1. **Bootstrapping**. _Always_ use some kind of "Test of Phylogeny". For now, use the **Bootstrap method** , which we looked at in the lecture. The default is 500 replicates for some reason. Use 100 when exploring trees and 1000 when making a "final" tree for your report. (If it is fast, you might want to use 1000 all the time.)
2. **Gaps/Missing Data Treatment**. This is an important one and you might want to make trees with different methods. It determines how gaps in your alignment are treated:
  1. **Complete deletion** will remove _all_ columns with gaps. This uses the best-quality data but can also chuck out a lot of data if you have lots of indels. Be particularly wary of this if you have one or more truncated sequences: any column with a gap in _any_ sequence will be chucked out.
  2. **Pairwise deletion** will only ignore gaps when comparing a given pair of sequences. This is less susceptible to rogue sequences messing things up but can introduce biases if a set of sequences have the same regions extra/missing.
  3. **Partial deletion** is a less severe version of complete deletion. You can set what percentage of your sequences should have (non-gap) data to be used.

- After choosing your options, press **Compute** to construct the tree.

### 14.2.2.Testing for biased multiple sequence alignment data

It is often a good idea to compare trees with complete and pairwise deletion methods to see what influence the option has. If your trees look basically the same, there is probably not any great indel-induced bias to worry about. If they look different, look at your alignment and consider the methods carefully to choose which you should use. It could be that a subset of sequences share a feature in the multiple sequence alignment, for example, which is missing from some other sequences due to incomplete data. This could be a greater problem if that feature is under different functional constraint – and therefore evolutionary rate – versus the rest of the alignment. On the other hand, discarding gapped columns might leave you with too little data. (You might be better off discarding one or two problematic sequences and regenerating the alignment.)

Make sure that you document what you do clearly in your lab book and include justification for your choices when you write up your results.

## 14.3.Visualising and manipulating phylogenies

Once you have computed your tree – or if you open a Newick file in MEGA – it will open in a **Tree Explorer** window. Refer to your phylogenetics lectures and assess your tree for topology, branch lengths, rooting and molecular clock assumptions.

We will concentrate on making your trees look nice in the next section. For now, concentrate on manipulating them to help you (a) understand the phylogeny you have produced, and (b) compare and contrast between methods.

- Save the tree. It will save as a MEGA tree session (\*.mts). By saving before manipulating/editing the tree, you can always go back.
- Explore the buttons down the left-hand side of the Tree Explorer window and make sure that you know what they all do.
- Explore the **View** menu commands to see how you can alter the visualisation. Save different views as different \*.mts files if you think they are useful.

![](RackMultipart20230102-1-ssjimi_html_64220a40343d4066.png)

### 14.3.1.Comparing and contrasting trees

MEGA allows you to have several trees open at once.

- Generate **Maximum Likelihood (ML)**, **UPGMA** and **Maximum Parsimony (MP)** trees. In the interests of time, do not bootstrap your ML tree. (You may want to try this later.)

**Q.** Use the Tree Explorer options to manipulate and rotate branches to compare and contrast these trees. Where are they similar? Where are they different? How do these relate to (in)consistent branch lengths and/or bootstrap support? Which relationships within your tree are robust?

**Q.** Remember that UPGMA assumes (_i.e._ enforces) a molecular clock. By comparing a UPGMA tree to NJ, what can you say about your sequences and whether they appear to be evolving in a clock-like fashion?

### 14.3.2.The impact of multiple sequence alignment on phylogenetics

A phylogenetic tree can only be as good as the data used to generate it. Where different phylogenetic methods disagree, it is good to ask whether there is anything about your sequence alignment data/quality that might account for apparent errors/discrepancies. Here, we are using a multiple sequence alignment generated with the tool Clustal Omega. The same sequences have also been aligned with MUSCLE. Two neighbour-joining trees, generated from these alignments, have been provided on Moodle:

- NSCUK81EOG090701X7.orth.clustalo.nwk
- NSCUK81EOG090701X7.orth.muscle.nwk

- Open the two trees in MEGA and see if you can use branch rotation to make them match.

**Q.** Do the two trees have the same topology?

**Q.** If your choice of MSA affects the placement of a branch, what does that tell you about (a) that branch of the phylogeny, and (b) the importance of the alignment algorithm?

### 14.3.3.Midpoint rooting and outgroup rooting

Most of the proteins in your GOPHER alignment and tree are from Metazoan species. The two exceptions are:

- _Monosiga brevicollis_ (MONBE) = Choanoflagellate
- _Oryza sativa_ _japonica_ (ORYSJ) = Rice.

Choanoflagellates are thought to be the sister group of Metazoa and therefore the outgroup for trees generated from this alignment should be rice, as the only plant.

- Open up your three trees from **section 14.3.1**  and select  **View » Root on midpoint.**

**Q. ** Do your midpoint rooted trees correctly place rice (ORYSJ) as the outgroup?

ML –

UPGMA –

MP –

- Now trying manually rooting the trees using rice as an outgroup. (The root button is the icon on the left with the green triangle. Click this, then choose the point on the tree to place the root.)

**Q.**  When you use rice (ORYSJ) as the outgroup, is the Choanoflagellate (MONBE) correctly placed outside the Metazoan clade?

ML –

UPGMA –

MP –

**Q.**  Why does the UPGMA tree not give you the option to move the root?

# 15.Making a good phylogenetic tree figure with MEGA

You should have made sure that you can make a variety of different phylogenetic trees with MEGA. This section will concentrate on generating publication-quality images using MEGA. Note that MEGA has many options. Here, we will only explore a handful that are (a) useful and (b) easily overlooked. These are neither the start nor end of the things that you might want to do to/with your trees.

## 15.1.General tips

There are a few helpful hints, most of which apply to all figures:

1. Make it large and bold enough. Use the **Options** panel and relevant buttons/options in the **Tree Explorer** window to make a tree that is the correct size and dimensions for your report. Clearly this will be influenced by the nature of the tree but also think about the layout in your report. A smallish tree with short labels might look best at half page width as part of a multipanel figure. If you have many sequences (and/or many short internal branches), you will probably want your figure to be full page width. Similarly, long sequence names or additional annotation might need a wider figure. Golden Rule: always print out your figure and see what it looks like. If lines are too thin, make them wider. (Use line size 2+ for the tree itself.) If colours are unclear, change them. If fonts are too small to read, make them bigger!

![](RackMultipart20230102-1-ssjimi_html_7ffd9303058abc8c.png)

1. M ![](RackMultipart20230102-1-ssjimi_html_6c72bb6e5151a9b9.png) ake clear labels. Font size and type is important but also placement and colour. Be efficient (but clear) by encoding information visually with symbols, colour and/or abbreviations where appropriate. **Remember that you can (and usually should) edit the sequence names.** Avoid extraneous/unclear detail in the figure itself: accession numbers might be better provided in the legend or even an additional table, for example; it would usually be better to use gene symbols and species (or species codes) in the tree itself. If text/lines are too thing to distinguish colours, make the colours more distinctive and/or the text/lines bolder. _If possible_, make sure that the figure is understandable if printed in black and white.
2. Make a clear legend. The **Caption** menu command can help with this. Make sure that any symbols etc. are clearly described.

## 15.2.Subtrees

One of the most powerful features of MEGA is the use of the **Compress/Expand** button to generate subtrees. You can add a **Name/Caption** that will be displayed next to the collapsed branch.

![](RackMultipart20230102-1-ssjimi_html_149c84c3fd885f36.png)

### 15.2.1.Formatting subtrees

O ![](RackMultipart20230102-1-ssjimi_html_796f3dfccb1749ad.png) nce made, subtrees can also be accessed and edited via the **S**** ubtree » Draw Options** menu item.

Beyond compresses and labelling a clade, these options can also be used for formatting the branches and taxon names, and adding a bracketing label when not compressed.

![](RackMultipart20230102-1-ssjimi_html_ad5c81779a75f797.png)

### 15.2.2.Nesting subtrees

Subtrees can be nested to identify/highlight specific subclades. For example, the snakes and mammals subclades of the vertebrates:

![](RackMultipart20230102-1-ssjimi_html_55b3d05ae83cf4eb.png)

**Q.** Why do you think _Branchiostoma floridae_ has been highlighted in red in this tree?

**Q.** What do the bootstrap values tell you about the confidence of the placement of this sequence?

## 15.3.Citing MEGA and its methods

Make sure that you appropriately cite any methods or tools you use in your report. MEGA has a **Citing MEGA in Publications** section in its **Help** , which contains its full citation. Some of the methods within MEGA have their own additional publications that should also be cited when used. The **Caption** command can be very helpful for this.

# 16.Protein Family Analysis

## 16.1.HAQESAC – Generating alignments and trees of protein families

Up to this point, we have been interested in a single protein and its homologues. However, as covered in the lectures, proteins are often members of protein families, created by gene duplications. In this activity, we will look at how phylogenetics and protein family analysis can aid the annotation of proteins and the identification of orthologues from other species.

For this, we will be using output from another SLiMSuite program, called **HAQESAC (Homologue Alignment Quality, Establishment of Subfamilies and Ancestor Construction)**. HAQESAC is a tool designed for processing a dataset of potential homologues (such as that made in  **Section 5** ) and generating a trustworthy global alignment and well bootstrap-supported phylogeny. By default, an initial dataset consisting of homologues (detected by BLAST, for example) is processed into a dataset consisting of the query protein and its orthologues in other species plus paralogous subfamilies in the same gene family.

Individual sequences are therefore screened to fulfil two criteria:

1. They must be homologous to (and alignable with) the query sequence of interest.
2. They must be a member of a subfamily within the gene family to which the query sequence belongs.

Details of HAQESAC - and instructions for generating the data we will use below - can be found in optional  **Section** 17 **– HAQESAC (Advanced)**. You might want to pause at this point and attempt **Section** 17 before returning. HAQESAC runs in three main stages:

1. **HAQ.**  The first stage of data cleanup is therefore to remove rogue sequences that either do not fit in the gene family at all or are too distantly related to the query protein for a decent alignment that can be used for useful further analysis. This is achieved firstly by a simple identity cut-off, determined by pairwise alignments of sequences, and then by a more complex procedure of removing sequences for whom the overall alignability is poor. During this procedure, sequences that have too many gaps are also removed as too many gapped residues can cause problems for downstream evolutionary analyses. Further screening is achieved based on phylogenetic information.
2. **ES. ** Once the dataset has been 'cleaned up' (and, indeed, during processing), HAQESAC can be used to assign sequences to subgroups or subfamilies, if such information is needed for downstream analyses.
3. **AC.**  The final step that HAQESAC is able to perform is ancestral sequence prediction using the GASP (Gapped Ancestral Sequence Prediction) algorithm. We do not use this in these pracs.

This can be considered an extension of the GOPHER approach taken in **Section 8** , which tries to identify and return orthologues. HAQESAC is designed to work with protein families, establishing both orthology and paralogy.

## 16.2.Visualising and improving the HAQESAC tree

HAQESAC has been run on the putative TLR4 BUSCO protein that we used previously. Details are in  **Section** 17 **,**  but a summary of the commands is as follows:

$ cat /share/data/babsgenome/prac/NSCUK81EOG090701X7.fas /share/data/babsgenome/prac/tlr4\_hits.full1000.fas \> NSCUK81TLR4.fas
$ cp /share/data/babsgenome/prac/tlr4.spec .
$ module add blast+/2.6.0 clustalw/2.1 clustalo/1.2.4 R/3.4.0
$ python /share/apps/slimsuite/tools/haqesac.py -seqin NSCUK81TLR4.fas -query NSCUK81EOG090701X7 -goodspec tlr4.spec -badspec CHICK -basefile NSCUK81TLR4.haqesac

» This generates a number of NSCUK81TLR4.haqesac.\* files. Create a new  **analysis/**  directory and copy in the data generated by a HAQESAC run:

$ cp /share/data/babsgenome/examples/HAQESAC-Auto/\* .

The most important files for this analysis are:

- NSCUK81TLR4.haqesac.fas is the multiple sequence alignment.
- NSCUK81TLR4.haqesac.nwk is the phylogenetic tree, which can be viewed in MEGA. The same tree is also available as a plain text rendering (NSCUK81TLR4.haqesac.tree.txt) and (hopefully!) a PNG for a convenient quick look (NSCUK81TLR4.haqesac.png).

Open up the  **\*.nwk Newick tree file**  in MEGA and have a look at it. Then load the multiple sequence alignment produced from HAQESAC and repeat the process of using MEGA to make some more trees and explore possible errors and biases in the data. You will notice that we now have multiple different sequences from some species that are found in different parts of the tree and have distinct protein descriptions.

Use the tips in  **Section 15**  about tree visualisation and try to mark some appropriate subtrees. Also mark your query sequence with an identifying symbol.

**Question:**  From your tree, how confident are you that our snake BUSCO protein is indeed TLR4? Are you more or less confident of this having seen the tree versus just looking at the results of the BLAST searches and alignments?

**Question:**  What other sequences would be useful to get a fuller picture of the identity of our query protein and its place in the gene family?

**NOTE:**  During the original BLAST and subsequent HAQESAC cleanup, decisions were made that limited the number of sequences that would end up as part of this analysis. You therefore cannot necessarily have confidence that the tree produced by HAQESAC will have all of the relevant members of the protein family in it. For gene annotation, the important question is whether it has _enough_ for a confident identification of the query. For more complex questions about the evolution of the protein family, more careful data generation is required.

**NOTE:**  Make sure you have worked through the phylogenetics lectures (Topic 3) before attempting this assignment. If you are struggling with this assignment, you might want to revisit the earlier pracs to remember how the data being analysed was created.

**TASK. Comparing phylogenetic methods**.

Using the BUSCO protein multiple sequence alignment (NSCUK81EOG090701X7.orthaln.fas) provided on Moodle, make four phylogenetic trees, each with 1000 bootstraps:

1. UPGMA
2. Mid-point rooted Neighbour-joining
3. Neighbour-joining, rooted using rice as an outgroup
4. Maximum parsimony, rooted using rice as an outgroup

Save each tree as a PNG and create an A4 Portrait page below that consists of:

1. A four-panel figure with the trees labelled A-D.
2. A legend describing the methods used to make the four trees. Unlike a lab book entry, this should not include file paths and names etc.

You may choose what to use for other settings (e.g. gap deletion) but be consistent and make sure it is clear in the legend what was done.

**The figure and legend should fit on a single page. Margins should be at least 2cm. The legend should be Arial or Times New Roman, size 10+.** (You may need to modify the View » Options to make trees that fit on the page well and still look good.) **NOTE:** You do not need to include references/citations in the legend.

Then, answer the questions below. Half the marks are for clear trees. Half the marks are for clear answers. Bonus credit is available for good use of colour/symbols etc. in your trees that make the answers to the questions clearer.

**QUESTION 1:** Does a comparison with of your UPGMA and midpoint-rooted NJ trees support a molecular clock for this protein? (Are the topologies essentially the same, with the same rooting?)

**QUESTION 2:** Does comparison of your mid-point rooted and outgroup-rooted NJ trees support a molecular clock for this protein? (Is the midpoint rooting in the correct place?)

**QUESTION 3:** Do your four trees (a) correctly place the six snake species as a monophyletic group, and (b) agree on the topology of the snake clade?

**TASK 2.2. Protein family analysis.**

Create a Maximum Likelihood tree with 100 bootstrap replicates using the TLR family multiple sequence alignment provided on Teams, NSCUK81TLR4.haqesac.fas. ( **NOTE:** This may take a while to generate, which is why we are limiting to 100 bootstrap replicates.) Use the visualisation options of MEGA to create two representations of this tree:

1. The full tree, mid-pointed rooted and with different subfamilies clearly marked. Mark the tiger snake TLR4 query sequence with a symbol.
2. The same tree, outgroup rooted using the CD180 subfamily as an outgroup. (NB. This may not be biologically accurate.) Collapse each subfamily and mark the TLR4 subfamily with a symbol.

Export each tree to an image and paste below as "Tree A" and "Tree B". Create a figure legend entry below as if this were a single two-panel figure labelled A and B, with the details of the method used to create the tree and descriptions of any formatting that helps interpretation. Bonus marks will be given for good use of colour and labels etc. that help identify the different TLR subfamilies and query sequence/subfamily.

**NOTE:** Because this alignment and tree was generated in a very query-centric fashion, it may not give a complete, balanced and accurate picture of the TLR family. Marks in this assignment are being awarded for clear presentation of data (including a clear, concise and complete legend), rather than interpretation.

**NOTE:** You do not need to include references/citations in the legend.

---

**Tree A.**

**Tree B.**

**Figure Legend.**

## 16.3.Orthology and Protein Family Analysis

Revisit your GOPHER trees from the end of  **Section 8**. Open one of these and compare it to the HAQESAC protein family. Pay special attention to two species: XENTR (_Xenopus tropicalis_) and XENLA (_Xenopus laevis_). These are closely related taxa and should fall together in a tree. In this case, our GOPHER tree includes XENTR (a Quest For Orthologues species), whilst XENLA (a model organism) was included in the species chosen for the HAQESAC tree.

**Question: ** Does the placement of the XENTR "orthologue" found by GOPHER appear to be consistent with the HAQESAC XENLA sequences? Which do you trust, and why? What does this tell you about the importance of phylogenetic analysis for selecting orthologues?

# 17.HAQESAC (Advanced)

Optional **Section 10**  demonstrated a number of different approaches to filtering BLAST hits prior to multiple sequence alignment. Each of the methods has its strengths and weaknesses and so it is often necessary to play around with a few different approaches, visualising the alignments produced as you go, to try and optimise your data quality. This is fine for very careful analysis of single proteins when you have a lot of time, but it can be very limiting for studying multiple proteins. (You will only need to write about one protein, but you will probably want to explore a few before settling on one.)

**HAQESAC (Homologue Alignment Quality, Establishment of Subfamilies and Ancestor Construction)** is a tool that tries to combine these different approaches with some additional tools for generating and cleaning up a multiple sequence alignment and phylogenetic tree. This can be considered an extension of the GOPHER approach taken in  **Section 8** , as HAQESAC is designed to work with protein families, establishing both  **orthology and paralogy**. HAQESAC output is used in  **Section 16**. This Activity will work through a few of the functions of HAQESAC, including the generation of the data used in  **Section 16**. Working through the whole Activity will take quite a while, but this tool could prove very useful to you for Part II of the prac, enabling you to quickly analyse several proteins before selecting your favourite to focus on.

The manual is available (if a bit out of date) here if you want to know more: [https://github.com/slimsuite/SLiMSuite/blob/master/docs/manuals/HAQESAC%20Manual.pdf](https://github.com/slimsuite/SLiMSuite/blob/master/docs/manuals/HAQESAC%20Manual.pdf).

**NOTE: ** The activities below use 2017 dates - you should use today's date when trying these activities.

## 17.1.Advanced filtering with HAQESAC

**NOTE: This activity follows from Section 10 Filtering sequences (Advanced) and refers to files used in that Section. If you want to run on your own data, paths to files should be updated to use your own relevant file paths. Note that some of the data may have changed since this tutorial was made, and therefore some of the details of the HAQESAC output will also be expected to change.**

Make and enter a new analysis directory (e.g.  **2017-09-11.HAQESAC/** ) and create a new fasta file consisting of  **the renamed BUSCO sequence and its full set of BLAST hits**  from  **Section 5** :

$ cat /share/data/babsgenome/prac/NSCUK81EOG090701X7.fas /share/data/babsgenome/prac/tlr4\_hits.full1000.fas \> NSCUK81TLR4.fas

We'll also make a new species list file based on the one used with the species filter above and add a couple more species of model organisms (mouse, rat and Xenopus):

$ cp /share/data/babsgenome/prac/wanted.spec tlr4.spec
$ echo MOUSE \>\> tlr4.spec
$ echo RAT \>\> tlr4.spec
$ echo XENLA \>\> tlr4.spec

It is also important to make sure that we include Tiger snake in this list, as we want to make sure that we keep our query BUSCO sequence:

$ echo NOTSC \>\> tlr4.spec

**NB. ** If you struggle with the echo commands, you can just copy /share/data/babsgenome/prac/tlr4.spec.

HAQESAC can perform some of the previous filtering options [default values in square brackets]:

- E-value filtering: **blaste=X [1e-4]**
- Species filtering:  **goodspec=LIST**  (or  **goodspec=FILE** ); can also negatively filter with  **badspec**. [None by default]
- %identity filtering: **qryid=X [40.0]**

Instead of GOPHER top hits or %identity NR filtering, HAQESAC features a phylogenetic-based subfamily assignment of the proteins, from which sequence variants are reduced to a single sequence per species (by default). It also has an additional top hits filter for the post-species/NR filtered sequences:

- **blastcut=X**  [None by default]

HAQESAC also needs a specific query to act as the focus for the alignment ( **query=X** ). HAQESAC will try to optimise alignment to this sequence. This is our renamed BUSCO sequence:  **query=NSCUK81EOG090701X7**.

## 17.2.Running HAQESAC

HAQESAC makes use of BLAST+, ClustalW2, Clustal Omega (by default) and R, so we need to add these modules before running. We will give our updated species file as the "good species". From the previous analysis, it was also clear that there were a lot of chicken sequences (95 out of 1000!) so we will exclude chicken from the analysis this time to speed things up a bit. This is done with  **badspec=CHICK**.

$ module add blast+/2.6.0 clustalw/2.1 clustalo/1.2.4 R/3.4.0
$ python /share/apps/slimsuite/tools/haqesac.py -seqin NSCUK81TLR4.fas -query NSCUK81EOG090701X7 -goodspec tlr4.spec -badspec CHICK -basefile NSCUK81TLR4.task11

This will take a while (~15+ mins) to run.

**SLiMSuite commandline arguments: -arg val versus arg=val**
 You might have noticed that I often refer to arguments in the text as  **query=X**  but then run them in the command as  **-query X**. SLiMSuite can use both notations interchangeably and it is simply a matter of convenience which to use.  **arg=value**  is often more clear to read bu  **-arg value**  is particularly useful when the argument takes a filename as you can you the  **TAB**  autocomplete functionality of UNIX to make typos less likely.

While HAQESAC is running, you can watch its progress in the terminal window. This can get a bit boring, though, so you might want to work on something else in the background. If running this during the prac session, be aware that the server might get quite slow if lots of people are using it!

## 17.3.HAQESAC alignments and trees

### 17.3.1.HAQESAC output

HAQESAC produces quite a few output files (including some in a HAQESAC/ subdirectory), named according to basefile:

-rw-r--r--. 1 z3452659 unsw 834K Jun 20 11:29 NSCUK81TLR4.fas
-rw-r--r--. 1 z3452659 unsw  128 Jun 20 11:29 tlr4.spec
-rw-r--r--. 1 z3452659 unsw 179K Jun 20 11:51 NSCUK81TLR4.haqesac.pickle.gz
-rw-r--r--. 1 z3452659 unsw 1.4K Jun 20 11:53 NSCUK81TLR4.haqesac.grp
-rw-r--r--. 1 z3452659 unsw  80K Jun 20 11:53 NSCUK81TLR4.haqesac.fas
-rw-r--r--. 1 z3452659 unsw 6.1K Jun 20 11:53 NSCUK81TLR4.haqesac.nwk
-rw-r--r--. 1 z3452659 unsw  19K Jun 20 11:53 NSCUK81TLR4.haqesac.tree.txt
-rw-r--r--. 1 z3452659 unsw 322K Jun 20 11:53 NSCUK81TLR4.haqesac.png
-rw-r--r--. 1 z3452659 unsw  262 Jun 20 11:53 NSCUK81TLR4.haqesac.aafreq.txt
drwxr-xr-x. 2 z3452659 unsw  214 Jun 20 11:54 HAQESAC
-rw-r--r--. 1 z3452659 unsw 121K Jun 20 11:54 NSCUK81TLR4.haqesac.log

./HAQESAC:
-rw-r--r--. 1 z3452659 unsw 253K Jun 20 11:39 NSCUK81TLR4.haqesac.clean.fas
-rw-r--r--. 1 z3452659 unsw  80K Jun 20 11:52 NSCUK81TLR4.haqesac.haq.fas
-rw-r--r--. 1 z3452659 unsw 1.7K Jun 20 11:53 NSCUK81TLR4.haqesac.phb
-rw-r--r--. 1 z3452659 unsw 156K Jun 20 11:54 NSCUK81TLR4.haqesac.anc.fas
-rw-r--r--. 1 z3452659 unsw 2.7K Jun 20 11:54 NSCUK81TLR4.haqesac.anc.nsf
-rw-r--r--. 1 z3452659 unsw  46K Jun 20 11:54 NSCUK81TLR4.haqesac.anc.txt

This is one reason why it is a good idea to run it in a fresh directory. I have highlighted in yellow the three most important files for now:

- NSCUK81TLR4.haqesac.fas is the multiple sequence alignment.
- NSCUK81TLR4.haqesac.nwk is the phylogenetic tree, which can be viewed in MEGA. The same tree is also available as a plain text rendering (NSCUK81TLR4.haqesac.tree.txt) and (hopefully!) a PNG for a convenient quick look (NSCUK81TLR4.haqesac.png).
- NSCUK81TLR4.haqesac.log is the log file that documents what HAQESAC actually did. (See below.)

### 17.3.2.HAQESAC Run Details

**NOTE: ** The output in this section is from an older run of the program - some details may be slightly different for your run.

So, what is HAQESAC actually doing? If you sat and watched it - or opened up the log file for a look - you will see there is a lot of stuff output. The main steps are as follows:

**1. Program setup**

The log file is created (or appended) and the introductory text generated:

Append file: /home/z3452659/babs3291/analysis/2017-09-11.HAQESAC/NSCUK81TLR4.task11.log

HAQESAC V1.10.2 run: Thu Sep  7 14:30:59 2017

  ######################################################################################################################
  #|#\> HAQESAC version 1.10.2 : Homologue Alignment Quality, Establishment of Subfamilies and Ancestor Construction \<#|#
  #|#\> ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ \<#|#
  #|#\> Copyright (c) 2005 Dr Richard J. Edwards. \<# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ #\> Last Modified: March 2015 \<#|#
  #|#\> ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ \<#|#
  #|#\> Disclaimer: HAQESAC comes with ABSOLUTELY NO WARRANTY;                                                       \<#|#
  #|#\>   This is free software, and you are welcome to redistribute it;                                             \<#|#
  #|#\>   For details see attached license file (gnu\_general\_public\_license.txt)                                     \<#|#
  #|#\>   or http://www.gnu.org/copyleft/gpl.html.                                                                   \<#|#
  #|#\> ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ \<#|#
  #|#\> Cite: Edwards RJ et al. (2007) Nature Chem. Biol. 3(2):108-112.                                              \<#|#
  ######################################################################################################################

Append file: /home/z3452659/babs3291/analysis/2017-09-11.HAQESAC/NSCUK81TLR4.task11.log

#VIO    00:00:00    Verbosity: 1; Interactivity: -1.

Commands give can be found in the log.

**2. Load sequences**

The sequence file is loaded and query established. Sequence names are checked for redundancy:

#SEQ    00:00:02    1,001 sequences loaded from NSCUK81TLR4.fas (Format: fas).
#QRY    00:00:02    Query Sequence = eog\_NOTSC\_\_NSCUK81EOG090701X7 (799 AA).
#DICT    00:00:02    Made "short" seqName dictionary: 1,001 seq; 1,001 keys.
#DICT    00:00:02    Made "AccNum" seqName dictionary: 1,001 seq; 1,001 keys.
#NR    00:00:02    No duplicate AccNum detected.

**NOTE:** If running HAQESAC yourself, make sure if it is recognising the correct query sequence.

**3. Species filtering**

Input sequences are species using our species criteria:

#REM    00:00:02    Deleted tr\_PATFA\_\_A0A1V4J6V9: Not found in Good-Spec filter.
#REM    00:00:02    Deleted tr\_9GRUI\_\_A0A091LR14: Not found in Good-Spec filter.
#REM    00:00:02    Deleted tr\_FICAL\_\_U3JZ62: Not found in Good-Spec filter.
#REM    00:00:02    Deleted tr\_PHORB\_\_A0A091UF21: Not found in Good-Spec filter.
...
#REM    00:00:02    Deleted tr\_CHICK\_\_A0A1L4FMC8: Excluded by BadSpec filter.
#REM    00:00:02    Deleted tr\_CHICK\_\_C4PCJ0: Excluded by BadSpec filter.
...
#REM    00:00:02    Deleted tr\_ACRSC\_\_A0A0A7MAU6: Not found in Good-Spec filter.
#REM    00:00:02    Deleted tr\_ACRSC\_\_A0A0A7MFD4: Not found in Good-Spec filter.

**4. Additional sequence clean up based on BLAST hits and similarity to other sequences.**

This runs a BLAST search, optionally keeps the top X sequences (blastcut=X) and checks similarity versus the query. A multiple sequence alignment is then performed and a second check compares each sequence to its nearest neighbour, deleting it if the sequence is too gappy (i.e. has too much sequence missing.)

#INF    00:00:02    Cleaning up data for NSCUK81TLR4.task11.fas (173 Sequences).
#FAS    00:00:02    173 Sequences output to NSCUK81TLR4.task11.fas.
#FAS    00:00:02    1 Sequences output to NSCUK81EOG090701X7.qry.
#NCBI    00:00:03    Installation of BLAST+ detected. Path not required.
#DB     00:00:03    makeblastdb -in "NSCUK81TLR4.task11.fas" -out "NSCUK81TLR4.task11.fas" -title "/home/z3452659/babs3291/analysis/2017-09-11.HAQESAC/NSCUK81TLR4.task11.fas" -parse\_seqids -dbtype prot
#SYS    00:00:03    blastp -query NSCUK81EOG090701X7.qry -db NSCUK81TLR4.task11.fas -out NSCUK81EOG090701X7.blast -seg no -comp\_based\_stats F -soft\_masking true -evalue 1.000000e-04 -num\_descriptions 173 -num\_alignments 173
#BLAST    00:00:04    Reading NSCUK81EOG090701X7.blast blastp BLAST results complete: 1 searches; 173 hits (vs 173 Seq; 137,633 letters)
#BLAST    00:00:04    Deleted BLAST results file: NSCUK81EOG090701X7.blast
#REM    00:00:04    Deleted tr\_OPHHA\_\_V8P6W7: Ordered BLAST Local hits \< 40.0% similarity vs Query.
#SEQ    00:00:04    GABLAMO Filter vs eog\_NOTSC\_\_NSCUK81EOG090701X7: 172 sequences remain.
#FAS    00:00:04    172 Sequences output to NSCUK81TLR4.task11.fas.
#FAS    00:00:04    172 Sequences output to NSCUK81TLR4.task11.fas.
#ALN    00:00:04    Clustal Omega alignment: clustalo -i NSCUK81TLR4.task11.fas -o NSCUK81TLR4.task11.aln --outfmt=clu
#SEQ    00:00:27    172 sequences loaded from NSCUK81TLR4.task11.aln (Format: aln).
#QRY    00:00:27    Query Sequence = eog\_NOTSC\_\_NSCUK81EOG090701X7 (799 AA).
#MAP    00:00:27    Aligned sequences successfully mapped onto originals
Removing gappy (\> 50.0%) sequences relative to neighbour...
#REM    00:00:34    Deleted tr\_MEGAM\_\_A0A1B0RYQ5: Too many gaps (\> 50.0%) relative to neighbour (tr\_STRCA\_\_A0A093HTW8)! (54%).
#REM    00:00:35    Deleted tr\_PIG\_\_K7GLZ3: Too many gaps (\> 50.0%) relative to neighbour (tr\_STRCA\_\_A0A093HTW8)! (71%).
#REM    00:00:35    Deleted tr\_PIG\_\_Q70EK4: Too many gaps (\> 50.0%) relative to neighbour (tr\_STRCA\_\_A0A093HTW8)! (68%).
Gappy Sequence removal complete! 169 sequences remain.
#DEGAP    00:00:35    8 gapped columns removed.
...
#SEQ    00:01:06    %ID/Gap Filter: 172 -\> 169 sequences.
#INF    00:01:06    Cleanup of NSCUK81TLR4.task11.fas complete: 169 of 173 Sequences remain.
#FAS    00:01:06    169 Sequences output to NSCUK81TLR4.task11.fas.
#FAS    00:01:06    169 Sequences output to NSCUK81TLR4.task11.clean.fas.

**5. Single sequence alignment quality**

HAQESAC then re-aligns the sequences and iteractively throws out sequences that align badly compared to their near neighbours (see manual for details):

#INF    00:01:06    Single Sequence Alignment Quality (SAQ) 1 for NSCUK81TLR4.task11.fas (169 Seqs).
#SAQ    00:02:02    SAQ1-1: Calculating "bad" residues ... 100.0% =\> 1,089 bad of 135,551 total residues
#SAQ    00:02:54    SAQ1-2: Calculating "bad" residues ... 100.0% =\> 1,125 bad of 135,551 total residues
#SAQ    00:03:45    SAQ1-3: Calculating "bad" residues ... 100.0% =\> 1,130 bad of 135,551 total residues
#SAQ    00:04:36    SAQ1-4: Calculating "bad" residues ... 100.0% =\> 1,130 bad of 135,551 total residues
#SAQ    00:04:36    SAQ1-4: Removing bad sequences and/or dodgy regions... Query (eog\_NOTSC\_\_NSCUK81EOG090701X7) processed...
tr\_CHEMY\_\_M7C4S8 worst: -3,077 aa if kept vs -840 aa if lost.
#REM    00:04:36    Deleted tr\_CHEMY\_\_M7C4S8: SAQ1: -3,077 aa if kept vs -840 aa if lost.
tr\_ASTMX\_\_W5K2F4 worst: -2,310 aa if kept vs -841 aa if lost.
tr\_XENLA\_\_A0A1L8FN49 worst: -889 aa if kept vs -861 aa if lost.
...
tr\_STRCA\_\_A0A093HTW8 worst: -87 aa if kept vs -690 aa if lost.
tr\_XENLA\_\_A0A1L8FNK9 worst: -16 aa if kept vs -800 aa if lost.
#HAQ    00:04:38    SAQ1: 169 -\> 168 sequences.
#FAS    00:04:38    168 Sequences output to NSCUK81TLR4.task11.fas.
#ALN    00:04:38    Clustal Omega alignment: clustalo -i NSCUK81TLR4.task11.fas -o NSCUK81TLR4.task11.aln --outfmt=clu
...
#HAQ    00:07:54    SAQ2: 168 -\> 167 sequences.
...
#HAQ    00:10:49    SAQ3: 167 -\> 167 sequences.
#FAS    00:10:50    167 Sequences output to NSCUK81TLR4.task11.haq.fas.

Finished Single Sequence Alignment Quality (3 Cycles):
 =\> 167 of 169 sequences retained.
#FAS    00:10:50    167 Sequences output to NSCUK81TLR4.task11.fas.

**6. ClustalW2 tree**

ClustalW2 is then used to make a neighbour joining tree

#FAS    00:10:50    167 Sequences output to NSCUK81TLR4.task11\_cw.fas.
#TREE    00:10:50    clustalw2 -infile=NSCUK81TLR4.task11\_cw.fas -bootstrap=100 -seed=760
...
#LOAD    00:11:04    Loading data from NSCUK81TLR4.task11.phb complete: 496 lines.
#TREE    00:11:04    Loaded phb tree data from NSCUK81TLR4.task11.phb.

Tree: (((((((((((((((((1:0.03369,2:0.03918):0.15481[100],3:0.19117):0.05664[100],((4:0.16817,5:0.16873):0.01168[78],(((6:0.00600,9:0.00142):0.07860[100],7:0.07878):0.02439[97],(((8:0.0
 …
 0.00012,39:0.00252):0.00000[77],37:0.00000):0.00000[68],54:0.00000):0.00119[60],51:0.00015):0.00088[42],(((((49:0.00000,77:0.00000):0.00067[47],82:0.00067):0.00036[40],81:0.00098):0.00042[13],(50:0.00000,78:0.00000):0.00024[34]):0.00052[15],69:0.00049):0.00021[7]):0.00043[5]):0.00038[5],(48:0.00000,62:0.00000):0.00070[49]):0.00048[31],80:0.00108):0.00026[45],(40:0.00000,74:0.00000):0.00133[71]):0.00000[24],47:0.00000,(63:0.00000,68:0.00000):0.00000[26]);

#SEQ    00:11:04    167 sequences in Tree.
332 nodes in Tree.  (Unrooted)

» This tree is mapped on the sequences, rooted and duplications identified as nodes where both descendant clades share a species. This highlights the importance of having the species encoded in the names.

#ROOT    00:11:10    Midpoint root - Established Extreme Tips 100.0%%: MaxDis = 0.838790, 126..138
=\> 126 -\> 241 -\> 250 -\> 259 -\> 249 -\> 240 -\> 233 -\> 227 -\> 218 -\> 208 -\> 194 -\> 138
#ROOT    00:11:10    Midpoint Root placed. (22.3% of 259 -\> 249, len 0.023150)
...
#DUP    00:11:19    Finding Duplications : 100.0%

**7. Protein family cleanup**

Each subgroup, defined by duplications, is cleaned up to keep the "best" representative from each species. This is based primarily on similarity to the group "Master" sequence, which in turn is determined by similarity to the Query.

               +--+ 118: TLR13\_MOUSE\_\_Q6R5N8 Toll-like receptor 13 OS=Mus musculus GN=Tlr13 PE=1 SV=1 {0.046430}
               |
         +-----+ 262 [100] {0.123480}
         |     |
         |     +--+ 119: tr\_RAT\_\_A0A0U1RS05 Toll-like receptor 13 OS=Rattus norvegicus GN=Tlr13 PE=4 SV=1 {0.045870}
         |
  +------+ 279 [100] {0.133970}
  |      |
  |      +-------+ 125: tr\_MONDO\_\_K7E294 Uncharacterized protein OS=Monodelphis domestica GN=LOC100019659 PE=4 SV=1 {0.171790}
  |
#=+ 296 [74] {0.007240}
  |
  |            \*---+ 138: tr\_XENLA\_\_A0A1L8FH87 Uncharacterized protein OS=Xenopus laevis GN=XELAEV\_18037872mg PE=4 SV=1 {0.071120}
  |            |
  +------------\* 278 [100] {0.277980}
               |
               \*---+ 139: tr\_XENLA\_\_A0A1L8FNK9 Uncharacterized protein OS=Xenopus laevis GN=XELAEV\_18036155mg PE=4 SV=1 {0.070040}

GroupMaster: Group 1, 5 Seqs (TLR13\_MOUSE\_\_Q6R5N8, tr\_RAT\_\_A0A0U1RS05, tr\_MONDO\_\_K7E294, tr\_XENLA\_\_A0A1L8FH87, tr\_XENLA\_\_A0A1L8FNK9)
tr\_RAT\_\_A0A0U1RS05:    19.98% ID (197 aa); 4.76% Gaps (47 aa); 22.82% Extra (225 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)

TLR13\_MOUSE\_\_Q6R5N8:    90.31% ID (895 aa); 0.00% Gaps (0 aa); 0.50% Extra (5 aa); vs tr\_RAT\_\_A0A0U1RS05
tr\_MONDO\_\_K7E294:    65.41% ID (624 aa); 3.96% Gaps (38 aa); 0.73% Extra (7 aa); vs tr\_RAT\_\_A0A0U1RS05
tr\_XENLA\_\_A0A1L8FNK9:    34.25% ID (325 aa); 4.36% Gaps (41 aa); 0.63% Extra (6 aa); vs tr\_RAT\_\_A0A0U1RS05
tr\_XENLA\_\_A0A1L8FH87:    32.87% ID (305 aa); 6.49% Gaps (60 aa); 0.65% Extra (6 aa); vs tr\_RAT\_\_A0A0U1RS05

2 XENLA variants. ("Best" = tr\_XENLA\_\_A0A1L8FNK9) Choice:
\<0\> tr\_XENLA\_\_A0A1L8FNK9:    34.25% ID (325 aa); 4.36% Gaps (41 aa); 0.63% Extra (6 aa); vs tr\_RAT\_\_A0A0U1RS05
\<1\> tr\_XENLA\_\_A0A1L8FH87:    32.87% ID (305 aa); 6.49% Gaps (60 aa); 0.65% Extra (6 aa); vs tr\_RAT\_\_A0A0U1RS05
Remove node 278 and combine branches 296 -\> 278 and 278 -\> 139.
Removing 2 nodes and 2 branches...
#REM    00:11:23    Deleted tr\_XENLA\_\_A0A1L8FH87: Probable sequence variant vs tr\_XENLA\_\_A0A1L8FNK9.

...

Subfamily Options:
\<P\>revious,  \<T\>ree Edit, \<G\>ene Edit, \<U\>ngroup, \<D\>elete Group, Group \<M\>enu,  \<F\>inish Review No backups saved.  Group Review Finished!

We'll revisit this later when looking at how to run HAQESAC manually for protein family analysis (below).

**8. Looped cleanup**

The alignment quality and subgrouping cleanup are repeated until there is convergence (no further sequences removed), then

#SAVE    00:11:27    HAQESAC Intermediate saved as NSCUK81TLR4.task11.pickle (Python pickle).
#GZIP    00:11:27    NSCUK81TLR4.task11.pickle zipped.
#FAS    00:11:27    61 Sequences output to NSCUK81TLR4.task11.fas.
#ALN    00:11:27    Clustal Omega alignment: clustalo -i NSCUK81TLR4.task11.fas -o NSCUK81TLR4.task11.aln --outfmt=clu
#SEQ    00:11:36    61 sequences loaded from NSCUK81TLR4.task11.aln (Format: aln).
#QRY    00:11:36    Query Sequence = eog\_NOTSC\_\_NSCUK81EOG090701X7 (799 AA).
#MAP    00:11:36    Aligned sequences successfully mapped onto originals
Removing gappy (\> 50.0%) sequences relative to neighbour...
Gappy Sequence removal complete! 61 sequences remain.
#INF    00:11:37    Single Sequence Alignment Quality (SAQ) 4 for NSCUK81TLR4.task11.fas (61 Seqs).
...
#HAQ    00:12:14    SAQ4: 61 -\> 60 sequences.
...
#FAS    00:12:19    58 Sequences output to NSCUK81TLR4.task11.fas.
#INF    00:12:27    Single Sequence Alignment Quality (SAQ) 5 for NSCUK81TLR4.task11.fas (58 Seqs).
#HAQ    00:12:54    SAQ5: 58 -\> 58 sequences.

**9. Query-focused alignment cleanup**

There is then a second round of alignment quality checks that removes sequences that are poorly aligned to the query:

#INF    00:12:54    Pairwise Alignment Quality (PAQ) 1 for NSCUK81TLR4.task11.fas (58 Seqs).
#PAQ    00:14:00    PAQ1: Pairwise Comparisons ... 100.0%.
#PAQ    00:14:02    PAQ1: Linking Residues to Query (eog\_NOTSC\_\_NSCUK81EOG090701X7) ... 100.0%
#PAQ    00:14:03    PAQ1: Accounting for divergence within aligned regions ... 100.0%
PAQ1: Removing bad sequences and/or dodgy regions... Query (eog\_NOTSC\_\_NSCUK81EOG090701X7) processed...
tr\_CHEMY\_\_M7AIQ3 worst: -1,786 aa if kept vs -638 aa if lost.
...
#HAQ    00:14:04    PAQ1: 58 -\> 58 sequences.
#FAS    00:14:04    58 Sequences output to NSCUK81TLR4.task11.haq.fas.

Finished Pairwise Alignment Quality (1 Cycles):
 =\> 58 of 167 sequences retained.
#FAS    00:14:04    58 Sequences output to NSCUK81TLR4.task11.fas.

**10. Establishment of subfamilies**

A more careful tree-based assessment of duplications and subfamilies is then peformed to produce the final tree and subfamilies.

#INF    00:14:04    Establishment of Subfamilies for NSCUK81TLR4.task11.fas (58 Seqs, Group=dup).
#FAS    00:14:04    58 Sequences output to NSCUK81TLR4.task11\_cw.fas.
#TREE    00:14:04    clustalw2 -infile=NSCUK81TLR4.task11\_cw.fas -bootstrap=1000 -seed=922 -kimura
...
#GRP    00:14:24    6 Groups (34 Sequences) output in NSCUK81TLR4.task11.grp.
#FAS    00:14:24    58 Sequences output to NSCUK81TLR4.task11.fas.
#TREE    00:14:24    Saving tree to NSCUK81TLR4.task11.nwk as Newick Standard Format (MEGA compatible).
#OUT    00:14:24    filename='NSCUK81TLR4.task11.nwk', type='nwk', seqnum=False, seqname='long', maxnamelen=123, blen='Length', bootstraps='boot'
#TREE    00:14:24    Saving tree to NSCUK81TLR4.task11.tree.txt as Plain text.
#OUT    00:14:24    filename='NSCUK81TLR4.task11.tree.txt', type='text', seqnum=True, seqname='long', maxnamelen=0, blen='Length', bootstraps='boot'
#OUT    00:14:24    Text tree saved to NSCUK81TLR4.task11.tree.txt
#TREE    00:14:24    Saving tree to NSCUK81TLR4.task11.png as PNG with query species highlighted.
#OUT    00:14:24    filename='NSCUK81TLR4.task11.png', type='qspec', seqnum=False, seqname='long', maxnamelen=123, blen='Length', bootstraps='boot'
#RTREE    00:14:24    Data for 115 nodes output to NSCUK81TLR4.task11.r.csv
#RPATH    00:14:24    R
#QSPEC    00:14:24    /share/apps/slimsuite/libraries/r/budapest.r
#RTREE    00:14:24    R --no-restore --no-save --args "NSCUK81TLR4.task11.r.csv" "NSCUK81TLR4.task11.png" \< "/share/apps/slimsuite/libraries/r/budapest.r" \> "NSCUK81TLR4.task11.r.run"

**11. Ancestral sequence prediction**

The final step of HAQESAC is ancestral sequence prediction, which we will not use in this prac.

...
#GASP    00:15:28    Gapped Ancestral Sequence Prediction Complete.
Saving Ancestral Sequences in NSCUK81TLR4.task11.anc.fas...
#FAS    00:15:28    115 Sequences output to NSCUK81TLR4.task11.anc.fas.
#PAM    00:15:39    Calculation of branch ML PAM complete.
#TREE    00:15:39    Saving tree to NSCUK81TLR4.task11.anc.nsf as Newick Standard Format (NSF).
...
#OUT    00:15:39    Text tree saved to NSCUK81TLR4.task11.anc.txt
#OUT    00:15:39    115 Sequences output to NSCUK81TLR4.task11.scanseq in scansite parallel format
#FAS    00:15:39    115 Sequences output to NSCUK81TLR4.task11.degap.fas.

Thank you for using HAQESAC. As always, it is recommended that you check your alignments manually for errors. Please send any comments or suggestions to richard.edwards@unsw.edu.au.

#LOG    00:15:39    HAQESAC V1.10.2 End: Thu Sep  7 14:46:39 2017

The log will record the start and end time, any commands used and the main steps. It will also record any errors etc. It is a good idea to copy the log file over and attach it to your LabArchives lab book entry.

## 17.4.Using MultiHAQ for protein family analysis using local BLAST databases

HAQESAC has a wrapper for more automated analysis, called  **MultiHAQ**. We are going to use MultiHAQ to run a number of BLAST searches for our query proteins and then run HAQESAC on the combined set of homologues. At the end of the Activity, we will see how MultiHAQ can be used to automate the whole process. If you are struggling with the interactive HAQESAC run, you might want to try out the exercise at the end first.

For this exercise, we will use two files on the server:

- /share/data/babsgenome/annotation/Nscutatus.k81L500.2017-08-18.busco.fas = all the BUSCO predictions for our ABySS assembly, reformatted for SLiMSuite
- /share/data/babsgenome/qfo/qfo\_eukaryota.2017-04.fas = a set of reference Eukaryote proteomes from the "Quest for Orthologues" project

**NOTE: ** This will give a more controlled set of outputs that should run quite quickly but with the downside that we will not have as many closely-related sequences as from a Uniprot search. There are also a file of Sauropsida sequences from Uniprot and a larger file of all Uniprot chordate sequences on the server that you can use for your real analysis if you choose:

- /share/data/babsgenome/uniprot/uniprot.sauropsida.2017-09-07.fas
- /share/data/babsgenome/uniprot/uniprot.chordata.2017-07-27\_all.fas

See also the updated files in **Section 18.6**.

### 17.4.1.Extracting our query sequence

First, we will extract the BUSCO query for the search. As the reformatted files have the sequences on a single line, we can use grep for this:

$ grep -A 1 NSCUK81EOG090701X7 /share/data/babsgenome/annotation/Nscutatus.k81L500.2017-08-18.busco.fas \> NSCUK81QUERY.fas

**Question: ** What does the  **-A 1**  flag do?

### 17.4.2.Running multiple BLASTs with MultiHAQ

MultiHAQ can run on multiple queries but we will run it here with just one. Because we are searching a database with a much more limited number of sequences, we can be a bit more stringent with our  **blastcut=X**  setting.

$ module add blast+/2.6.0 clustalw/2.1 clustalo/1.2.4 R/3.4.0
$ python /share/apps/slimsuite/tools/multihaq.py -seqin NSCUK81QUERY.fas -basefile NSCUK81QUERY.multi blast2fas="/share/data/babsgenome/annotation/Nscutatus.k81L500.2017-08-18.busco.fas,/share/data/babsgenome/qfo/qfo\_eukaryota.2017-04.fas" blastcut=50 i=0 haqesac=F

When running against a Uniprot database, the number of hits will be protein-dependent as it depends largely on how well studied that protein is. (TLR4 is pretty well studied.) You may therefore need to increase the blastcut value and/or add some species filters if your first run does not produce useful output. The blastcut=50 cut-off is applied to each search database independently by MultiHAQ but then applied to the _combined_ hits file by HAQESAC. This means that if we had included the uniprot.sauropsida.2017-09-07.fas file and it returned a lot of TLR4 hits (which it would!), those hits would potentially swamp the more distant QFO and BUSCO hits. To get round, you can prevent MultiHAQ from running HAQESAC automatically on the combined file by adding  **haqesac=F**. This gives you an opportunity to look at the file produced and run HAQESAC (or something else) with filtering setting based on what it looks like. This can be useful when searching the wider uniprot files as you can check the species distribution and/or relax the blastcut value for the HAQESAC run.

You should now have a NSCUK81QUERY\_HAQESAC/ directory containing three files:

$ ls -lrth NSCUK81QUERY\_HAQESAC/

haqesac.bat
haqesac.ini
NSCUK81EOG090701X7.fas

The haqesac files would have been used if we has not run with haqesac=F. The NSCUK81EOG090701X7.fas file contains the combined hits from our searches. If we had multiple query sequences in our original file, we would have one file for each sequence.

**NOTE:**  In addition to the sequence files we told it to search, MultiHAQ also performs a search against the query file itself. If several of our search databases contain the same sequences, these will be present in the file multiple times:

$ grep NSCUK81EOG090701X7 NSCUK81EOG090701X7\_HAQESAC/NSCUK81EOG090701X7.fas
\>eog\_NOTSC\_\_NSCUK81EOG090701X7 EOG090701X7:Nscutatus.k81L500.2017-08-18.fasta:scaf\_NOTSC\_\_K81SCAF11599273:5156-9185
\>eog\_NOTSC\_\_NSCUK81EOG090701X7 EOG090701X7:Nscutatus.k81L500.2017-08-18.fasta:scaf\_NOTSC\_\_K81SCAF11599273:5156-9185

This will not be an issue if we run HAQESAC as it automatically cleans this up but is something to remember if you use the file with a different downstream tool.

**Question**** :** Why do we have NSCUK81EOG090701X7 twice in our output file?

**CAUTION: ** If you run MultiHAQ several times with the same seqin=FILE input _in the same directory_, you will need to set  **haqdir=PATH**  to rename the output HAQESAC directory. By default, it is named after the query file and it will cause conflicts if multiple runs use the same directory. Alternatively, run in a different directory or copy the input file to give it a new name.

## 17.5.Running HAQESAC interactively

Now enter the NSCUK81QUERY\_HAQESAC/ directory. It is here that HAQESAC would be run had we not stopped it with haqesac=F. As we saw above, it has three files:

$ ls

haqesac.bat  haqesac.ini  NSCUK81EOG090701X7.fas

If we had run MultiHAQ with haqesac=T, the command in the haqesac.bat file would have run:

$ more haqesac.bat

python /share/apps/slimsuite/tools/haqesac.py seqin=NSCUK81EOG090701X7.fas query=NSCUK81EOG090701X7 basefile=NSCUK81EOG090701X7

Instead, we will run HAQESAC ourselves but give it a few more options.

Look in the  **haqesac.ini**  file. You will see the list of commandline options that HAQESAC will read in. These were set by MultiHAQ. Note that HAQESAC will automatically read in a haqesac.ini file if present, so it was not needed as part of the python call above. Options in this file can be over-ridden by commandline settings.

This this case, we want to over-ride the blastcut=50 setting to keep ALL of the sequences that MultiHAQ pulled out. Setting blastcut=0 will use all sequences that pass the other filters. We will also switch multihaq=F as we are not running this as part of MultiHAQ:

$ python /share/apps/slimsuite/tools/haqesac.py seqin=NSCUK81EOG090701X7.fas query=NSCUK81EOG090701X7 basefile=NSCUK81EOG090701X7 blastcut=0 multihaq=F

As before, HAQESAC is now going to cycle through a number of steps:

1. Initial sequence filtering. (It will have removed the rogue query duplicate.)
2. Removal of sequences that are too disimilar to the query. (Must have 40%+ global similarity and 60%+ coverage.)
3. Several rounds of sequence aligment followed by removal of sequences that appear to align badly. This iterates until no more sequences are removed.
4. Generation of a phylogenetic tree, which is used to identify gene duplications.
5. Cleanup of each putative protein subfamily (produced by a duplication) to retain the "best" representative sequence of each species. (Where "best" is highest identity to the query.)
6. Additional rounds of sequence alignment, alignment quality and protein subfamily cleanup until no more sequences are removed.
7. Generation of a final phylogenetic tree with 1000 bootstrap replicates.
8. Ancestral sequence prediction using GASP.

However, this time we have run with i=0 rather than i=-1. This means that HAQESAC will stop to ask us questions, and give some opportunites for additional editing that is useful later.

### 17.5.1.Subfamily grouping

HAQESAC will run to the point of initial subfamily grouping and then pause. It will show a tree where groups have been compressed:

      #==+ \*88\*: 16 Seqs (eog\_NOTSC\_\_NSCUK81EOG090701X7, tr\_CHICK\_\_C4PCF3, tr\_MONDO\_\_F6Y6W8, TLR4\_BOVIN\_\_Q9GL65, tr\_CANLF\_\_F1PDB9, tr\_BOVIN\_\_Q6WCD5, tr\_PANTR\_\_H2QXS5, TLR4\_HUMAN\_\_O00206, tr\_GORGO\_\_G3RY19, TLR4\_GORGO\_\_Q8SPE8, TLR4\_MOUSE\_\_Q9QUK6, TLR4\_RAT\_\_Q9QX05, tr\_DANRE\_\_F1QSN2, tr\_DANRE\_\_F6NLN8, tr\_DANRE\_\_B8A691, tr\_LEPOC\_\_W5M7V9) [100] {0.034940}
      |
    #=# 90 [100] {0.018290}
    | |
    | #===+ \*87\*: 10 Seqs (tr\_CHICK\_\_E1BRV3, CD180\_MOUSE\_\_Q62192, tr\_PANTR\_\_H2QR03, tr\_RAT\_\_D3ZIP2, CD180\_HUMAN\_\_Q99467, tr\_GORGO\_\_G3QYH4, tr\_MONDO\_\_F6TTU8, tr\_BOVIN\_\_F1MFI2, tr\_CANLF\_\_E2R687, tr\_DANRE\_\_F1RAS7) [100] {0.060590}
    |
+---# 91
    |
    | #==+ \*86\*: 11 Seqs (tr\_RAT\_\_E9PTD9, TLR2\_HUMAN\_\_O60603, TLR2\_GORGO\_\_B3Y615, tr\_PANTR\_\_H2QQA8, tr\_GORGO\_\_G3QKN2, TLR2\_PANTR\_\_B3Y613, tr\_LEPOC\_\_W5MMU8, tr\_XENTR\_\_F6PY71, tr\_XENTR\_\_A0A1B8XYC9, tr\_XENTR\_\_F6PY92, tr\_XENTR\_\_A0A1B8XYC2) [100] {0.042190}
    | |
    #=# 89 [100] {0.012780}
      |
      | #=+ \*79\*: 6 Seqs (TLR13\_MOUSE\_\_Q6R5N8, tr\_RAT\_\_A0A0U1RS05, tr\_MONDO\_\_K7E294, tr\_LEPOC\_\_W5NP58, tr\_XENTR\_\_F6Y5V3, tr\_DANRE\_\_B3DJL6) [100] {0.024800}
      | |
      #=# 85 [79] {0.006820}
        |
        #========+ \*78\*: 3 Seqs (tr\_BOVIN\_\_Q2LDA0, tr\_RAT\_\_G3V6F8, tr\_MONDO\_\_F7AEY6) [100] {0.176340}

A summary of the grouping options:

#\*# Grouping Options #\*#
[Bootstrap cut-off: 70 (0.700000)]
[Min Family Size: 3]
 [Min Family Number: 0]
[Group by Query Species: False (None)]
[Allow Sequence Variants: False]
[Allow Query species Variants: False]
 [Allow Orphan Sequences: True]

This means that groups will be defined by duplications where a clade has 70% bootstrap support and at least 3 members. Don't worry about the other options for now. There is then a group summary:

#\*# Grouping Summary #\*#
Currently 5 groups. (0 Orphans)

Group 1: 3 seqs (tr\_BOVIN\_\_Q2LDA0, tr\_RAT\_\_G3V6F8, tr\_MONDO\_\_F7AEY6)
Group 2: 6 seqs (TLR13\_MOUSE\_\_Q6R5N8, tr\_RAT\_\_A0A0U1RS05, tr\_MONDO\_\_K7E294, tr\_LEPOC\_\_W5NP58, tr\_XENTR\_\_F6Y5V3, tr\_DANRE\_\_B3DJL6)                                                               Group 3: 11 seqs (tr\_RAT\_\_E9PTD9, tr\_LEPOC\_\_W5MMU8, TLR2\_HUMAN\_\_O60603, TLR2\_GORGO\_\_B3Y615, tr\_PANTR\_\_H2QQA8, tr\_GORGO\_\_G3QKN2, TLR2\_PANTR\_\_B3Y613, tr\_XENTR\_\_F6PY71, tr\_XENTR\_\_A0A1B8XYC9, tr\_XENTR\_\_F6PY92, tr\_XENTR\_\_A0A1B8XYC2)
Group 4: 10 seqs (tr\_CHICK\_\_E1BRV3, CD180\_MOUSE\_\_Q62192, tr\_PANTR\_\_H2QR03, tr\_RAT\_\_D3ZIP2, CD180\_HUMAN\_\_Q99467, tr\_GORGO\_\_G3QYH4, tr\_MONDO\_\_F6TTU8, tr\_BOVIN\_\_F1MFI2, tr\_CANLF\_\_E2R687, tr\_DANRE\_\_F1RAS7)                                                               Group 5: 16 seqs (eog\_NOTSC\_\_NSCUK81EOG090701X7, tr\_CHICK\_\_C4PCF3, tr\_MONDO\_\_F6Y6W8, TLR4\_BOVIN\_\_Q9GL65, tr\_CANLF\_\_F1PDB9, tr\_BOVIN\_\_Q6WCD5, tr\_PANTR\_\_H2QXS5, TLR4\_HUMAN\_\_O00206, tr\_GORGO\_\_G3RY19, TLR4\_GORGO\_\_Q8SPE8, TLR4\_MOUSE\_\_Q9QUK6, TLR4\_RAT\_\_Q9QX05, tr\_DANRE\_\_F1QSN2, tr\_DANRE\_\_F6NLN8, tr\_DANRE\_\_B8A691, tr\_LEPOC\_\_W5M7V9)

"Orphans" are sequences not assigned to a particular group. We have used some well-behaved data here (one of the benefits of QFO) so none of our sequences are orphans. You then have some options of what to do next:

 \<K\>eep current grouping.  \*\*\* WARNING: Current Grouping breaks 1+ rules. \*\*\*
 ---
 \<O\>ptions (Change Grouping 'rules').
 ---
 \<L\>oad Grouping.
 \<D\>uplication Grouping.  (All Duplications)
 \<M\>anual Grouping.
 \<N\>o Grouping (MinFamNum=0).
 \<A\>ll sequences in one group.
 \<E\>dit Grouping (Manual)
 ---
 \<R\>eview Groups
 \<G\>roup in SeqList (Reorder)
 \<P\>urge Orphan Sequences (not in a group)
 \<S\>ave Groups
 ---
 \<F\>ull auto mode
 ---
 \<Q\>uit

Choice for Grouping? [default=K]:

**NOTE:**  It its giving a warning: \*\*\* WARNING: Current Grouping breaks 1+ rules. \*\*\*. This is because some of our groups contain multiple sequences from the same species and we have set [Allow Sequence Variants: False]. This is what we will clean up in the next step.

**NOTE:**  If you run on more complex data, your initial groupings will be messy and/or have low bootstrap support. You can manually tidy this up using \<E\>dit Grouping (Manual). Ask for help the first time you try this! Alternatively, just accept the grouping suggestions each time - they should get cleaner as HAQESAC progresses.

For now, we will \<K\>eep current grouping despite the warning and go on to the Group Review phase. It will ask if you are sure:

Keep Groups? (y/n) [default=Y]:
Grouping rules broken. Are you sure? (y/n) [default=Y]:

Hit ENTER to proceed.

### 17.5.2.Manual Group Review

Next, HAQESAC will step through each of the groups identified in the previous stage and give some editing options. For now, there are only two we want to worry about:

1. Sequence variant removal.
2. Gene naming.

The first group has no variants:

            +------+ 32: tr\_BOVIN\_\_Q2LDA0 Toll-like receptor 5 OS=Bos taurus GN=TLR5 PE=3 SV=1 {0.146740}
            |
         +--+ 69 [100] {0.043090}
         |  |
         |  +-------+ 33: tr\_RAT\_\_G3V6F8 RCG20122 OS=Rattus norvegicus GN=Tlr5 PE=3 SV=1 {0.150460}
         |
#========+ 78 [100] {0.176340}
         |
         +--------+ 44: tr\_MONDO\_\_F7AEY6 Uncharacterized protein OS=Monodelphis domestica GN=TLR5 PE=3 SV=1 {0.195010}

GroupMaster: Group 0, 3 Seqs (tr\_BOVIN\_\_Q2LDA0, tr\_RAT\_\_G3V6F8, tr\_MONDO\_\_F7AEY6)
tr\_RAT\_\_G3V6F8: 21.58% ID (188 aa); 12.14% Gaps (106 aa); 19.40% Extra (169 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)

tr\_BOVIN\_\_Q2LDA0:       70.28% ID (603 aa); 1.49% Gaps (13 aa); 0.00% Extra (0 aa); vs tr\_RAT\_\_G3V6F8
tr\_MONDO\_\_F7AEY6:       58.22% ID (503 aa); 2.41% Gaps (21 aa); 1.62% Extra (14 aa); vs tr\_RAT\_\_G3V6F8

Subfamily Options:
\<T\>ree Edit, \<G\>ene Edit, \<U\>ngroup, \<D\>elete Group, Group \<M\>enu,  \<Q\>uit Review, \<N\>ext  ? [default=N]:

Looking at these sequences, you can see that many of them start tr\_, indicating they come from TrEMBL. This is not particularly useful for quickly identifying what a given sequence is. Instead, we can make a judgement call and replace this with the probably gene.

**Question:**  Looking at the descriptions on these three sequences, which gene do you think this is?

Type  **G**  (and ENTER) to perform the \<G\>ene Edit:

New Gene?:  tlr5

Enter tlr5. We will use lower case to avoid making the sequences look like SwissProt IDs. (We'll see this in a minute.) You will now see that all of the sequences have been renamed:

            +------+ 32: tlr5\_BOVIN\_\_Q2LDA0 Toll-like receptor 5 OS=Bos taurus GN=TLR5 PE=3 SV=1 {0.146740}
            |
         +--+ 69 [100] {0.043090}
         |  |
         |  +-------+ 33: tlr5\_RAT\_\_G3V6F8 RCG20122 OS=Rattus norvegicus GN=Tlr5 PE=3 SV=1 {0.150460}
         |
#========+ 78 [100] {0.176340}
         |
         +--------+ 44: tlr5\_MONDO\_\_F7AEY6 Uncharacterized protein OS=Monodelphis domestica GN=TLR5 PE=3 SV=1 {0.195010}

GroupMaster: Group 0, 3 Seqs (tr\_BOVIN\_\_Q2LDA0, tr\_RAT\_\_G3V6F8, tr\_MONDO\_\_F7AEY6)
tlr5\_RAT\_\_G3V6F8:       21.58% ID (188 aa); 12.14% Gaps (106 aa); 19.40% Extra (169 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)

tlr5\_BOVIN\_\_Q2LDA0:     70.28% ID (603 aa); 1.49% Gaps (13 aa); 0.00% Extra (0 aa); vs tlr5\_RAT\_\_G3V6F8
tlr5\_MONDO\_\_F7AEY6:     58.22% ID (503 aa); 2.41% Gaps (21 aa); 1.62% Extra (14 aa); vs tlr5\_RAT\_\_G3V6F8

This is much more user-friendly and will make like much easier when looking at the final alignments and trees.

Now go onto the \<N\>ext subgroup. This time, we have one Swissprot sequence with a gene ID already part of the name:

                +--+ 26: TLR13\_MOUSE\_\_Q6R5N8 Toll-like receptor 13 OS=Mus musculus GN=Tlr13 PE=1 SV=1 {0.046180}
                |
          +-----+ 61 [100] {0.122880}
          |     |
          |     +--+ 27: tr\_RAT\_\_A0A0U1RS05 Toll-like receptor 13 OS=Rattus norvegicus GN=Tlr13 PE=4 SV=1 {0.046110}
          |
  +-------+ 71 [100] {0.172320}
  |       |
  |       +-------+ 28: tr\_MONDO\_\_K7E294 Uncharacterized protein OS=Monodelphis domestica GN=LOC100019659 PE=4 SV=1 {0.172390}
  |
#=+ 79 [100] {0.024800}
  |
  |     +-----------+ 29: tr\_LEPOC\_\_W5NP58 Uncharacterized protein OS=Lepisosteus oculatus PE=3 SV=1 {0.259800}
  |     |
  |  +--+ 60 [100] {0.036700}
  |  |  |
  |  |  +-----------+ 43: tr\_DANRE\_\_B3DJL6 Toll-like receptor 22 OS=Danio rerio GN=tlr22 PE=2 SV=1 {0.263050}
  |  |
  +--+ 70 [100] {0.035370}
     |
     +------------+ 30: tr\_XENTR\_\_F6Y5V3 Toll-like receptor22 OS=Xenopus tropicalis GN=LOC100485706 PE=3 SV=1 {0.298660}

GroupMaster: Group 1, 6 Seqs (TLR13\_MOUSE\_\_Q6R5N8, tr\_RAT\_\_A0A0U1RS05, tr\_MONDO\_\_K7E294, tr\_LEPOC\_\_W5NP58, tr\_XENTR\_\_F6Y5V3, tr\_DANRE\_\_B3DJL6)
tr\_RAT\_\_A0A0U1RS05:     19.47% ID (192 aa); 5.26% Gaps (52 aa); 23.23% Extra (229 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)

TLR13\_MOUSE\_\_Q6R5N8:    90.31% ID (895 aa); 0.00% Gaps (0 aa); 0.50% Extra (5 aa); vs tr\_RAT\_\_A0A0U1RS05
tr\_MONDO\_\_K7E294:       65.41% ID (624 aa); 3.96% Gaps (38 aa); 0.73% Extra (7 aa); vs tr\_RAT\_\_A0A0U1RS05
tr\_LEPOC\_\_W5NP58:       32.54% ID (314 aa); 5.27% Gaps (51 aa); 3.21% Extra (31 aa); vs tr\_RAT\_\_A0A0U1RS05
tr\_XENTR\_\_F6Y5V3:       31.48% ID (295 aa); 7.20% Gaps (67 aa); 2.35% Extra (22 aa); vs tr\_RAT\_\_A0A0U1RS05
tr\_DANRE\_\_B3DJL6:       29.25% ID (277 aa); 6.49% Gaps (61 aa); 2.64% Extra (25 aa); vs tr\_RAT\_\_A0A0U1RS05

Note that we also have something of a naming conflict, with the mammalian sequences being TLR13 (or uncharacterised) and the others as TLR22. This could be a grouping issue and we might decide to regroup on this basis. For now, to demonstrate the program functions, we will stick with TLR13.

Type  **G**  (and ENTER) to perform the \<G\>ene Edit and set the gene to tlr13:

**Question:**  What happened to TLR13\_MOUSE? Now \<G\>ene Edit to tlr22. What happened to TLR13\_MOUSE? Now \<G\>ene Edit back to tlr13 again.

You should have noticed that TLR13\_MOUSE\_\_Q6R5N8 remained unchanged throughout. This is because the upper case gene identifies it as a curated Swissprot ID that we do not want to change. (This is why we stick to lower case genes ourselves.)

### 17.5.3.Sequence variant removal

The next group is a bit messier. This has several XENTR (Xenopus tropicalis) variants that all cluster together:

             +------+ 34: tr\_RAT\_\_E9PTD9 Toll-like receptor OS=Rattus norvegicus GN=Tlr2 PE=1 SV=1 {0.137820}
             |
   +---------+ 81 [100] {0.201910}
   |         |
   |         |          +-+ 36: TLR2\_HUMAN\_\_O60603 Toll-like receptor 2 OS=Homo sapiens GN=TLR2 PE=1 SV=1 {0.000670}
   |         |          |
   |         |        #=+ 55 [57] {0.000860}
   |         |        | |
   |         |        | +-+ 37: TLR2\_GORGO\_\_B3Y615 Toll-like receptor 2 OS=Gorilla gorilla gorilla GN=TLR2 PE=2 SV=1 {0.000610}
   |         |        |
   |         |      +-# 65 [49] {0.000820}
   |         |      | |
   |         |      | #=+ 39: tr\_GORGO\_\_G3QKN2 Toll-like receptor OS=Gorilla gorilla gorilla GN=TLR2 PE=3 SV=1 {0.001690}
   |         |      |
   |         +------+ 73 [100] {0.142950}
   |                |
   |                | \*-+ 38: tr\_PANTR\_\_H2QQA8 Toll-like receptor OS=Pan troglodytes GN=TLR2 PE=3 SV=1 {0.000700}
   |                | |
   |                +-\* 64 [65] {0.001730}
   |                  |
   |                  \*-+ 40: TLR2\_PANTR\_\_B3Y613 Toll-like receptor 2 OS=Pan troglodytes GN=TLR2 PE=2 SV=1 {0.000570}
   |
#==+ 86 [100] {0.042190}
   |
   |     +----------+ 35: tr\_LEPOC\_\_W5MMU8 Toll-like receptor OS=Lepisosteus oculatus PE=3 SV=1 {0.241980}
   |     |
   +-----+ 80 [100] {0.109540}
         |
         |           \*-+ 41: tr\_XENTR\_\_F6PY71 Toll-like receptor OS=Xenopus tropicalis GN=LOC100485512 PE=3 SV=1 {-0.001380}
         |           |
         |   \*-------\* 63 [100] {0.166880}
         |   |       |
         |   |       \*-+ 42: tr\_XENTR\_\_A0A1B8XYC9 Toll-like receptor OS=Xenopus tropicalis GN=XENTR\_v90029415mg PE=3 SV=1 {0.001380}
         |   |
         +---\* 72 [100] {0.068460}
             |
             |        \*-+ 45: tr\_XENTR\_\_F6PY92 Uncharacterized protein (Fragment) OS=Xenopus tropicalis GN=LOC100485358 PE=4 SV=1 {0.000000}
             |        |
             \*--------\* 62 [100] {0.178010}
                      |
                      \*-+ 46: tr\_XENTR\_\_A0A1B8XYC2 Toll-like receptor OS=Xenopus tropicalis GN=XENTR\_v90029413mg PE=3 SV=1 {0.000000}

GroupMaster: Group 2, 11 Seqs (tr\_RAT\_\_E9PTD9, TLR2\_HUMAN\_\_O60603, TLR2\_GORGO\_\_B3Y615, tr\_PANTR\_\_H2QQA8, tr\_GORGO\_\_G3QKN2, TLR2\_PANTR\_\_B3Y613, tr\_LEPOC\_\_W5MMU8, tr\_XENTR\_\_F6PY71, tr\_XENTR\_\_A0A1B8XYC9, tr\_XENTR\_\_F6PY92, tr\_XENTR\_\_A0A1B8XYC2)
tr\_XENTR\_\_F6PY92:       20.85% ID (172 aa); 15.64% Gaps (129 aa); 18.30% Extra (151 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)

tr\_XENTR\_\_A0A1B8XYC2:   98.57% ID (825 aa); 0.00% Gaps (0 aa); 1.43% Extra (12 aa); vs tr\_XENTR\_\_F6PY92
tr\_XENTR\_\_A0A1B8XYC9:   64.02% ID (532 aa); 0.73% Gaps (6 aa); 1.44% Extra (12 aa); vs tr\_XENTR\_\_F6PY92
tr\_XENTR\_\_F6PY71:       66.20% ID (521 aa); 4.61% Gaps (36 aa); 0.00% Extra (0 aa); vs tr\_XENTR\_\_F6PY92
tr\_LEPOC\_\_W5MMU8:       52.10% ID (421 aa); 3.64% Gaps (29 aa); 1.61% Extra (13 aa); vs tr\_XENTR\_\_F6PY92
TLR2\_HUMAN\_\_O60603:     29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92
TLR2\_GORGO\_\_B3Y615:     29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92
TLR2\_PANTR\_\_B3Y613:     29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92
tr\_PANTR\_\_H2QQA8:       29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92
tr\_GORGO\_\_G3QKN2:       29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92
tr\_RAT\_\_E9PTD9: 29.72% ID (233 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92

4 XENTR variants. ("Best" = tr\_XENTR\_\_F6PY92) Choice:

\<0\> tr\_XENTR\_\_F6PY92:   20.85% ID (172 aa); 15.64% Gaps (129 aa); 18.30% Extra (151 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)
\<1\> tr\_XENTR\_\_A0A1B8XYC2:       20.55% ID (172 aa); 15.64% Gaps (131 aa); 19.47% Extra (163 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)
\<2\> tr\_XENTR\_\_A0A1B8XYC9:       20.22% ID (168 aa); 15.64% Gaps (130 aa); 18.89% Extra (157 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)
\<3\> tr\_XENTR\_\_F6PY71:   21.09% ID (166 aa); 17.90% Gaps (141 aa); 16.65% Extra (131 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)
 \<0\> tr\_XENTR\_\_F6PY92; \<1\> tr\_XENTR\_\_A0A1B8XYC2; \<2\> tr\_XENTR\_\_A0A1B8XYC9; \<3\> tr\_XENTR\_\_F6PY71; \<K\> keep variants; \<N\>ext group:? [default=0]:

Unless they are closely related to your query, we generally do not want to keep multiple variants. These might represent splice variants, annotation artefacts or "in-paralogues", which are lineage-specific duplications. HAQESAC will show each variant with some summary statistics of how similar they are to the query (our BUSCO gene), derived from the current multiple sequence alignment. If in doubt, accept the first one (\<0\>). Sometimes, you might decide to keep a slightly less similar sequence because it has better annotation, for example.

After removing the Xenopus variants, we are presented with Gorilla variants:

2 GORGO variants. ("Best" = TLR2\_GORGO\_\_B3Y615) Choice:
\<0\> TLR2\_GORGO\_\_B3Y615: 29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92
\<1\> tr\_GORGO\_\_G3QKN2:   29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tr\_XENTR\_\_F6PY92

 \<0\> TLR2\_GORGO\_\_B3Y615; \<1\> tr\_GORGO\_\_G3QKN2; \<K\> keep variants; \<N\>ext group? [default=0]:

In this case, we definitely want the first one as it is a Swissprot sequence (TLR2\_GORGO vs tr\_GORGO).

**NOTE:**  It is not always easy to decide how much to clean up a subfamily and which variants to remove. Just make sure that you  **document your choices**  and why you made them (even if arbitrary).

Repeat with the PANTR (chimp) variants and change the gene to tlr2:

             +------+ 34: tlr2\_RAT\_\_E9PTD9 Toll-like receptor OS=Rattus norvegicus GN=Tlr2 PE=1 SV=1 {0.137820}
             |
   +---------+ 71 [100] {0.201910}
   |         |
   |         |        +-+ 36: TLR2\_HUMAN\_\_O60603 Toll-like receptor 2 OS=Homo sapiens GN=TLR2 PE=1 SV=1 {0.000670}
   |         |        |
   |         |      +-+ 56 [57] {0.001680}
   |         |      | |
   |         |      | +-+ 37: TLR2\_GORGO\_\_B3Y615 Toll-like receptor 2 OS=Gorilla gorilla gorilla GN=TLR2 PE=2 SV=1 {0.000610}
   |         |      |
   |         +------+ 63 [100] {0.142950}
   |                |
   |                +-+ 38: TLR2\_PANTR\_\_B3Y613 Toll-like receptor 2 OS=Pan troglodytes GN=TLR2 PE=2 SV=1 {0.002300}
   |
#==+ 76 [100] {0.042190}
   |
   |     +----------+ 35: tlr2\_LEPOC\_\_W5MMU8 Toll-like receptor OS=Lepisosteus oculatus PE=3 SV=1 {0.241980}
   |     |
   +-----+ 70 [100] {0.109540}
         |
         +----------+ 41: tlr2\_XENTR\_\_F6PY92 Uncharacterized protein (Fragment) OS=Xenopus tropicalis GN=LOC100485358 PE=4 SV=1 {0.246470}

GroupMaster: Group 2, 11 Seqs (tr\_RAT\_\_E9PTD9, TLR2\_HUMAN\_\_O60603, TLR2\_GORGO\_\_B3Y615, tr\_PANTR\_\_H2QQA8, tr\_GORGO\_\_G3QKN2, TLR2\_PANTR\_\_B3Y613, tr\_LEPOC\_\_W5MMU8, tr\_XENTR\_\_F6PY71, tr\_XENTR\_\_A0A1B8XYC9, tr\_XENTR\_\_F6PY92, tr\_XENTR\_\_A0A1B8XYC2)
tlr2\_XENTR\_\_F6PY92:     20.85% ID (172 aa); 15.64% Gaps (129 aa); 18.30% Extra (151 aa); vs Query (eog\_NOTSC\_\_NSCUK81EOG090701X7)

tlr2\_LEPOC\_\_W5MMU8:     52.10% ID (421 aa); 3.64% Gaps (29 aa); 1.61% Extra (13 aa); vs tlr2\_XENTR\_\_F6PY92
TLR2\_HUMAN\_\_O60603:     29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tlr2\_XENTR\_\_F6PY92
TLR2\_GORGO\_\_B3Y615:     29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tlr2\_XENTR\_\_F6PY92
TLR2\_PANTR\_\_B3Y613:     29.85% ID (234 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tlr2\_XENTR\_\_F6PY92
tlr2\_RAT\_\_E9PTD9:       29.72% ID (233 aa); 7.15% Gaps (56 aa); 2.30% Extra (18 aa); vs tlr2\_XENTR\_\_F6PY92

Continue through the rest of the groups. Once you finish, you will be asked to accept the groups and given the option to make yourself a note in the log:

Accept Groups? (y/n) [default=Y]:
Text for log file? (Blank to skip):  Reduced to a single variant per group. Unsure of TLR13 labelling.

You will also be given the option to save a backup at this point. Generally, you will not need this. (Later HAQESAC cleanup might dump some of these sequences/groups. If you have spent a lot of time going over them, you might want to revisit these data.)

Save current sequence alignment and tree for backup? (y/n) [default=N]:
No backups saved.  Group Review Finished!

### 17.5.4.HAQESAC Cycles and final subgrouping

HAQESAC will now cycle through additional cycles. If there was any change in sequence grouping since the previous (pre-edit) groups, it will give you the option to review again. Otherwise, it will cycle until it is ready for the final subgroup allocation:

\*\*\* No Sequences lost. Accept 35 seqs (5 Groups)? (y/n) [default=Y]:

This will now generate a new tree with 1000 bootstraps rather than 100. You now have a final chance to repeat the subgroup analysis. At this point, all the sequences should be well-aligned, but you might still decide that some sequences and or groups are not useful in your final tree and decide to get rid of them.

For now, keep all the groups. HAQESAC will perform its final steps and then finish with a recommendation:

Thank you for using HAQESAC. As always, it is recommended that you check your alignments manually for errors. Please send any comments or suggestions to richard.edwards@unsw.edu.au.  \<ENTER\> to continue.

## 17.6.Combining interactive and non-interactive HAQESAC runs

Some of you might be a feeling a bit overwhelmed by now. The last task for this week is to see how we can combine the automated and interactive applications of MultiHAQ and HAQESAC to generate pretty decent alignments with useful sequence names.

First, we run MultiHAQ in fully automated mode (i=-1) and include the Sauropsid Uniprot data to increase the number of close homologues in our alignment and tree. I have already done this and the results can be found in:

/share/data/babsgenome/examples/HAQESAC/

The command run, should you want to repeat it (or, better still, emulate with a different query in future) was:

$ python /share/apps/slimsuite/tools/multihaq.py -seqin NSCUK81QUERY.fas -basefile tlr4\_example blast2fas="/share/data/babsgenome/annotation/Nscutatus.k81L500.2017-08-18.busco.fas,/share/data/babsgenome/qfo/qfo\_eukaryota.2017-04.fas,/share/data/babsgenome/uniprot/uniprot.sauropsida.2017-09-07.fas" blastcut=200 i=-1 group=dup blaste=1e-10 haqdir=HAQESAC

Next, we can run HAQESAC _interactively_ on the file produced by this automated run:

$ python /share/apps/slimsuite/tools/haqesac.py -seqin /share/data/babsgenome/examples/HAQESAC/NSCUK81EOG090701X7.fas query=NSCUK81EOG090701X7 basefile=tlr4\_auto cleanup=F i=0

We can switch cleanup=F because we already know that the data has been cleaned up nicely. (If we really trust the output and purely want to rename seqeuences, we can switch saq=F paq=F too.)

**NOTE:**  All the output files will now be named according to basefile=tlr4\_auto, not the query (NSCUK81EOG090701X7.fas). This lets us perform multiple different runs with extra filters, if we wish.

**CHALLENGE:**  Use HAQESAC to rename the sequences in the three gene families and open up the alignment in AliView and the tree in MEGA. How do these compare to the alignment and tree you made above without the Sauropsida sequences?

![](RackMultipart20230102-1-ssjimi_html_92939a517937f46f.gif)

# 18.Snake Protein Annotation

## 18.1.Candidate Protein Selection

Part 2 of the bioinformatics practical is primarily a  **protein annotation**  exercise. You now have all the analytical tools required for the annotation of a snake protein. The final step is to select a candidate protein to annotate for your report.

For the report, you will start with a protein, gene or transcript of your choosing, and work through the annotation and analysis pipeline in **Section 23: Gene Annotation Workflow**. Note that not all questions and analyses will be relevant for your annotation project: some will depend on what kind of sequence you start with, whilst others will depend on the nature of the gene/protein you end up analysing.

The possible sources of a gene/protein to work with are:

1. BUSCO protein predictions. This is primarily validating the identity, checking the completeness, and analysing the evolution of the protein predicted by BUSCO.
  - Assembled tiger snake transcripts. Those who want a bit more a challenge can annotate an assembled transcript. This requires an additional step of generating the protein sequence prior to analysis, which may not correspond to an actual protein.
2. A candidate protein of your choosing from another organism. One good source of these is the venom proteins from the Uniprot animal toxin collection: [https://www.uniprot.org/program/Toxins](https://www.uniprot.org/program/Toxins). This is the most challenging starting sequence in terms of generating the snake protein sequence - you will need to use the search server from **Section 20**  to do this.

An overview of selecting a protein sequence of each type is given below. Note that you might need to try a few before you find one that you want to work with. Transcripts may lack open reading frames with homology to known proteins, whilst candidate proteins from other organisms may lack homologues in the snake genome. In either case, select a different transcript or query protein if it is proving difficult to generate a multiple sequence alignment of predicted orthologues.

**NOTE:** In principle, _any_ protein with a snake sequence and vertebrate homologues can be analysed. In reality, you will probably find some easier to interpret and write about than others, so **it is recommended that you perform preliminary analyses on several before choosing the one you want to write up.**

**You should pick one gene/protein/transcript for your entire report. **

## 18.2.Setting up your workspace

It is recommended that you make a new  **annotation/**  BABS3291 subdirectory and create a new directory for each candidate protein. This should be named:

annotation/YYYY-MM-DD.AccNum/

Where AccNum is the candidate protein identifier you are working on (e.g. TS10X1EOG090701X7).

## 18.3.Choosing a BUSCO genes to work on

The easiest protein to work with is one of the BUSCO predictions. This is because the protein sequence has already been generated by BUSCO, and you can be confident that it is in the snake genome. To make selecting a BUSCO protein easier, I have run a HAQESAC BLAST search and alignment cleanup (see  **Section 17** ) and copied the data here:

/share/data/babsgenome/haqesac/tiger10x/

Each BUSCO gene was searched against four databases:

- 10X1.2017-09-07.busco.fas = Tiger snake BUSCO genes
  - Species code: NOTSC
- 10X1.2017-09-14.busco.fas = Eastern brown snake BUSCO genes
  - Species code: PSETE
- 2017-09-16.prot.fas = Combined proteomes for four available snake genomes:

  - _Ophiophagus hannah_ = OPHHA
  - _Python bivittatus_ = PYTBI
  - _Thamnophis sirtalis_ = THASI
  - _Protobothrops mucrosquamatus_ = PROMU

- qfo\_eukaryota.2017-04.fas = Quest For Orthologues reference eukaryote proteomes.

The  **Top 50**  hits were retained for each BLAST search.

**NOTE: ** For speed, HAQESAC was also run to keep the  **Top 50 hits**  across all searches. As we have restricted our search datasets to selected species, this should be sufficient. However, remember that you don't have everything when interpreting your results.

**NOTE:**  These were run against an older version of QFO than you used for GOPHER. You may want to run GOPHER on your protein as well. Instructions for re-running HAQESAC are provided below. The biggest difference is that HAQESAC will include other members of a protein family in its alignments and trees, but it will take a lot longer than GOPHER to run.

### 18.3.1.Picking a candidate

There are 3093 BUSCO proteins with alignments are trees in /share/data/babsgenome/haqesac/tiger10x/. Choose a _random_ candidate to work on:

1. Pick a random number from 1-3093

2. Identify your candidate. You can do this using a combination of ls (list directory contents), head and tail. _e.g. _protein 488:

$ ls -1 /share/data/babsgenome/haqesac/tiger10x/\*.png | head -n 488 | tail -n 1

/share/data/babsgenome/haqesac/tiger10x/TS10X1EOG090701X7.png

**NOTE:**  This is TLR4 again, so pick another one for your report unless you get desperate!

You should have four files for this protein:

$ ls -lrth /share/data/babsgenome/haqesac/tiger10x/TS10X1EOG090701X7.\*

-rw-r--r--. 1 z3452659 unsw 2.8K Sep 17 20:15 /share/data/babsgenome/haqesac/tiger10x/TS10X1EOG090701X7.nwk
-rw-r--r--. 1 z3452659 unsw  25K Sep 17 20:15 /share/data/babsgenome/haqesac/tiger10x/TS10X1EOG090701X7.fas
-rw-r--r--. 1 z3452659 unsw 120K Sep 17 20:15 /share/data/babsgenome/haqesac/tiger10x/TS10X1EOG090701X7.png
-rw-r--r--. 1 z3452659 unsw  27K Sep 17 20:15 /share/data/babsgenome/haqesac/tiger10x/TS10X1EOG090701X7.log

**NOTE:**  If your protein does not have all four files, pick another one!

You then want to copy your four candidate protein files into the annotation directory you made, _e.g. _(from your BABS3291 prac main directory on the server):

$ cd ~/BABS3291/annotation/2017-09-18.TS10X1EOG090701X7
$ cp /share/data/babsgenome/haqesac/tiger10x/TS10X1EOG090701X7.\* .

Have a quick look to see if you like the look of it based on the alignment and tree. Try another if you do not!

## 18.4.Choosing a transcript ORF to annotate

For those after more of a challenge, you can also annotate a _de novo_ assembled RNA-Seq transcript. These are available in:

/share/data/babsgenome/transcripts/trinity/

- /share/data/babsgenome/transcripts/trinity/Nscu.meta.trinity.fasta = the full Trinity assembly, but this will include many errors with fragmented or missing ORFs.
  - 371,857 sequences
- /share/data/babsgenome/transcripts/trinity/Nscu.babs3291.trinity.fasta = the subset of transcripts with at least one ORF \>= 200 amino acids, and therefore most likely to be from a real gene.
  - 41,947 sequences
- /share/data/babsgenome/transcripts/trinity/Nscu.meta.200aa.fas = translated protein sequences for the ORFs from the above file.
  - 49,553 sequences

The easiest course of action is to use one of the protein sequences directly. For those wanting more of a challenge (and bonus marks towards higher grades), you can extract one of the transcripts and work through **Section 19 - Transcript annotation**.

In each case, you can use  **head**  and  **tail**  to pull out a random sequence. Each sequence is present on two lines - the description line and the sequence line. Pick a random number from 1 to the total number of sequences indicated above for the relevant file (example below).  **Double ** that number (two lines per sequence) and then pull out that many lines from the head of the file. Then pull out the last two lines to get your sequence.

### 18.4.1.Example ORF sequence to annotate

There are 49,553 ORF sequences. I randomly choose ORF 30,010. I need to pull out the first 60,020 lines and then the final two lines to get my sequence:

$ head -n 60020 /share/data/babsgenome/transcripts/trinity/Nscu.meta.200aa.fas | tail -n 2

\>trin\_NOTSC\_\_NSCUMETAT208262.RF-3.ORF1 TRINITY\_DN46334\_c0\_g1\_i3 len=1739 path=[1717:0-29 9998:30-53 1748:54-146 1841:147-147 1842:148-170 1865:171-188 1883:189-208 1903:209-279 1974:280-303 1998:304-314 2009:315-365 9999:366-389 2084:390-452 2147:453-453 2148:454-476 2171:477-477 2172:478-484 9996:485-508 2203:509-622 2317:623-643 2338:644-659 2354:660-664 2359:665-665 2360:666-683 2378:684-689 2384:690-747 9993:748-771 2466:772-851 9997:852-875 2570:876-917 2612:918-925 2620:926-941 2636:942-945 2640:946-952 9994:953-976 2671:977-977 9995:978-1001 2696:1002-1046 2741:1047-1061 2756:1062-1070 2765:1071-1135 2830:1136-1337 9992:1338-1361 3056:1362-1433 3128:1434-1435 3130:1436-1455 3150:1456-1473 3168:1474-1530 3225:1531-1550 3245:1551-1551 3246:1552-1559 3254:1560-1574 3269:1575-1583 3278:1584-1603 3298:1604-1626 3321:1627-1674 3369:1675-1695 3390:1696-1738] [-1, 1717, 9998, 1748, 1841, 1842, 1865, 1883, 1903, 1974, 1998, 2009, 9999, 2084, 2147, 2148, 2171, 2172, 9996, 2203, 2317, 2338, 2354, 2359, 2360, 2378, 2384, 9993, 2466, 9997, 2570, 2612, 2620, 2636, 2640, 9994, 2671, 9995, 2696, 2741, 2756, 2765, 2830, 9992, 3056, 3128, 3130, 3150, 3168, 3225, 3245, 3246, 3254, 3269, 3278, 3298, 3321, 3369, 3390, -2] Length=367
MASAKVKMTKNKDNIPHELESQFILRLPSEYASTVRRAVQSGSVNLKDRLTIELHGKGTTSADGRHGIVRVDQVPLAAKLVDLPCTMESLKTIDKKTFYKTADICQMLVCTVDGELYPPLEEPSVSTDARANKKKDKDREKKFIWNHGITLPLKNVRKRRFRKTAKKKYIESPDVEKEVKRLLSTDAEAVSVRWEVIAEDETKEAENHGVLTGLDISSPGMTGHKQGHGSSERDELRELFNEISSSSSDEDERDHHDDEDLNVMDTEEDLERRLQGKLNESSSQQQENEGSSQIAIGIQKQIDNLKGKLQETQERRKRQEDLIMKVENLALKTRLQAVLDEFKQQEDREKQQLTSLQEQLEALMEK\*

» As you can see, these trinity transcripts have long unwieldy description lines - feel tree to clean these up for your downstream analysis. (But make a note of it somewhere.)

## 18.5.Choosing a GeMoMa prediction to search against

The BABS genomes have been updated with Oxford Nanopore Technologies (ONT) long-read data since the above data were generated. Version 2.4 of the assemblies have also been provided on the server. These were first assembled from the ONT data using a program called Redbean. Next, sequence quality was improved by polishing with both ONT long reads (using Racon+Medaka) and 10x linked reads (with Pilon), before scaffolding with the 10x linked reads. Finally, an in-house program (Diploidocus) was used to try to remove "haplotigs" (where both diploid copies end up in the haploid assembly) and low quality sequences. This assembly was then annotated using a program called GeMoMa, which uses reference genomes and sequence homology to predict protein-coding genes. The predictions are available on the teaching server:

- /share/data/babsgenome/annotation/tigersnake.v2.4.gemoma.faa = predicted tiger snake proteins (67,903 isoforms)
- /share/data/babsgenome/annotation/ebrownsnake.v2.4.gemoma.faa = predicted brown snake proteins (50,452 isoforms)

To pick a random snake protein, pick an even number between 2 and 135806 (tiger snake) or 100904 (brown snake) and use the head and tail command as for the transcript files, e.g.

head -n 67902 /share/data/babsgenome/annotation/tigersnake.v2.4.gemoma.faa | tail -n 2

## 18.6.Updated protein search databases

In addition to new protein annotations, there are several additional files that you can search against for orthologues or other homologues:

- /share/data/babsgenome/qfo/qfo\_eukaryota.2020-04.fas = Updated eukaryotic QFO proteomes
- /share/data/babsgenome/qfo/qfo\_vertebrata.2020-04.fas = Updated vertebrate QFO proteomes
- /share/data/babsgenome/proteomes/snake\_proteomes.2020-07-16.fas= Updated snake proteomes, now with proteins from 12 different snake proteomes (predicted, see below).

QFO eukaryotic data and the updated snake proteomes have been combined into a new orthdb for GOPHER or HAQESAC searches:

- /share/data/babsgenome/gopherdb/orthdb.2020-07-16.fas = qfo\_eukaryota.2020-04.fas + snake\_proteomes.2020-07-16.fas

Finally, there is an expanded version that has BUSCO predictions for v1.x genomes and the v2.4 GeMoMa predicted protein annotations:

- /share/data/babsgenome/gopherdb/orthdb.2020-07-16plus.fas

For GOPHER, I recommend trying the orthdb.2020-07-16.fas first, as it only has one version of each tiger/brown snake protein. However, it is likely that some proteins are missing from this annotation. For HAQESAC, which can better deal with paralogues and variants, I recommend using the orthdb.2020-07-16plus.fasfile.

**NOTE:** It doesn't "matter" which data you use for your project. Using the latest data will show the ability to apply your learning, but might also be a bit more difficult to interpret. The golden rules are (1) work within (but preferably expand) your comfort zone, and (2) make sure that you interpret your results in the context of the data you have used. You can pick up a few marks by generating better data, but the bulk of the marks are in the presentation and interpretation of data. (And there are many different ways to pick up the marks.)

### 18.6.1.Snake species in snake\_proteomes.2020-07-16.fas

The new snake proteomes in snake\_proteomes.2020-07-16.fas include some with species codes we had to invent as they were not in UniprotKB taxonomy at the time. Ordered by species code, the snake species in this file are:

- BOACO: 19,178 sequences = Boa constrictor v1.0 (_Boa constrictor_)
- CROVV: 17,480 sequences = Prairie rattlesnake v1.0 (_Crotalus viridis viridis_)
- HYDCUR: 27,521 sequences = Shaw's sea snake v1.0 (_Hydrophis curtus_)
- NAJNA: 31,036 sequences = Indian cobra v1.0 (_Naja naja_)
- NOTSC: 31,232 sequences = Mainland tiger snake v1.1 [NCBI annotation] (_Notechis scutatus_)
- OPHHA: 18,445 sequences = King cobra v1.1 (_Ophiophagus hannah_)
- PANGU: 10,917 sequences = Corn snake v1.0 (_Pantherophis guttatus_)
- PROFL: 35,815 sequences = Habu v1.0 (_Protobothrops flavoviridis_)
- PROMU: 22,660 sequences = Taiwan Habu v1.0 (_Protobothrops mucrosquamatus_)
- PSETE: 31,677 sequences = Eastern brown snake v1.1 [NCBI annotation] (_Pseudonaja textilis_)
- THAEL: 30,876 sequences = Western terretrial garter snake v1.0 (_Thamnophis elegans_)
- THASI: 25,180 sequences = Garter snake v1.0 (_Thamnophis sirtalis_)

**NOTE:** These annotations come from various sources, so the quality will vary. Snakes probably have around 20k proteins so many more than this indicates duplicates and/or isoforms, whereas a lot fewer indicates incomplete assembly/annotation.

**NOTE:** Some of these genomes have since been improved and updated in NCBI and better annotation may be available online. Additional snake genomes have also been sequenced and released since this file was compiled.

## 18.7.Optional: using HAQESAC for a first pass annotation

**NOTE: This is an optional activity for students who are feeling more confident with UNIX. If it seems confusing, do not feel that you have to attempt it.**

Even if you have not worked through  **Section 17** , you might want to use HAQESAC to generate an automated alignment and tree for an initial look at a given set of proteins, as was performed for the BUSCO candidate proteins. For this, we can use the combined search database we used for GOPHER:

$ python /share/apps/slimsuite/tools/multihaq.py -seqin accnum.fasta -basefile haqesac\_auto blast2fas="/share/data/babsgenome/gopherdb/orthdb.2020-07-16.fas" blastcut=50 i=0 group=dup blaste=1e-10 haqdir=HAQESAC

Replace the highlighted settings for seqin and basefile with your sequence file name and whatever you want the output to be named after. Note that the orthologue database for this search has also been updated compared to the default files provided in **Section 18.3.1**. The details of this file are found in **Section 18.5** , along with some other files that you can search against, depending on the focus of your analysis. You may also want to increase the number of homologues above 50 for more detailed protein family analysis.

**Warning:**  this may take a while to run, so don't start it just before you want to go home! (Unless you are using **screen** – see **Section 2.3.7**.)

If you have worked through  **Section 17** , you can then run HAQESAC interactively to tidy it up. Enter the HAQESAC directory and run something like:

$ python /share/apps/slimsuite/tools/haqesac.py -seqin accnum.fas query=accnum basefile=accnum\_auto cleanup=F i=0

Where accnum is the accession number of your protein. If you know the gene at this point, you can use this for the basename instead. We can switch cleanup=F because we already know that the data has been cleaned up nicely. (If we really trust the output and purely want to rename sequences, we can switch saq=F paq=F too.)

**NOTE:**  All the output files will now be named according to basefile=accnum\_auto, not the query (accnum.fas). This lets us perform multiple different runs with extra filters, if we wish.

# 19.Annotating a snake transcript (Advanced)

To annotate a transcript, you just need to go through an additional step to work out the protein sequence encoded by the transcript prior to following the rest of the annotation protocol.

The transcripts can be found in:

/share/data/babsgenome/transcripts/trinity/Nscu.babs3291.trinity.fasta

The instructions for picking a transcript are in  **Section 18**. Because a transcript might not have a decent protein sequence, it might be worth pulling out a few into a file to analyse further, before picking one to annotate.

You are welcome to use whatever method you see fit to discover the correct open reading frame (ORF) for your protein, but the easiest thing to do is to run your transcript through an online tool like ORFfinder: [https://www.ncbi.nlm.nih.gov/orffinder/](https://www.ncbi.nlm.nih.gov/orffinder/). It is a good idea to restrict your ORF to starting with an ATG in the first instance, but you may want to remove this restriction if your sequence alignment analysis indicates that the beginning of the protein is missing.

Once you have identified the correct ORF, you want to make a fasta file of the protein sequence. Do this in a text editor and make sure that you give it a sensible name that will be compatible with SLiMSuite (see  **Section 8**.). After this, treat it like a BUSCO protein: find homologues, make an alignment and trees etc.

## 19.1.Using BLASTX to help choose a transcript

As mentioned, one potential issue that you might pick a poorly assembled, non-coding, or "noisy" transcript, lacking a protein sequence. Rather than spending time extracting ORFs and then discovering a lack of homologous proteins, you can use a  **blastx**  search first at the NCBI BLAST site ([https://blast.ncbi.nlm.nih.gov/Blast.cgi](https://blast.ncbi.nlm.nih.gov/Blast.cgi)) to show you whether there are likely to be any protein-coding sequences. You can BLAST a few transcripts at once to save a bit of time too. If there are hits, you can then select a transcript to run through ORFfinder to get the full ORF.

**NOTE:**  It is also possible that a transcript will have a sequence error in the form of a base error or even an indel. This could destroy the ATG start codon, create a premature stop codon, or even cause a frameshift. This in turn might mean that a single protein sequence is split over several ORFs. You should be able to identify such situations by a combination of protein translation, BLASTX and multiple sequence alignments. If you need to extend an ORF, you might find it useful to use a general translation tool like ExPASY Translate: [https://web.expasy.org/translate/](https://web.expasy.org/translate/). If you need to, use a text editor to splice together two different reading frames - make sure you make a note of what you have done to make the protein sequence.

![](RackMultipart20230102-1-ssjimi_html_cd0c855dca9f5d03.gif)

For this part of the prac, we are using an in-house server to perform sequence searches of the snake genomes and then analyse the results in an online genome browser.

**NOTE: ** It takes a while to run jobs on the server.  **Read through the search instructions but do not actually run any new jobs for this Activity**  - results have been pre-computed to look at:

1. Protein search using the  **Venom prothrombin activator notecarin-D1**  [_Notechis scutatus scutatus_] protein sequence from Uniprot: FAXD1\_NOTSC (P82807).
  - [http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700016](http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700016)
2. Coding sequence from BUSCO EOG090701X7 predicted transcript.
  - [http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700017](http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700017)
3. Full-length Trinity-assembled tiger snake transcript.
  - [http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700018](http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700018)

**NOTE: ** This server is still in development, so please report any unexpected behaviour. Currently, only protein sequence searches are fully supported, although transcript search support is in development. (The transcript searches themselves are executed fine but some of the results parsing and downstream files may not currently behave correctly.) For unknown reasons, these links do not appear to work when the VPN is connected.

# 20.Sequence searches of snake genomes

To search the snake genomes for specific DNA or protein sequences, a custom web sever has been set up for BABS3291 at [http://www.slimsuite.unsw.edu.au/servers/babs3291.php](http://www.slimsuite.unsw.edu.au/servers/babs3291.php):

![](RackMultipart20230102-1-ssjimi_html_827c8d72107d687.png)

This server contains links to the Apollo genome browsers for the BABS Genome species, as well as a basic search tool.

## 20.1.Protein sequence searches

The most common sequence to search with is a protein sequence:

1. Select the **Search Genome** (default, tiger snake) to search.
2. Choose a **WebApollo ID** that matches the search genome. This will not affect the search itself but is used for formatting output links to the relevant genome browser.
3. Optionally set a password. This will be needed to retrieve your search results. It is recommended to leave blank.
4. Select **Protein sequence** from the drop-down box (the default).
5. **Paste fasta format sequence(s)** into the text box. The server can take a maximum of 10 sequences to search at once.
6. Click **Run Apollo Search**.

**NOTE:** In this prac, we will use exonerate. Feel free to try one of the BLAST programs if you want a quicker, cruder answer. The server will return the top 10 hits by default. This can be reduced to speed up searches.

![](RackMultipart20230102-1-ssjimi_html_f8d1abd0ab4ea0.png)

This will generate a server job and put it in the run queue:

![](RackMultipart20230102-1-ssjimi_html_4e39ef3bcab5dad.png)

Save the Job ID and/or URL to look up the results later. Server output is covered in section 2.

## 20.2.Transcript searches

Searching with a transcript is fundamentally the same. Just select **DNA transcript sequence (mRNA/EST)** instead of **Protein sequence** from the drop-down box:

![](RackMultipart20230102-1-ssjimi_html_f34171002fc3412f.png)

If the transcript is just the coding region, you can select **DNA coding sequence (in-frame)** instead:

![](RackMultipart20230102-1-ssjimi_html_75e22f8ae3cd0b21.png)

## 20.3.Server outputs

Output for the search server is fairly crude, and takes the form of several results tabs (e.g. [http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700016](http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700016)):

![](RackMultipart20230102-1-ssjimi_html_b93234c81e49722c.png)

The main results to look at are:

- **html** contains a summary table of the hits, with links out to the scaffolds in the Apollo browser.
- **local** contains a summary line for each local alignment chunk. This is useful for seeing a summary of how similar each alignment chunk is by comparing the **Length** and **Identity** fields.
- **locgff** contains the hits in GFF3 format, which can be imported into the Apollo browser. This tab contains a URL link to a plain text version of the file, which should be saved if you want to load the mapped feature into Apollo.
- **alignment** contains the alignment returned by exonerate. This is useful for an initial look to see how similar the query and the hit are. If the query sequence comes from the genome being searched, this should be an extremely similar hit.
- **prothits** for protein searches contains each protein hit. This can be useful when trying to reconstruct the predicted snake protein. ( **NOTE:** the hit sequence parsing does not currently work consistently for transcript searches.)

The first place to look it the **html** tab. This will summarise the top hits and give you an indication of whether any close matches have been found. Pay particular attention to the **Identity** versus **Length** (how similar is the sequence), and the **QryLen, QryStart** and **QryEnd** (how much of the query sequence was in the alignment):

![](RackMultipart20230102-1-ssjimi_html_c8c19b0d3ed858e7.png)

## 20.4.Checking Hit Quality

The two outputs to look at for checking the initial quality of the sequence hit, are the **alignment** and **local** tabs. The **alignment** tab shows the actual exonerate alignment:

![](RackMultipart20230102-1-ssjimi_html_36fc402294d8d0ab.png)

Each exon is summarised as a local alignment in the **local** tab:

![](RackMultipart20230102-1-ssjimi_html_81ffbc3d6853d803.png)

**NOTE:** Exonerate is much more precise but less sensitive than BLAST. It will give you good alignments of the top hits in the genome but it is not a comprehensive search tool that will find _all_ regions of homology in the genome. As such, an exonerate search with a single query sequence will not be sufficient for a detailed protein family analysis, especially without increasing the number of top hits returned.

## 20.5.Retrieving predicted protein sequences

If you have searched with a candidate protein from another species, you may want to extract the predicted protein sequence for further analysis. This can be accessed from the **prothits** tab in fasta format:

![](RackMultipart20230102-1-ssjimi_html_d99f894a0732d189.png)

To get a plain text version that is easier to copy and paste from, add **&rest=prothits** to the URL ([http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700016&rest=prothits](http://rest.slimsuite.unsw.edu.au/retrieve&jobid=21072700016&rest=prothits)):

![](RackMultipart20230102-1-ssjimi_html_3d788c40f8d152ce.png)

This plain text page can also be saved directly to a text file.

**NOTE:** You can similarly get outputs of the other tabs as plain text by adding the relevant &rest=X to the URL, e.g. &rest=locgff.

# 21.Analysing genome and gene prediction quality

At this point, you should one or more tiger snake proteins aligned to other vertebrate proteins. From this, you may have identified regions or amino acids in the protein that look different in your tiger snake versus its orthologues. These could be otherwise conserved residues that have changes in the snake protein, or regions that appear to be missing/extra in the snake protein.

The question then becomes:

**Are these real biological differences that you see, or sequencing/assembly artefacts?**

To address this question, we generally do the following:

1. "Map" the raw sequencing reads onto the genome assembly. For this, we have used a program called BWA mem. This matches the sequence of the raw Illumina reads to find where they belong on the genome, allowing for some mismatches to account for sequencing errors and/or polymorphism.
2. Look at the region containing the predicted gene to see if the reads appear to be well-mapped and support the consensus sequence of the assembly. We are going to use a web-based Apollo genome browser for this part of the task.
3. Look at whether there is additional supporting evidence for the gene and/or its structure based on RNA-Seq, transcript or homologous protein evidence.

**NOTE: ** It is beyond the scope of this prac to provide extensive details of how to do this, and it is not required to complete the Prac 2 report. However, because it requires depth of understanding, it is a great way to get one of the higher grades. Here, we will just outline the general process. If you want to try this out and need to get help as you work through your own sequences, please ask!

## 21.1.Opening results in the Apollo Genome browser

The real power of the search tool comes from using the results to directly query a particular region of the genome assembly in the Apollo browser. The easiest way to do this is through the **html** tab:

![](RackMultipart20230102-1-ssjimi_html_c8c19b0d3ed858e7.png)

Each **Hit** is a scaffold of the assembly, hyperlinked to the browser. Click on one of the hits (usually the top hit is of most interest) and Apollo will launch in another browser tab. If you are not already logged on, you will need to do so:

![](RackMultipart20230102-1-ssjimi_html_55fbfa1b8a26366f.png)

The username is **babs3291@unsw.edu.au** and the password in **BABS3291**. The Apollo browser should then jump to the relevant scaffold and region (next page). If it does not, make sure that you do not have any Apollo browser windows open already on a different organism. If you do, switch to the tiger snake and try again.

**NOTE:** You may not have the same tracks displayed as below when you first log on. These can be altered using the **Tracks** tab on the right-hand side of the browser. These tracks will be explained in LabArchives. Navigating the browser is hopefully quite intuitive, but click on **Help** if you want to learn more. Specific questions can also be posted to the Moodle forum.

![](RackMultipart20230102-1-ssjimi_html_21a1e7c4cdfcfb0b.png)

## 21.2.Importing annotation

One of the main roles of the genome browser is to enable visualisation, assessment and improvement of gene/protein annotation. Exonerate hits from the web search tool can be imported as new tracks using the **locgff** output.

![](RackMultipart20230102-1-ssjimi_html_94c8abde0546922c.png)

Click on the link to the gff3 file and save it to your local machine:

![](RackMultipart20230102-1-ssjimi_html_614aeb11763a1cea.png)

Then, in the Apollo browser, **File »**** Open track file or URL**:

![](RackMultipart20230102-1-ssjimi_html_4be76ec80d291037.png)

In the dialogue box, **Select Files…** and open the file you have saved. Give your new track a sensible **Name** so that you can easily recognise it later, then click **Open** :

![](RackMultipart20230102-1-ssjimi_html_39eba2d9ba8e204.png)

Your new track will now appear in the browser window, allowing you to compare your annotation to other sources of evidence.

![](RackMultipart20230102-1-ssjimi_html_5620a84989ded57b.png)

Try importing the FAXD1 GFF3 file into Apollo as a track. Name the new track "FAXD1-zID", where zID is your zID. (This is in case of possible conflicts between students as everyone is using the same log in.)

Explore the different Tracks in the browser

**NOTE:**  This browser is a new tool for UNSW, which is under development. As with a lot of "bleeding edge" research tools, there are still a few kinks to be ironed out. We are also unsure of how performance will scale if everyone accesses the server at the same time. If you experience performance difficulties, please try again later.  **Completion of this Activity is not required for lab credit or successful submission of the Part 2 Report.**

![](RackMultipart20230102-1-ssjimi_html_442029be35281f6b.gif)

# 22.BABS3291 Prac Assignment

## 22.1.Assignment submission

Your assignment should be submitted in **an electronic format (Word or PDF)** uploaded via Moodle to the **BABS3291 Bioinformatics Practical Report** Turnitin Assignment in the **Assessment** section. The deadline for this is **14:00 on Friday 22 April 2022**.

**NOTE:** This file will be run through the Turnitin plagiarism software. There is nothing to worry about if you have not plagiarised anything! There are always some short matches – particularly to paper names etc. – and scores alone are not used for any penalties. For minor cases, any plagiarised passages will not be marked. Major cases will be reported as possible academic misconduct and may be subject to further penalties.

**NOTE:** Your LabArchives Notebook is also part of your assessed submission. It is expected that all data used in the final report can be traced back to its source via the relevant information in the Appendix (see below) and LabArchives.

### 22.1.1.Word limits and penalties

There is **no overall word limit** for this assignment, but marks will be awarded for **concise answers**. The abstract and conclusions sections do have word limits (see below). There will be a **late submission penalty of 10% per day** without appropriate special considerations.The assignment is worth 30% but will be marked on a standard 0-100% scale. Any penalties will be applied to the 100% scale.

## 22.2.Project write up

Assessment for this project is in the form of a research report using the provided template. Main text should be **Times New Roman font size 12**. Headings and subheadings should be in **Arial**** font **. Figure legends should be** Arial font size 10 **. All margins should be** at least 2cm **. Each page should have a** header **featuring your** name and zID **and a** footer **with** page numbers**.

**NOTE:** Real journals are picky about fonts etc. so you need to pay attention. Find out how to use **Styles** in Microsoft Word if you don't already know. It will change your life. Using the provided template as a starting point will also make your life easier.

### 22.2.1.Report structure

The report itself should be broken down into the following sections:

Title and Name

Provide an informative title for your research project. In one short sentence, this should summarise what you have looked at and/or found. Use real journal articles for inspiration. **Include your name under the title.**

Abstract

The Abstract of the manuscript must **not exceed 350 words** and should summarise what you have done, the main findings and potential implications. Minimise the use of abbreviations and do not cite references in the abstract.

Project Aim

One or two sentences explaining the main aim of your analysis. Usually, this will be to identify, annotate and/or characterise a protein or transcript.

Analysis

This is a combined methods, results and discussion section. It will be divided into sections, covering specific questions to answer whilst characterising your gene, protein or transcript. **Four** topics will each contribute 20% to the final mark. Not all topics are of relevance for all proteins. You may complete more than four, in which case the best four marks will be used.

Analysis should be presented as concise methods, clear figures (with legends) and a short discussion of what the results mean. **You do not need to show every result you generated** if they do not add to answering a given question of the data. Also, **you do not need to reproduce results in the order that they were generated**. Order your results to maximise the flow of the narrative you are telling through the data, using the questions as guidelines.

Conclusions

**Max 250 words.** This should state clearly the main conclusions of the research and give a clear explanation of their importance and relevance. You may also highlight the limitations of your analysis. Try to include some suggestions of the next step in analysing/annotating your chosen sequence.

References

**All references,** including textbooks, must be accurately cited. You may choose your citation format, but be consistent. I recommend author-date formatting rather than numbered references, as this is generally clearer and you are less likely to make mistakes following insertions of text _etc._

If you have trouble finding the appropriate references for programs and databases, please post it on the Moodle forum.

**NOTE:** Citing lectures/tutorials should be a last resort. If you want to include something interesting, try to find an actual publication that supports that view. If you feel that you _must_ cite lectures/tutorials to support a statement, refer to them as a "personal communication", _e.g._ "(Edwards RJ, personal communication)", and do _not_ include them in your list of references. The snake data itself can be cited in text as "(Edwards RJ, unpublished data)."

### 22.2.2.Writing methods

Methods should include the design of the study, the type of materials involved, a clear description of all comparisons, and the type of analysis used, to enable replication. Describe clearly but **concisely** what you did, the data, programs and settings you used, how the analyses were designed. Remember, the methods are to enable reproduction of the **science** , not an exact step-by-step reconstruction of your work. Think about what is important information (e.g. program settings) and what is not (e.g. which program you used to manually edit a file or copy data). Detailed information will be available in your LabArchives entries if they are ever needed. Sometimes you cannot provide enough details for someone to literally repeat your work, particularly when manual decisions/edits have been made. In these circumstances, simply draw attention to where there was manual intervention and make the data available – in this case, your data will be available on the server as indicated in the appendix.

Your methods should include the accession numbers of all key proteins in your report and the date that data was downloaded. Details of the data on the server will be provided on LabArchives.

In principle, methods should be the easiest bits to write. In practice, it is often the one that gives people trouble. Here are some tips to help. (I've left it to you to find the citations marked by "[ref]".)

Do:

- Cite databases and programs using published papers where possible. Most resources will have some kind of "How to Cite" information. Failing this, search PubMed and/or try a Google search.
- Include the version numbers of programs/databases where possible and the date of any downloads.
- Include the settings selected for a program. If the program was run with default settings, say so.
- Keep it concise.

Don't include unnecessary details like:

- Which text editor you used to delete sequences or edit sequence names.
- How data was transferred on/off the server.
- Step-by-step instructions of _how_ to do a particular step.

### 22.2.3.Appendix

In addition, your report should contain an appendix listing where to find the data on the server.

## 22.3.Assessment criteria

Overall, the bioinformatic prac Part 2 report is worth **30%** of the BABS3291 mark. It will be marked out of 100%:

- 10% abstract, project aims and conclusion
- 10% general presentation (including reference formatting)
- 4 x 20% research topics. There are two compulsory and four optional topics. If more than four are answered, the best four grades will be used. (If using a BUSCO protein, you will probably want to do a fifth.)

Good answers to all of the questions in a section will be required for full marks. A pass grade can be achieved by answering the core elements of each section.

### 22.3.1.Research question assessment

Research question sections will be assessed on:

- The design of the analysis.
  - _Have you communicated a clear research question?_
  - _Are you analysing the right data? Have you selected sensible proteins and species?_
  - _Are the methods clear and appropriate?_
- Presentation of the data in a scientific style.
  - _Have you been_ _ **concise** _ _and clear?_
  - _Are your figures clear, well labelled and correctly cited in the text?_
  - _Are the references correctly cited?_
- Quality of the results and evidence of vigorous endeavour.
  - _Have you gone beyond the bare minimum to answer your question?_
  - _Have you returned_ _ **quality** _ _results – not quantity?_
- Ability to understand and interpret your data.
  - _Have you picked out the key points? (Remember your question.) Have you been critical of the data and methods? Have you included the important and_ _ **relevant** _ _data/methods?_

**NOTE:** You may lose marks if data cannot be found when I look for it!

# 23.Gene Annotation Workflow

Part 2 of the bioinformatics practical is primarily a **gene annotation** exercise. You will start with a protein, gene or transcript of you choosing, and work through the annotation and analysis pipeline laid out below, using resources from appropriate activities in previous pracs to guide you.

**IMPORTANT:**  Make sure that you save all your files appropriately and document things clearly in **as you go** _. _You will need to have this information for the protein you select for your write up.

The possible sources of a gene/protein to work with are:

1. BUSCO protein predictions. This is primarily validating the identity, checking the completeness, and analysing the evolution of the protein predicted by BUSCO.
2. Assembled tiger snake transcripts. Those who want a bit more a challenge can annotate an assembled transcript. This will require an additional step of generating the protein sequence prior to analysis.
3. A candidate protein of your choosing from another organism. One good source of these is the venom proteins from the Uniprot animal toxin collection: [https://www.uniprot.org/program/Toxins](https://www.uniprot.org/program/Toxins). This is the most challenging starting sequence in terms of generating the snake protein sequence.

You should include the source and general question in your project aims. Note that transcripts may lack open reading frames with homology to known proteins, whilst candidate proteins from other organisms may lack homologues in the snake genome. In either case, select a different transcript or query protein if it is proving difficult to generate a multiple sequence alignment of predicted orthologues.

**You should pick one gene/protein/transcript for your entire report. It is recommended that you perform preliminary analyses on several before choosing the one you want to write up.**

**NOTE:** You will be analysing data and asking questions that have not been looked at before. The important thing, which will be assessed, is whether you communicate coherent analyses and relevant results. You will not be graded for finding the "right" answer as there may not be one, although you will lose marks for jumping to the wrong conclusions, or failing to argue why your conclusions are correct _given your data_.

**NOTE:**  Not all questions and analyses will be relevant for your annotation project: some will depend on what kind of sequence you start with, whilst others will depend on the nature of the gene/protein you end up analysing. There will also be some overlap between sections/questions. The **Predicted snake protein sequence** and **Functional protein assignment/annotation** sections are compulsory for all sequences. Your grade will be based on the  **Functional protein assignment/annotation**  section plus the best  **three****  **other sections of this workflow. (It is not required to complete all sections.)

## 23.1.Predicted snake protein sequence [\*compulsory]

If you are working with a BUSCO protein, this section is simply the BUSCO prediction (description and sequence). If you are starting with a transcript or candidate protein from another organism, this should include the predicted protein sequence and details of how the sequence was predicted. Details of how to choose/predict a snake protein sequence to work on can be found in  **Section 18 -** Snake Protein Annotation. If working on a raw transcript, you will want to refer to  **Section 19 -** Annotating a snake transcript (Advanced). If using a candidate protein from another species, look at the  **prothits**  output for  **Section 20 -** Sequence searches of snake genomes.

**NOTE:**  Following analysis of the multiple sequence alignment and/or the source data/assembly ( **Section 21** - Analysing genome and gene prediction quality), you might want to modify the protein sequence that you originally obtained. If you use any modified sequences for any analyses, make sure they are also provided, along with a description of how they were generated. (You can cross-reference other analyses.)

## 23.2.Functional protein assignment/annotation [\*compulsory]

The primary task is to functionally annotate a snake protein. Use one or more of the approaches from earlier pracs to generate a multiple sequence alignment and phylogenetic tree of predicted orthologues.

### 23.2.1.Multiple Sequence Alignment

Include a figure of a multiple sequence alignment ( **Prac 3** ). Comments on the quality. (Do your sequences align well in nice blocks, or are there many insertions and deletions?) Does the candidate appear to be full-length and complete? If not, where does data appear to be missing, or extra.

### 23.2.2.Phylogenetic tree

Include a figure of your most confident phylogenetic tree ( **Prac 2** ). (This may be based on more detailed analyses in a later section.) Based on the phylogeny and annotation of homologues, what does this candidate appear to be? If this is a BUSCO prediction, is BUSCO right?

### 23.2.3.Domain composition

What is the domain composition of the protein? You can identify domains a number of ways but four of the best are:

1. Perform a BLAST search on the NCBI website ([https://blast.ncbi.nlm.nih.gov/Blast.cgi](https://blast.ncbi.nlm.nih.gov/Blast.cgi)). This has built-in domain prediction.
2. Pfam sequence search: [https://pfam.xfam.org/](https://pfam.xfam.org/). Pfam is a dedicated domain database and will provide much more information on the strength of domain hits, in addition to functional annotation of the domains.
3. Identify a human or mouse orthologue and look at its annotated domain composition in Uniprot.
4. Perform a sequence search at the SMART database: [http://smart.embl-heidelberg.de/](http://smart.embl-heidelberg.de/). This is probably my favourite. In addition to giving you a nice graphical representation of your domain structure (good for your report), SMART also gives you tools to investigate other proteins with the same domain architecture. This might help you identify whether your protein is part of a protein family.

Is the domain composition consistent with the protein's annotation? If annotation is lacking, what functions to the domains suggest?

### 23.2.4.Gene duplications and protein families

Based on your homology searches (including as part of domain analysis), is the protein part of a protein family? If so, are you confident which family member it is? (Does the tree have good support?) A more detailed analysis can be carried out as part of **Section 23.5**.

## 23.3.Evolutionary conservation analysis

Analyse your MSA in AliView ( **Section 7** ). Using the previous multiple sequence alignment figure and other figures where appropriate (e.g. zoomed in on specific regions), comments on the apparent evolutionary conservation of this protein compared to (a) other snake genomes, and (b) vertebrates more widely. Are there any interesting or notable features of the snake protein that warrant further investigation?

### 23.3.1.Snake proteins

- Which of the other snake genomes also have this protein?
- Identify the regions of the protein that seem (a) highly, and (b) poorly conserved. How does this relate to the domain composition (above)?
- Are there any residues conserved across other snakes/vertebrates that are not conserved in the tiger snake?
  - If so, note them. They may be sequencing errors so will need to be checked at some point.
- Are there any other interesting or notable features of the snake protein that warrant further investigation?

### 23.3.2.Orthologue annotation

- Check which human and mouse proteins (if any) are orthologues. Look them up in Uniprot.

  - How well annotated are these proteins? What are the important regions/sites?
  - Does your snake protein have sequence aligning to the annotated regions?
  - Are there any obvious differences worth noting in these regions? Do any of the residues noted in the previous step fall in these regions?

### 23.3.3.Inferred protein evolution

- Use the ancestral state inference of a Maximum Parsimony tree ( **Prac 2** ) to step through the sequence and identify any amino acids that appear to have changed in the ancestral branch leading to the snakes and subsequently conserved.

![](RackMultipart20230102-1-ssjimi_html_50bf967e7ab710f1.png)

  - Are these the same or different to the residues identified previously from the alignment?
  - Are any of these important sites as identified in Uniprot orthologues?

## 23.4.Phylogenetic analysis

Use different phylogenetic inference methods ( **Prac 2** ) to check the robustness of your annotation and gain further insights into the evolution of the protein.

### 23.4.1.Phylogenetic robustness

Use MEGA to make UPGMA, Neighbour Joining, Maximum Parsimony and Maximum Likelihood trees

- Root the trees using outgroup known relationships of the sequences (e.g. protein family structure and/or species tree) if possible. Otherwise use midpoint rooting.
- Are your conclusions about the identity of your protein robust to phylogenetic method? If not, which do you trust and why?

### 23.4.2.Alignment quality

​Is the alignment quality having an impact on your tree? Make NJ trees with different gap treatment methods (partial/complete) and see if the tree topology is affected. Look at how "gappy" the alignment looks when assessing this.

### 23.4.3.Molecular clock analysis

The "molecular clock" hypothesis predicts that proteins will evolve at an approximately constant rate.  Do your proteins or families appear to be evolving in a clock-like fashion? (If so, you expect (a) mid-point rooting to match outgroup rooting; (b) UPGMA to give the correct topology; (c) distances from the root to the tips of a NJ tree to be approximately the same for all sequences.)

- Is the protein evolving in a reasonably clock-like fashion?

  - Do the UPGMA and NJ trees agree?
  - Are the root-to-tip distances similar for all proteins for NJ and ML trees?
  - Does mid-point rooting agree with outgroup rooting?
  - Are there any parts of the tree that concern you with respect to rate artefacts?

## 23.5.Protein family analysis

Many proteins are members of protein families. This can make functional inference tricky, as lineage-specific duplications and/or gene losses can affect rates of evolution and selective constraints. _If_ your protein is part of a protein family, you can analyse the family in more detail:

- Do there appear to be any duplications in the snake lineage since its divergence from mammals?
- How are different members of a protein family related to each other? In which order, and at which points in evolution, did they duplicate?
- Do different species return the same complement of proteins with the same relationships? For example, you could draw a tree of all the snake family members you have found (or a decent subset) and compare to all human or mouse family members.

**NOTE:**  To perform this analysis systematically on the BABS genomes requires searching the unannotated genome for candidate proteins, which goes beyond the prac analyses. It is therefore recommended that you use the combined information from our snakes and the four annotated snake proteomes if attempting this. You can infer protein family structure from an organism other than the tiger snake. It is then up to you whether you go hunting for all the family members in the snake genome ( **Section 20 -** Sequence searches of snake genomes).

## 23.6.Genome integrity, quality and evidence

Thus far, you have assumed that the protein sequence you have been working with is correct, and that any errors in interpretation are due to analytical errors. It is also possible that a poor-quality protein sequence, or particularly unusual evolutionary signal, reflects poor assembly quality. Use the BABS3291 Apollo server ( **Sections 20 and 21** ) to find your gene in the genome and check its integrity, quality and supporting evidence.

Use edited screen grabs from the Apollo server to support your answers. The easiest way to edit and annotate a screen grab is probably using PowerPoint - the screen grab can easily be cropped and then labels added. The final figure can then be exported as a graphic.

### 23.6.1.Gene/genome integrity

- Is the gene contained on a single scaffold?

### 23.6.2.Sequence/assembly accuracy

- Look at the mapped 10x read data. Are there any protein-coding parts of the gene that have poor read support?
- Zoom in to the sequence itself. Are any unusual variants identified in **Section 23.3** supported by the genome assembly sequence and mapped reads?

### 23.6.3.Supporting evidence

- What is the supporting evidence for the gene? Is there:

  - RNA-Seq read support?
  - Assembled transcript support?
  - Mapped snake and/or venom protein homologues?

### 23.6.4.Gene structure

- What is the exon structure of the gene? (Remember that if you are starting with a protein, there might be UTRs too.)
- How does this relate to:

  - the domain composition of the protein?
  - predicted homologous/orthologous proteins from other species

## 23.7.Custom research question

The above sections cover all of the analyses you are likely to perform. However, we do not want to stifle particularly creative students. If there is a specific question you want to research that does not easily fall within these categories, you may add a custom section. Examples of this include analysis of domain evolution in multi-domain proteins, _e.g._ one of:

- How did differences in domain composition arise? Gain and/or loss? Are gains from tandem duplication or insertion from another protein?
- Do different domains within a protein have the same evolutionary rates and/or history?

Check with the course coordinator before committing to a custom research question.

![](RackMultipart20230102-1-ssjimi_html_fe4bce7d7c3a2240.gif)

# 24.Appendix

## 24.1.Tricks and Tips

The **Tricks and Tips** from the Information boxes throughout the manual have been collected here for reference. For general tips if things don't work as expected, see **Section 2.3.5 -** What to do when things go wrong.

### 24.1.1.Using the UNIX server

**READ THIS IF YOU DON'T READ ANYTHING ELSE!**
 Unix has  **no undo**  function. If you  **delete or overwrite**  a file, it will be gone forever! As a result, you should:
 1.    Keep  **back up copies**  of important files.
 2.    Be  **very careful**  with the command rm ("remove", i.e. delete) and any commands to move/create files that might over-write something important (mv, cp and redirecting output with \> and \>\>).
 3.    Use  **rm -i**  to provide an additional safety check against rogue deletion.
 4.     **Make sure that you keep good notes. ** Ultimately, it should be fairly straight-forward to regenerate anything from the starting data, provided you have adequate records of how you made it in the first place. This is one of the primary goals of keeping a lab book.

**Logging on from outside UNSW.**
 To log on from outside UNSW, you will need to connect to the university virtual private network (VPN).
 See https://www.myit.unsw.edu.au/services/students/remote-access-vpn for more information.

**The importance of windows real estate.**
 One thing you will quickly learn is the importance of being able to see clearly what you are doing. This generally means making the Putty/Terminal window much bigger than it opens by default. Ideally, you want it wide enough to avoid long commands and/or screen output wrapping onto multiple lines. You also want to see as many lines as possible to keep track of the context of what you are doing, and to make sure that important messages (particularly errors) do not disappear off the top of the screen. The precise way to resize your window will depend on your computer/software combination, but seek some advice during a prac session if you cannot find out how to do it.

**NOTE:** You will also find life easier with a bigger monitor – use the biggest screen/resolution that you can, especially when working with anything graphical.

**Copying and pasting in Putty.**
 Copying and pasting in Putty is easy but can also be a bit frustrating. To copy text to the clipboard, simply highlight with your mouse. Highlighted text can now be pasted in the usual fashion. To paste text in Putty, simply  **right click**  the mouse.
**WARNING: ** Any text that you paste into Putty in this fashion at the command prompt will be interpreted and executed as a list of commands!

**zID and $USER**
 On the server, your username is your zID. A handy shortcut to this is the UNIX environment variable $USER. Where you see "zID" or "$USER" in commands and outputs throughout this manual, remember that this will be your zID when you run the commands. If a command fails, check you've not left a generic "zID" in there!

**Saving your session and sanity with screen.**
 Whenever doing anything that will take a while, it is recommended that you use a utility called "screen", which will maintain an active session even if you log out or your connection to the server is dropped. You can read more about screen **Section 2.3.7**** -****Using screen (Advanced)**. The core elements are:

1. To start a new screen called "myscreen": screen -S myname

2. To "detach" the screen so you can re-attach it later and pick up where you left off: ctrl+a » d

3. To re-attached the screen "myname" after logging back on: screen -dr myname

**Mastering commands with man pages. And Google.**
 Want to know more about a command and it's options? The man ("manual") command can be used to access documentation about UNIX commands (including man itself): $ man man

Use up and down arrows to scroll through text, or "q" to quit. Other UNIX programs will normally have documentation that is accessed by running that program with --help or -h.

Manuals and help output for commands can be quite long. It is often easier to Google "UNIX" and the command in question. Or: "How do I … in UNIX?"

**The command prompt.**
Remember that $ is the "command prompt" and we are using it to distinguish commands you type from "standard output" printed to the screen. If you include the $ when running a command, you will get an error like this: bash: $: command not found

**Directories, folders and paths.**
 Don't get confused if you see "directories" and "folders" referred to in various places with respect to file locations. These are the same thing. A "path" is just the full address of that file/folder/directory. Type pwd ("path of working directory") to see the path for the directory you are currently in - this is the same as would appear in the "address bar" in Windows or the "path bar" in OSX. The "full path" includes the leading / that marks the root of the directory structure, and every single directory level, e.g. /home/$USER/BABS3291-Jun22/analysis/. A relative path does not have the leading / and will be interpreted relative to the current working directory. This is explained more in the Unix and Perl Primer.

**Autocomplete: tab is your friend.**
 One of the most useful keyboard shortcuts on the terminal is the use of TAB to autocomplete file/directory names. Simply start typing a name and hit TAB and it will autocomplete until it reaches a point of ambiguity. For example, if you have example.txt and example.fas in the directory, ex + TAB will stop at example. – just type t or f and hit TAB again. Not only does this save time, it is a great way of checking that files are located and named the way you think.

**File permissions.**
 Files and directories have three types of access permission: read, write and execute (rwx). We won't worry much more about these now other than to say that if the instructions tell you to do something and you get a file permission error, please let Rich know. It probably just means that the permissions need to be changed to let you read that file or write to that directory.

**Unix and Perl Primer data.**
 When you are working through sections from Unix and Perl Primer for Biologists, it will refer to data in /Volumes/USB/ as it assumes that you are working off a USB drive. We have created an equivalent directory on the server. However, you will _not_ have write permissions for this directory. If you want to work through other exercises in your own time, you will need to copy the data into your own directory. Ask if you need help with this.

### 24.1.2.LabArchives and lab books

**Lab book or Lab notebook?**
 You might have spotted that you have LabArchives "Notebook" whereas I keep referring to a "Lab Book". What's the difference? Not much. Your LabArchives Notebook is a general notebook where you can document and collect all manner of thoughts, activities and reference materials. A _Lab Book_ is specifically for recording what you have done in the lab. (Remember this is a "computer lab".) Hence your Notebook has a **Lab Book** folder for logging all your experimental activity. It is important that you keep accurate records of what you actually did, not simply what you intended to do, as this will help track down problems later. (Its mostly semantics.)

**The curse of autocorrect.**
 If you are using a "clever" office tool, such Word, OneNote or Evernote, it - or even your OS itself - will probably include an oh-so-helpful autocorrect function. This can be a real pain when trying to make notes about bioinformatics (or course documentation), as it will do helpful things like turn "zID" into "aid". Keep an eye your notes! Computers are dumb when it comes to typos, so an autocorrect-induced mistake in your recorded command will render it useless - or worse! A particular issue is the replacement of hyphens – which Word will often replace with a "dash" like it did just then. -n might be a valid program option but –n will not be! Spot the difference?

**What the font?**
 Along with copy-and-paste auto-correct issues, you also need to be wary for characters that look very similar, e.g.

0 1 2 1 0

k l m N O

**ISO 8601 Dates.**
 Despite adopting a common calendar, humanity has failed to use a common date format. Americans, for example, favour MM/DD/YY, whilst Aussies have DD/MM/YY (or YYYY). In addition to the confusion of month/day order, / is a path separator and so cannot be used in names. Although not widely used, humanity has actually agreed on a common date format: ISO 8601, YYYY-MM-DD. The beauty of this format is that alphabetical order and date order match perfectly, so sorting issues are a thing of the past. Use it!

### 24.1.3.Text file manipulation

**What the CRLF?**
 Windows, UNIX and Mac OSX all use different line ending encodings, in their infinite wisdom. There are two "hidden" characters: Carriage Return (CR) and Line Feed (LF). Windows uses CRLF. Linux only uses LF. Mac OSX used to only use CR, though I think modern Macs now use LF too. If you are getting odd behaviour when loading a file or running it with a Linux program, open it up in a good text editor and check the line endings!

1.
### Homology searching & sequence alignment

**The importance of E.**
 For some reason, BLAST websites often have a default e-value threshold of 10. This means that you expect to see 10 hits _purely by chance_ given your search parameters! I think they do this because people get upset when they get no results but it can catch out the unwary. Generally speaking, real BLAST hits will have very low e-values, so set this to 0.0001 (1e-4). You only need to use bigger e-values when searching very short sequences or for very distant homology. When looking for close homologues of genes or proteins, you will often want an even more stringent e-value that this, which can be done using local BLAST searches (as we will see later).

**Local or Global?**
 This match has 92.7% identity. But 92.7% of what? The query sequence? The hit sequence? (These are different lengths.) Or the matching region? I don't think this is explicitly stated anywhere but this is the  **local percentage identity,**  meaning that it refers only to the hit region. (The  **L**  in  **BLAST**  stands for local.) A  **global**  alignment or statistic deals with the full-length of the sequence. Note that these percentage identities can be very misleading as a result. What would you rather have, a 90% match to 10% of the sequence or an 80% match to 100% of the sequence?

**Which aligner should I use?**
 There is no such thing as the best multiple sequence alignment program. The three mentioned above - Clustal Omega, MUSCLE and MAAFT - are all good and will have similar performance overall. One might do better with one set of sequences and a different program might do better with another. When the alignment is important to you, you should always look at it. Where it really matters, you might want to try two or three different programs and see which looks better - or perform downstream analyses with both if you can't decide, and see how much difference the alignment makes to your final results, e.g. the phylogenetic tree produced.

**What species is that?**
 The five-letter uppercase code used by the SLiMSuite naming format is the Uniprot species code. Some of them are obvious (e.g. HUMAN for human), while many are the concatenation of the start of the genus and species (e.g. _Canis familiaris_ becomes CANFA). In time, you will get to recognise some (e.g. NOTSC for the tiger snake). Any that you are not sure about can be looked up at [https://www.uniprot.org/taxonomy/](https://www.uniprot.org/taxonomy/).

**What makes a good redundancy cut-off?**
 Every protein is different - both in terms of functional constraint (and thus evolutionary rate) but also in terms of how well it has been sampled from different species. It is therefore tricky to come up with a one-size-fits all solution. Generally speaking, 95% is probably good for most annotation/phylogeny analyses but when you have lots of sequences you might even want to go lower.

### 25.1.1.Using SLiMSuite

See **Section 8.1** for details on the SLiMSuite fasta file format.

**The log file**
 Every SLiMSuite program generates a \*.log file with key details of the run. The name of this file is either set with log=FILE or basefile=PREFIX (as above). The latter also sets the prefix for results files, depending on the program. By default, the log is named after the program run. (Look in the directory you used for sequence renaming and aligning in Task 9.) Changing the name makes it easier to keep logs associated with the actual task being performed, in addition to having multiple separate logs of different runs in the same directory.

**SLiMSuite command line arguments: -arg val versus arg=val**
You might have noticed that I often refer to arguments in the text as  **query=X**  but then run them in the command as  **-query X**. SLiMSuite can use both notations interchangeably and it is simply a matter of convenience which to use.  **arg=value**  is often clearer to read by  **-arg value**  is particularly useful when the argument takes a filename as you can you the  **TAB**  autocomplete functionality of UNIX to make typos less likely.

© RJ Edwards 02/01/2023
