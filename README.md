Download Link: https://assignmentchef.com/product/solved-cis2250-lab3
<br>
What you learned from the last lab:

<ol>

 <li>How to read through a CSV file and select the items that you want.</li>

 <li>How to read parameters off of the command line, such as the name files thatwe used in Lab 2 containing the names of people in the United States born ina particular year.</li>

</ol>

In this lab we will do two things:

<ol start="12">

 <li>We will trace popular names across a number of years.. We will look for the names of people in the class in those American name files.</li>

</ol>

Be sure toportant tips are included at the end. (Always a good strategy for any assignment,actually!)             <em>read the entire lab description </em>before beginning the lab, as some im-

<h3>Lab Task Description</h3>

Open the CourseLink page for our course (link is in the sidebar) and collect thematerials for Lab Assignment 3.<sub>usaSSnames.zip</sub>. Unzip these to get the input data for the tasks below.You will need the files cis2250Names.csv and

Retrieve a copy of your Perl script fromwhich of your implementations to use. If you did not get the previous assignmentworking, you can download working code from the CourseLink site for but you willlose 10% of your grade for this lab. You will see this available as “Solution for Lab 2.” <em>last week’s lab</em>. Decide with your new partnerEmergency Kit:

to the following description:Copy your code into a new file called findFirstNames.pl and change it according

<ul>

 <li>the command line should list two files:</li>

</ul>

<ol start="12">

 <li>the name of one of the “. the name of a file containing first names only, one per line(these files contain data about a given “Year Of Birth” in the US– Thein this formcis2250Names.csvyob” name data files stored withinfile you have downloaded from CourseLink isusaSSnames.zip)</li>

</ol>

<ul>

 <li>Your code should read in both files and output the following:</li>

</ul>

– Print out each of the names in theline) and next to each name also print out in brackets its ranking. Theranking should appear in one of the following three forms, depending onthe data: cis2250Names.csv file (one name per

<ol start="12">

 <li>if the name is used. if the name is used for both women and men, then the name shouldthe appropriate number should appear,have the female then the male ranking,<em>exclusively </em>for only women<em>e.g.e.g.</em>, “, “Andrew (3070,7)Kassy (4475)<em>or </em>for men, then only” ”</li>

 <li>if the name does not appear in the name data file at all, it should haveranking zero <em>e.g.</em>, “Otter (0)”</li>

</ol>

<ul>

 <li>At the end it will print out both:</li>

</ul>

–– the number of names from the second file that were found in the first file,the number of names from the second file thatand                                                                    <em><sub>were not </sub></em>in the first file.

<sup>#H</sup>This lab is about integrating databetween multiple files.Learning objectives:<sup>iteration</sup>manage multiple open filescalculate values based on multiplepieces of data within a fileSelecting a strategy to deal with file Constucting strategies to# Learning to

<h2>Skills</h2>

coordination + communication (3/6) organization + planning (3/6) teamwork (3/6) programming + tools (5/6) strategy (1/6) visualization (0/6)

(*)[tal Awareness) to 6 (Main Focus).]The skill scale is from 0 (Fundamen-

Image description

A pair of sea otters. Image courtesyof US National Oceanic andAtmospheric Administration, whoplaced this image into the publicdomain.

<h3>Strategies for This Lab</h3>

Think about your loop structure: you want to compare each value from one fileagainst every value from the other file. Do you need:

<ul>

 <li>•• <sup>two loops, one after another?</sup>two nested loops (one inside the other)?three loops (two nested and one later)?</li>

</ul>

How can you decide this?

Remember that the female names come first and the male names follow so you willhave to make sure that the “ranking” for the male names reflects this. on line 3070 of the file, andFor example, if we search for “<sub>Andrew,M,23641</sub><sup>Andrew</sup>” in the fileon line 17662.<sup>yob2000.txt </sup>we would find Andrew,F,45

The first male name,male name ranked as number 1 we need to subtract 17655 from the line count inthe file. To calculate the rank of the male name Andrew correctly, we also have tosubtract 17655 from its line count.Jacob,M,34477 is on line 17656. Thus to mark “Jacob” as the

An example output looks like the following:

$ perlAakil     (0)findFirstNames . pl yob2000 . txt               cis2250Names . csv

<sup>Umut (0)</sup>Number ofNumber ofZayn (3920)Aasim (6313)Adarsh (4065)Wesley (6468,171)Abdul (1061)AbdullahZufarWilliam. . . . . . . . . .(0)(3521,11)(869)found names:missing names:9028

<h3>Overall Programming Strategies</h3>

You will likely run into some debugging problems in this lab. Debugging, when youdon’t know what is going on, is made much harder if you only have large files towork with.

Ask yourself this question: “<em><sub>lab?</sub></em>” <em>Where can I get smaller data files to help me debug this</em>

Another issue in this lab is ensuring that you have exercised each of the importantcases. <em><sub>How many different ranking situations are there? How can you ensure that</sub></em>

<em>you have each situation covered, and that you know what the correct answer is for your code to be printing?</em>

For this lab, it may be the case that Perl::Critic complains about the complexity ofyour code. We will address this next week.

Once you have completed this lab, go to the CIS*2250 CourseLink site and uploadthe <sub>findFirstNames.pl </sub>file for grading.