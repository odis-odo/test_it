<br>

### rsync - a fast, versatile, remote (and local) file-copying tool

<br>

  Basic usage of rysnc:

	rsync dir1 dir2

<br>

  Copying a file from local machine to a server:

	rsync dir (username)@(servername/ipaddress):/home/user/dir

<br>

  Copying a file from local machine to a server dong a test run first: 

	 	rsync -r --dry-run  dir (username)@(servername/ipaddress):/home/user/dir


  The -r option is added as well for recursive,also adding -v for verbose displays the
  file names to be copied.

<br>
  
  Copying a file from a server to a local machine:

	rsync -rv --dry-run (username)@(servername/ipaddress):/home/user/dir/ dir/

<br>

  The --delete option will delete any file in the target directory thats not in the 
  source.

	rsync -rv --delete  dir (username)@(servername/ipaddress):/home/user/dir

<br>

  The -a option will make sure that the meta data of the files are the same:

	  rsync -rva --delete  dir (username)@(servername/ipaddress):/home/user/dir

<br>
  
  The -z option will compress the files while transferring on slower connections:

	rsync -rvaz --delete  dir (username)@(servername/ipaddress):/home/user/dir

<br> 

  To remove the source files after copying use --remove-source-files option:


      	rsync -rva --remove-source-files dir (username)@(servername/ipaddress):/home/user/dir
