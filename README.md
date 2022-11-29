This project is meant to run in a linux environment. 
All necessary tools are built into the singularity container, which can be built directly from the biovino_sing.def file. 
In order to build the container on a linux server, you have to create an access token https://cloud.sylabs.io/dashboard after making an account.
You can then use the command 'singularity remote login' and enter your access token when prompted.
After logging in you can then execute the bash script 'biovino_record.txt' to build the singularity container and produce the assembly results!
