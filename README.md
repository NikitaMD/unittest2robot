What
The script when run in a directory containing python unittest will generate the keyword script file and binding python library so that the keyword script file will run the original unittest within the robot framework

Why
I wrote this bash/python script to allow an existing python unittest suite to be run using the robot framework . We also discovered that the script works for selenium2 tests exported from webDriver ( since they are also unittest.TestCase subclasesses ) Our organisation is attempting to consolidate all automated test reporting thru the robot framework

How
1) drop these in the directory where the python unittest files are are . ( note theres no naming restriction on the unit test files except that they have the .py extension )

2) open terminal and cd to the directory first test the unittest in its output form to make sure it runs ok in python ( outside robot ) python name_of_unit_test_file.py

3) make the script executable chmod a+x unittest2robot.sh

4) generate robot scripts ./unittest2robot.sh

5) run robot scripts python -m robot.run <<generated script name>>.txt

Where
I've tested the script on Mac OS X and Centos and it should generally run on fine any community 'nix .

Who
I hope this is of use to anyone who's working on integrating their testing into ronot framework . Maybe I solved a problemm that was already solved but I went looking for a solution and couldnt find one . My feeling is that there may be good integration material for robot frameworks based on java . but strangely , albeit a python based framework there doesnt seem ( I am obviously not looking hard enough ) to be the same supporting utilities for python based test code . Anyway as I say HTH - You have artistic licence so go crazy - please let me know how you get on or any comments , suggestions , chiding etc ..
