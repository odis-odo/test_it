<br>

### tar and gzip (archiving files)

<br>

  Using the -c option is to create the tar file and the f option will provide a filename:

	tar -cf testdir_backup.tar TestDIr/

  The file name of the tar file comes first followed by the directory to archive.

<br>

   The -t option will list whats inside a tar file without extracting it:

	tar -tf testdir_backup.tar

   Also use the f option so that it tar knows its a file.

<br>

The -v option will show additional information in the output:

	tar -tvf testdir_backup.tar

<br>

   The -x option will extract the contents of the file:

	tar -xf testdir_backup.tar

   Also add the f option as well and can also add the v option as well for additonal
   information.




 -----------------------------------------------------------------------




Basic usage of the gzip command:

	gzip  (file to compress)

<br>

   To uncompress a file that has been compressed:

	gunzip (file to uncompress)

<br>

 
   To compress a tar file with gzip use the -z option will compress the tar file
   using gzip in the same command. So you dont have to pipe it into gzip itself:


	tar -czf testdir_back.tar.gz TestDIr/

<br>

   The -v option can be added as well for addtional information:

	tar -czvf testdir_back.tar.gz TestDIr/
   
<br>
   
   To view the contents of the file is the same as in viewing a tar file:

	tar -tvf testdir_back.tar.gz

<br>

   Extracting the file is the same as well:

	tar -xvf testdir_back.tar.gz





   
   
   





  



