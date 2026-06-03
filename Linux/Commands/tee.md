<br>

### tee - read from standard input and write to standard output and files

<br>

  basic usage of the tee command: 

	ls | tee file.txt

   this will list the output to the screen as well redirect into a text file.

<br>

   to view its own help file just add a --help after the command:

	tee --help

<br> 

you can write output to more than one file :

	ls | tee file1.txt file2.txt file3.txt

  this will  create the files and write the output to  each one.

<br>

to append to a file use the -a  option:

	ls | tee -a file1.txt

   this will not overwrite the file it will add to it . 	    




