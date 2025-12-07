# PYTHON
Under python, we did a number of labs. I will show case 2 of the labs here

# FIRST LAB
# HELLO WORLD
I worked through an introductory lab with Python programming using AWS Cloud9, learning how to set up my development environment and write my first Python program. Here's what I did.

- Starting the Lab Environment I clicked "Start Lab" at the top of the instructions and waited for the "Lab status: ready" message before closing the panel. Then I accessed the AWS Management Console, selected Services > Cloud9, found the reStart-python-cloud9 environment, and clicked "Open IDE."
- Exercise 1: Creating a Python Exercise File In the AWS Cloud9 IDE, I created a new Python file by choosing File > New From Template > Python File. I deleted the sample code from the template and saved the file using File > Save As.
- Accessing the Terminal Session I opened a terminal by clicking the + icon and selecting "New Terminal." I used the pwd command to check my present working directory, which showed /home/ec2-user/environment. Then I checked the default Python version and explored other available Python versions installed in the environment.
- Exercise 2: Writing My First Python Program I entered Python code into my file and ran it to see the results, successfully executing my first Python program in the Cloud9 environment.

![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/pythonImages/pyEnvironment.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/pythonImages/pyTerminal.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/pythonImages/createFile.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/pythonImages/fileCreated.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/pythonImages/pyVersion.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/pythonImages/HelloWorld.PNG?raw=true)

# Challenges

At first, I wasn’t entirely sure how to run my Python file from the terminal. I had to experiment a bit to figure out the right command, and at one point I forgot to save the file before executing it. That small mistake had me wondering why none of my changes were showing up in the output, which added a bit of confusion until I realized what happened.

# WHAT I LEARNED
Here's what I learned from this:

- I created my first Python program following the traditional "Hello, World" exercise, which is the standard starting point for learning any programming language.
- I verified that Python was correctly installed and configured on my Linux system by successfully running a basic script.
- I used the nano text editor to write Python code and executed it from the command line using the python3 command.

# Lab Complete 🎓
# SECOND LAB

This lab was given to us as a challenge and my challenge was to:

Write a Python script to:

- Display all the prime numbers between 1 to 250.
- Store the results in a results.txt file.
- Test the script. Verify that it produced the expected results in the results.txt file.

Save the script and make a note of its location (absolute path) for future reference.

Note: Both Python 2 and Python 3 are installed on the Linux Host. It is recommended to use Python 3. To run a Python script using version 3, run the following command by replacing file.py with your f0ile name.

CHALLENGES
File Handling Syntax: I struggled with properly closing the file after writing to it. I forgot to include the close() method initially, which could have caused issues with data not being saved properly to results.txt.

# WHAT I LEARNED
Here's what I learned from this challenge:

- I created a Python script using the nano text editor and learned the importance of proper indentation and syntax in Python.
- I implemented a prime number algorithm that identifies all prime numbers between 1 and 250 by checking for divisibility.
- I used Python's file handling methods to write results to a text file for permanent storage.

# OVERALL
I learned how to write and execute Python scripts on Linux, process numerical data, and save output to external files using the command line

# Lab Complete 🎓

