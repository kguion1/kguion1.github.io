---
title: Introduction to GitHub
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

## What is GitHub?
GitHub is a cloud-based software development tool. You can think of GitHub similar to Google Drive, but created for code! With GitHub you can save code in your web-based account, revert your code back to previous "versions", and collaborate with other coders just like you can edit, track changes, and collaborate on files with Google Drive! The key differences between GitHub and Google Docs is in the usage. GitHub requires more manual steps by the user than the automatic saving that Google Docs provides. In GitHub, the saved file and the file being edited are separated. The user will have both a copy of their code on their computer to edit as well as the saved copy on their GitHub web account. Any edits must be manually saved and uploaded to GitHub.

**INSERT PHOTO**

## How do I use GitHub?
There are a few different methods to take advantage of a GitHub account. While there is a Desktop application version of GitHub, this article will discuss how to access GitHub using command line on a terminal and through any web browser. If you are unsure about what “terminal” we are referring to, please see INSERT LINK before continuing.

### Step 1: Set up an account!
Navigate to [github.com](https://github.com) to create an account

### Step 2: Ensure the git client is installed in your terminal of choice.
An easy way to do this is just to type ```git --version``` on the command line. The version of git that you are using should appear. If it does not, you can download git [here](https://git-scm.com/).

### Step 3: Set up an SSH key.
An SSH key is a security feature that is not unique to GitHub. Creating an SSH key will allow you to sign into GitHub from your terminal without even typing in your password! It works by generating two unique “keys” for your identity. One private key is kept on your computer while the other public key is given to GitHub, or any other service you are using. Whenever you attempt to login, an algorithm converts your private key to the public key and matches it to your account. Rather than GitHub storing a traditional password, GitHub only has access to a public version of your SSH key, creating a more secure account and login. 

To generate an SSH, complete the following steps, or see [this article](https://docs.github.com/en/enterprise-server@3.0/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). 

  1. Open you terminal and type 
        
          ssh-keygen -t rsa -b 2048 -C "insert email here"
        
  2. Press Enter for default “Enter file in which to save.” and enter your desired passphrase. This passphrase is optional. Skip by pressing Enter. This should result in a random image being generated in the terminal.

 3. Go to your [GitHub Keys](https://github.com/settings/keys). This can also be found in your Settings -> SSH and GPG keys.

  Click the green “New SSH key” button in the top right. You should see the following screen. **INSERT IMAGE**

  In the Title section, name your key. For example, “My Laptop.” A separate SSH key is used and needs to be generated for each individual computer that you login from.

 4. Run the following command in your terminal and copy the output, which should start with “ssh-rsa” and end in your email.
                   
          cat ~/.ssh/id_rsa.pub

HINT: Sometimes your copy and paste keyboard shortcuts do not work in the terminal. For example, ```ctrl-C``` in Terminal usually is a shortcut to stop running  the current program. On Windows Ubuntu, you can right click the top banner and select Edit -> Copy or Paste. Alternatively, you can try ```ctrl-shift-C``` to Copy and ```ctrl-shift-V``` to Paste. For Mac, you can select Edit -> Copy or Paste, or ```command-c``` and ```command-v```. Unfortunately, these commands do not always work with the Nano text editor and typing it out may be the easiest option.
         
 5. Set up Git on your computer:

Configure your personal information with the following commands in your terminal:

		git config --global user.name "First Last Name"
		git config --global user.email "insert email"

(Optional) Set some quality-of-life settings:

		git config --global color.ui auto
		git config --global core.editor "nano"
		git config --global core.autocrlf input
		git config --global push.default simple


WHEW that was a lot of steps! You can now use the SSH key to login to GitHub from your terminal without typing in your password! Remember, a separate SSH key is used and needs to be generated for each individual computer that you login from.

### Step 4: Create your first repository
In GitHub, a *repository* is a project folder for all the files related to a single project. Remember that in practice, two “versions” of this repository will exist. The first is a local copy of the repository. This will look like any other folder that you have on your computer. In this version, you can edit and run your code. The second version is the saved version on your GitHub account. This can be accessed via your GitHub web account and any code history or changes can be tracked. You must manually upload any edits made to your local version to the saved version. There is NO automatic saving. 

We also mentioned that like Google Drive, you can collaborate on GitHub. To do this, each collaborator has *their own local copy of the repository* and then saves it to the *same repository on GitHub*. 

#### Let's try to set up your first repository!
Please note that there are multiple ways to do this. This is just an easy first example.
   1. Login to your GitHub account on any web browser
   2. Look for your icon in the top right corner -> Your Respositories -> green **New** button
   3. Create an informative name for your project folder, select **Private** and select an "Add a README file"
   4. Create!
   5. Click the green **Code** dropdown -> SSH -> Copy the line starting with **git@github.com**
   6. Open your terminal and use ```cd``` to navigate to where you want to create your local copy of the folder. We suggest the Desktop or Documents.
           
           git clone PASTE FROM STEP 5
           
   7. Congrats! You have created your first repository. To double check, open your file system normally and look for your folder.

### Step 5: "Push" your first file
Now you that you have an empty repository, let's create and save your first file!
   1. Open your terminal and navigate into the local copy of your new repository
   2. Create a new file with ```nano```
    
           nano test_file.txt
        
   3. Use the nano test editor to write a fun message in your new file
   4. Now is the important part. If you login to your GitHub account, you can see that your *test_file.txt* is not yet there. That is because there is **no automaic saving**. The following commands will need to be followed every time you want to save the changes from your local copy to the saved, web-based copy.
          
         ```git status``` shows the current "status" of your repositories. 
         Anything in red and labelled as "Untracked files" are saved in your LOCAL copy, but NOT saved in your web-based copy. 
         
         ```git add .``` This gets all untracked files ready to be saved. Alternatively you can replace the . with a specific file name to just save one file rather than all untracked files.
         
         ```git commit -m "informative message"``` This "commits" your files to being pushed up to the GitHub version
         
         ```git push``` This "pushes" your files to the GitHub version
         Check your online GitHub account and your file should now be visible!
         
         ```git status``` Notice the difference after you have added, committed, and pushed your new file.
         
         
Congratulations! You should now have a basic understanding of how to use GitHub. Though it may be confusing at first, GitHub is very heavily used in the coding community and is a great, marketable skill to have. As you practice more and more, GitHub will make more sense and you will be able to take advantage of all that GitHub has to offer. 

## TL;DR
* GitHub is like Google Drive for coders.
* To use GitHub from the terminal, an SSH key is used.
* Repositories are project folders in GitHub.
* TWO “versions” of the repository exist: one on your local computer for editing and running code; the second is saved on your GitHub account.
* To save code:
      
     - Use ```cd``` to navigate into your repository
      
      git status
      
      git add .
      git commit -m “insert an informative message in quotes"
      git push
      
      git status
