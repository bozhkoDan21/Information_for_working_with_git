# Information_for_working_with_git
A small cheat sheet for those new to learning git

### Command Line Basics
| Сonsole command                                       | Description of the console command                       |
|-------------------------------------------------------|----------------------------------------------------------|
| ```pwd```                                             | displays the path to the current directory               |
| ```cd```                                              | change directory                                         |
| ```ls```                                              | display directory contents                               |
| ```cd ..```                                           | go to a higher level in the directory                    |
| ```ls -a```                                           | output a list showing hidden files                       |
| ```touch «name_file»```                               | file creation                                            |
| ```mkdir «name_dir»```                                | creating a directory                                     |
| ```mkdir -p «name_dir/name_dir»```                    | creating an entire directory structure                   |
| ```cp "what we copy" "where we copy"```               | copying files (you can specify several files at once)    |
| ```mv "what we are moving" "where we are moving"```   | moving files and folders                                 |
| ```сat «name_file»```                                 | reading files (works only with text files)               |
| ```rm «name_file»```                                  | deleting a file                                          |
| ```rmdir «name_dir»```                                | deleting a directory                                     |
| ```rm -r «name_dir»```                                | deleting a directory along with all its contents         |
| ```cd ~/[Tab]```                                      | displaying a list of directories using the [Tab] key     |

*Commands in the terminal do not need to be typed in and executed one by one. They can be specified not one at a time, but in a list at once. To do this, they need to be separated by two ampersands (&&).*
*__Example:__* $ ```mkdir second-project && cd second-project && touch index.html style.css```

### Git Basics
| Сonsole command                                                                    | Description of the console command                                     |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| ```git config --global user.name```                                                | to set up a user in the system - enter a name                          |
| ```git config –-global user.email```                                               | to set up a user in the system - enter email                           |                                      
| ```cat ~/.gitconfig```                                                             | reading user settings in a configuration file                          |
| ```git config --list```                                                            | output the contents of the configuration file                          |
| ```git init```                                                                     | make the folder a repository (to do this, move to the desired folder)  |
| ```rm -rf .git```                                                                  | delete the created local repository                                    | 
| ```git status```                                                                   | checking the repository status                                         |
| ```git add  --all```                                                               | preparing to save all files to the repository                          |
| ```git add .```                                                                    | add the entire current folder                                          |
| ```git commit -m "comment"```                                                      | commit                                                                 |
| ```ls -la .ssh```                                                                  | checking for SSH key availability                                      |
| ```ssh-keygen -t ed25519 -C "the email associated with your GitHub account"```     | SSH key generation                                                     |
| ```ssh-keygen -t rsa -b 4096 -C "the email associated with your GitHub account"``` | generating an SSH key if an error occurred during the first generation |                             
| ```ls -a ~/.ssh```                                                                 | checking SSH key generation                                            |
| ```ssh -T git@github.com```                                                        | checking the correctness of the SSH key                                |
| ```git remote add origin git@github.com:%ACCOUNT_NAME%/first-project.git```        | linking a remote repository to a local one                             |
| ```git remote -v```                                                                | make sure the repositories are linked                                  |
| ```git push```                                                                     | push changes to a remote repository                                    |

```git push -u origin main``` 
*The first time this command must be called with the -u flag and the parameters origin (the name of the remote repository) and main or master (the name of the current branch). The -u flag will link the local branch to the remote branch of the same name. Just as you linked the local and remote repositories in the previous lesson, here you also need to additionally link the branches.*
