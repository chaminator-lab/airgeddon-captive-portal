#Requierements: Some basic html
# HOW TO MODIFY AIRGEDDONS CAPTIVE PORTAL AND STORE USER INPUT.
IMPORTANT NOTE :\
-The files in the repo represent an example of a targeted virtual attack against an Educational institution made for educational purposes only.

# First :

when using the "9: Evil twin attack with captive portal" you need to know that the captive portal files that are presented to the target when they try to login are stored in the /tmp/www file on your linux machine, AND ARE PRESENT ONLY DURING THE ATTACK SO DONT LOOK FOR THEM BEFORE YOU START AN ATTACK.
This is the structure of the tmp/www/ file .

![Screenshot_2023-11-25_17_20_09](https://github.com/chaminator-lab/airgeddon-captive-portal/assets/82542602/46cb659f-d08d-43ce-a877-af7d900aebe9)

in our example we are going to first create the desired html/css/js files of a website you wanna display on the targets screen, in my case i just downloaded the files from the original login page of my target in this case its and educational institution Universite de Namur.

# Second :

You need to add the bash tags as such :\
add a #!/usr/bin/env tag at the first line of the html. \
add (echo -e ')  at the beggining of each line and close each line with ('). \
in general try to follow the structure of the original index.htm file : 

![Screenshot_2023-11-25_17_48_07](https://github.com/chaminator-lab/airgeddon-captive-portal/assets/82542602/a6da0fad-a1ae-486f-9b47-c6f2e0848c52)



Once that is done go to the html file and change the action tag of the login form to point to check.htm .


# CHECK.HTM  is where the bash magic happens.
Now create a check.htm file in the same directory as index.htm, you can copy the one in the repo and modify the path (lines 32 and 40) to a txt file where the credentials will be stored on your local machine.
 
