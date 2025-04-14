## Overview
- pip (short for "Pip Install Packages") is the default package manager for Python
  - This is since core principle of Python is its modular design, where functionality is organised into reusable applications 
  - Allows developers to build powerful applications by composing existing libraries rather than reinventing the wheel 
  - To support this, Python uses package maangers which are tools that automate the process of downliading, installing, upgrading, and managing these packages
- Allows users to easily install, upgrade, and manage third-party libraries and dependencies from the Python Package index 
- Especially useful when working in virtual environments, helping keep project dependencies isolated, reproducible and organised
- Note that there are other package managers beyond pip, such as conda 
  - All these are package managers that can be used to install packages, create and be used inside virtual/isolated environments 
  - There are advantages to choosing either (e.g. if use conda, it is a general-purpose package manager can install packages from conda repositories and manage non-Python packages)
    - I.e. packages from Python + system libs 
  - Usage note: 
    - if using venv (pip created virtual env), try to use only pip 
    - if using conda to create virtual environment, generally pip commands will work because it also sets up a Python interpretor and installs pip inside it
      - Use pip to install pip based commands that are not available in conda. 
      - If not, default is to use conda install whenever possible 
      - Best practice for reproducibility 
        - conda list 
        - conda env export --from-history #(minimal clean.yml)
        - pip freeze > requirements.txt #add for pip-installed extras 
  
- General syntax of pip commands: pip <command> [options] [package names]
  - <command> -> what you want to do e.g. install, list, uninstall
  - [options] -> optional flags to modify behaviour (e..g --upgrade, -r)
  - [package_names] -> package(s) you want to act on e.g. requests, numpy 

- Understanding CLI (command line interface) flags 
  - There are two types of flags 
    1. Short flags that start with "-" e.g. -r used in pip install -r requirements.txt
    2. Long flags that start with "--" e.g. --upgrade
  - Often both forms exist (e.g. -U = --upgrade), but not all long flags have short equivalents
    - Short flags usually used for core tasks, long flags offer more contro;
    - check pip help to see all 
  - common pip flags include 
    1. -r / --requirement: install packages from a requirements file 
    2. -u / --upgrade: upgrade package to the latest version 
    3. -v / --verbose: show more detailed output during execution 
    4. --no-cache-dir: do not use pip's cache when installing packages

----- Pip level commands  -------

1. Set up virtual environment by running a setup script (if provided). For manual creation of virtual environment, see below. 
source setup-env.sh

2. Get general pip help and version info documentation
pip help        #Shows general help and lists all available pip commands
pip --version   #Shows current pip version 

3. See help for a specific command (e.g. install)
pip help install OR 
pip install --help

----- Package Installation and Upgrading Commands -------

4. Install a package (e.g. requests)
pip install requests

5. View all packages currently installed in your environment:
pip list

6. Check all available versions of the requests package:
pip install requests==
Note: this will give an error message, but in that message all the available versions are displayed.

7. Install a specific (usually older) version of a package:
pip install requests==2.25.1

8. Check the installed version of a package:
pip list OR pip show requests

9. Upgrade to the latest version of a package
pip install --upgrade requests

10. Check all available versions of a package (e.g. requests), but only works if I'm using pip >= 20.3 version
pip index version requests 

10. Uninstall a package (e.g. requests)
pip uninstall requests

11. Freeze environment packages (for requirements.txt)
pip freeze > requirements.txt 

12. Recreate environment from requirements.txt
pip install -r requirements.txt


## Other notes 
- Create virtual environment to manage dependencies specific to project and avoid conflict between global and project-level packages 
  - Especially if developing portable projects, where sharing dependencies leads to the following two problems: 
      (1) Challenging to determine which packages are requirements for any given project. File may reference packages not needed for current project, when distribute these waste disk space and time. 
      (2) Over time, will have projects that require different versions of the same package. If sharing installed packages, need to change installed version whenever change projects or update these. 
  - Hence, better to create a unique virtual environment per project, e.g. using virtual machines and containers. 
  - Simple way in Python is to create a Python virtual environment - packages installed here are only ringfenced to the environment, hence keeping project dependencies isolated. 

- Workflow below (based on pip)
  (1) create directory 
    - mkdir my_first_project #creates a new directory named "my_first_project" in the current working directory
  (2) cd my_first_project #changes current working directory to "my_first_project"
  (3) pwd - print working directory 
  (4) create virtual directory with name "my_env"
    - python3 -m venv my_env 
  (5) Activate virtual environment before being able to use it
    - source my_env/bin/activate 
  (6)  Install packages to virtual environment
    - pip install pandas
  (7) List packages installed in environment
    - pip list 
  (8) Save installed packages to requirements file
    - pip freeze > requirements.txt
  (9) Deactivate virtual environment 
  deactivate

  There is also an equivalent workflow in conda that we will cover in a separate cheatsheet 

+++ 
## Create and export a requirements file 

1. Type:
pip freeze > requirements.txt
- To create a requirements file with the packages installed using pip. 
  #pip freeze command outputs the installed packages and their versions in the current Python environment 
  - > requirements.txt redirects the output of pip freeze to a file called requirements.txt. This file will list each package and version in the following format 'package_name==version'. 


#2. Type:
cat requirements.txt 
- To see the contents of the new requirements file. Idea is to quickly view the contents of the file in ther terminal without opening it in an editor
- Note that cat is not a pip command; it is a Unix/Linu shell command that also works in macOS. 
- Stands for concatenate, but most commonly used to print the contents of a file to the terminal 

  cat file.txt | grep "search_term"
    # use grep to search for patterns in text; when combined with cat, will filter out lines containing specific strings 
  cat file.txt | less
    # less allows viewing of large files in a scrollable manner 
  cat file.txt | wc -l
    # wc: word count, used to count lines, words and bytes. -l: display lines, -w: display words, -c: count bytes (characters)

  # Summary:
    cat file.txt | grep "search_term" – Search for specific lines.
    cat file.txt | sort – Sort the lines alphabetically.
    cat file.txt | less – View the file in a scrollable manner.
    cat file.txt | wc -l – Count the number of lines.
    cat file.txt | tee output.txt – Display and write to a file.
    cat file.txt | awk '{print $1}' – Extract the first word in each line.
    cat file.txt | head -n 5 – Show the first 5 lines.
    cat file.txt | tail -n 5 – Show the last 5 lines.
    cat file.txt | tr 'a-z' 'A-Z' – Convert lowercase to uppercase.
    cat file.txt | cut -d',' -f2 – Extract the second field from each line.
    cat file.txt | sort | uniq – Remove duplicate lines after sorting.

+++
#ls: list contents of a specified directory
  # e.g. ls /home/user/documents 
