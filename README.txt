This plugin allows you to configure automatic relationships between users from an external database.  

THIS PLUGIN IS IN BETA STATUS! BE CAREFULL WITH PRODUCTION ENVIRONMENT!

Users familiar with enrol/db should have no problems configuring this.

Plugin has been tested on 2.3 and 2.6. and 3.4

This plugin was first developed by Penny Leach <penny@catalyst.net.nz> for Moodle 1.9
by I modified it to work with Moodle 2.3. Modified by https://github.com/mfuhrmeisterDM for 2.9 and Madhu Avasarala for 3.4

This is my first experience with Moodle plugin development, so your comments are more than
welcome. Useless to say that you use this piece of code at your own risk :)

In the configuration, "Subject" represent the parent, and "Object" represent the student.
(You can easily create a table in your database same or separate from Moodle using phpmyadmin using a CSV file.
In phpmyadmin, click on import and select file and if it is CSV all options are filled in automatically.)

HOW TO INSTALL
==============
Prerequisis
a. SQL table containing mentee-mentor-role relationship information
b. PHP library to connect to SQL table
c. mentee and mentor already in Moodle
d. role already in Moodle

1. Download all the files in the directory {MOODLE_DIR}/enrol/dbuserrel (using git, GitHub website, or anything else)
2. Go to http://{MOODLE_URL}/admin to complete the installation
3. Fill all parameters using Moodle plugin administration interface (http://{MOODLE_URL}/admin/settings.php?section=enrolsettingsdbuserrel
4. Setup a cron job to execute {MOODLE_DIR}/enrol/dbuserrel/cli/sync.php (add -v for more output, and redirecte output to log file)

Feel free to send me any comments/suggestions

Maxime Pelletier <maxime.pelletier@educsa.org>
