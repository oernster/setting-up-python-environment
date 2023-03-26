# setting-up-python-environment
A quick guide on how to setup a python environment for development

Install python latest from https://www.python.org (make sure you tick set PYTHONPATH during the install)

Install vscode from https://code.visualstudio.com/download

Launch a command line in windows: run cmd.exe

Or on a mac: run Terminal.

Then ‘pip3 install virtualenv’
 
To edit code, you use vscode the program you installed.  On a mac I don’t think vscode actually formally installs itself, it just extracts the contents of a zipped up program which has been compressed to save on download bandwidth into your user Downloads folder.  Therefore you will need to code the ‘vscode.app’ or whatever it’s called program from your Downloads folder into ‘Applications’ folder using Finder (see bottom left of your mac).
 
On windows I think it’s a simple follow the instructions to install so not a worry there.
 
Create a directory called Development somewhere on your mac or windows laptop using Finder or explorer.  Then create a subdirectory INSIDE that directory after double clicking on it called e.g. ‘example_project’.
 
Then, on either windows or mac do: ‘virtualenv venv’ AFTER changing directory to your example_project directory where you want to work.
 
To change directory on windows OR mac you type ‘cd name_of_folder’

To identify your current directory on windows just look at the command line.

To identify your current directory on mac do ‘pwd’ on the Terminal (Present Working Directory).

Once you’ve created your virtual environment (venv in this case) on either windows or mac you’ll need to activate it.
 
On mac, in the terminal, type: ‘source venv/bin/activate’

On Windows it’s different, I think it’s ‘venv/Scripts/activate’ but you can check the directory names (folders) on windows by typing dir in the command line (cmd windows terminal).

To list the contents of a directory on a mac, type ‘ls’ in a terminal.
 
To install any python package (make sure you activate your virtual environment first), you need to run the following command:
 
‘pip3 install <insert name of package here without angled brackets>’
 
For example:
 
‘pip3 install requests’
 
Or pandas, numpy, whatever.  If you’re not sure of the name of a package or it complains due to misspelling or something when you try and pip3 install a package then you may need to google for the correct pypi (which is the name of the package central storage location for python packages you can install using pip3) package.
 
Note, when you first use pip3, it may complain saying you need to upgrade.  It may also do this periodically if it detects you aren’t on the latest version of pip3.
 
To fix this type: ‘pip3 install –upgrade pip’ on the Terminal on mac or cmd program on Windows.
 
When you are ready, open vscode.

Open the directory Development / example_project in vscode

Select the create file button and call it something like ‘elizabeth.py’ – I have attached a small picture of the create file/create folder buttons in vscode: Image - they are the ones with plus signs.  On mac save the file with ‘command + s’ – on windows save the file with ‘ctrl + s’ – obviously you will need to write some code first.
 
Useful commands on a mac:
 
Command + x (cut text or image)
Command + c (copy text or image)
Command + v (paste text or image)
 
Windows has the same policy but it’s Ctrl + whatever instead since there is no command button on windows.
 
To run a python program, launch Terminal on mac or cmd on windows and then navigate using cd (change directory aka folder) to your project directory in Development.  Then activate your virtual environment.
 
Now if you have installed stuff into your virtual environment it’s nice to be able to reinstall it if necessary or save the setup.  You can store it all by doing this:
 
‘pip3 freeze > requirements.txt’  - this will ONLY work properly if you have activated the venv.

That will save all python installed libraries in the virtual environment into a text file called requirements.txt.  This can be opened in vscode or notepad or whatever you like; your favourite editor basically.
 
Now when you next want to give your code to someone else or use it again you simply activate a venv and then type: ‘pip3 install -r requirements.txt’ and this will install all python packages that are required for your current project.

Later on, if you need to, you can exit the virtual environment by typing 'deactivate' on the command line/terminal prompt.

OK next…
 
In a terminal on a mac, or in a cmd prompt on windows, run your program:
 
‘python3 elizabeth.py’
 
Look at the results on the output before the next waiting command prompt appears.  That will show your standard output printed statements.
