# 1. Introduction

`FlymeOS` Flyme Patchrom -- providing developers with industry-leading Patchrom tools

June 30, 2015,`FlymeOS` Patchrom Finally Released.

[![License](https://img.shields.io/badge/License-Apache%20V2.0-blue.svg)](LICENSE)


# 2. Branch

Now Flyme6 Only Support **Android 6.0** and Corresponding branch is `marshmallow-6.0`


Directory Structure: 

    FlymeOS
     +-- manifest           List of projects
     +-- tutorials          Tutorial documentation
     +-- plugins            Extensions for extending existing functionality
     +-- build              Compiler Environment , Used to build and compile rom
     +-- tools              Patch tool
     +-- flyme              Flyme related, content is updated regularly
          +-- release       ROM Package By Flyme Official
          +-- overlay       Overlay
     +-- devices            Devices directory
          +-- base          Official default Device
          +-- your_device   Your Devices Base


# 3. Code download

Use repo init with "-b" for download the branch you want
Use repo sync for upgrade The latest code form flyme git

    $ repo init -u https://github.com/FlymeOS/manifest.git -b marshmallow-6.0
    $ repo sync -c -j4

If the connection has failed or the download code is too slow, use the following command:

    $ repo init --repo-url git://github.com/FlymeOS/repo.git \
                -u https://github.com/FlymeOS/manifest.git \
                -b marshmallow-6.0 --no-repo-verify
    $ repo sync --no-clone-bundle -c -j4


# 4. Port to your Device

<b>* Standard procedure</b>

After downloading the code, Execute the following command to initialize the development environment

    $ source build/envsetup.sh

Create a new device(E.g demo), ROM will Build in this directory

    $ mkdir -p devices/demo
    $ cd devices/demo

then follow the Step for build a full flyme patchrom :

    $ flyme config      # Generate device config file - Makefile
    $ flyme newproject  # Generate new device directory (will pull vendor form your phone)
    $ flyme patchall    # Automatic Patching
    $ flyme fullota     # Generate Your own Flyme ROM Package


<b>* Conflict</b>

Automatic Patching may cause some reject Conflict. Each Conflict will be display like this.
Developer have to fix these Conflicts by hand.


    <<<<<<< VENDOR
      Vendor Code
    =======
      Flyme Code
    >>>>>>> BOSP


<b>* Version Upgrade</b>

You can upgrade your device code like this (No Need to do patchall every time)

    $ flyme cleanall
    $ flyme upgrade


# 5. Contribution code

We encourage developers to contribute to flyme open source. Using Github`s Pull-Request，Then you can send your code to official

![image](github-pull-request.png)

- First,Click 'Fork', Fork the source to your github
- Then,Change or Add the Code Form your Github && Commit
- At Last , Click "New pull request" at the Github Page, For Sending a Pull Request to Flyme Official


# 6. Other

<b>* Ask For Help && Feedback</b>

- <p><a href="mailto:446108651@qq.com">446108651@qq.com</a></p> (QQ Mail)
- <p><a href="mailto:zoujunhua86@gmail.com">zoujunhua86@gmail.com</a></p> (Gmail)


#Test Translate / May Have some Grammar error 
