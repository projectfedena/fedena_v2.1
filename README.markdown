Fedena : Open source school management system

Project Fedena is the open source school management system based on Ruby on Rails. It is developed by a team of developers at Foradian Technologies. The project was made open source by Foradian, and is now maintained by the open source community. Fedena is the ideal solution for schools and campuses that want an easy means to manage all campus records.

The Project Fedena website http://www.projectfedena.org/ is the home to the developer community behind Fedena project. There you can find forums and bug tracker for Fedena.

Demo
A demo website for Fedena has been set up at demo.projectfedena.org. You can log in with following usernames and passwords:

    * As admin -- username - admin, password - admin123
    * As student -- username - 1, password - 1123
    * As employee -- username - E1, password - E1123

License

Fedena is released under the Apache License 2.0.

Installation

Fedena requires Ruby,Rails,MySQL and some gems installed.
Step 1: Install Ruby

   1. Download the latest One-Click Ruby Installer for Windows. (Preferably version 1.8.6)
   2. Double-click on the downloaded executable and follow the installation instructions. Unless you have some special needs, just press Enter to accept all of the defaults.

Note to Linux and OS X users: Please install rubygems from the packages.

Step 2: Install Rails

Now we can use the RubyGems package manager to download and install Rails 2.3.5(Note: Version should be 2.3.5),

   1. Open a command window and run the command gem install rails -v=2.3.5 --remote.
   2. RubyGems will also install all of the other libraries that Rails depends on. For each of these dependencies, RubyGems will ask you if you want to install it. Answer "y" (yes) to each one.

Step 3: Install MySQL

   1. Download  and install the latest "essential" version of the MySQL installer.


Step 4: Setup Fedena

   1. Download Fedena source code for GitHub. Extract the ZIP/TAR archive and save to a folder (say C:\Fedena).
   2. Now goto the fedena source directory in the command window.
   3. Run the command  rake gems:install .This will install all missing gems.
   4. Update the MySQL login details in config/database.yml
   5. Run the command  rake db:create. This will create the required databases.
   6. Run the command  rake db:migrate. This will populate the database with required tables.
   7. Finally, run the command ruby script/server .This would start the server and it will be accessible at http://localhost:3000
   
Fedena Configurations:

 1. To enable SMS Module
            i) Add a new row with config_key = "AvailableModules" and config_value = "SMS" (without quotes,case-sensitive) of `configurations` Table
           ii) Update the SMS API settings in Libs/sms_manager.rb to use the SMS Module.
2. To disable HR module, delete the row with config_key = "AvailableModules" and config_value = "HR"
3. To disable Finance module, delete the row with config_key = "AvailableModules" and config_value = "Finance"

Community Support:

Visit www.projectfedena.org for community support.
