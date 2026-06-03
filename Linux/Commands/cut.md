

###   cut - remove sections from each line of files



  The -b option will only select the first byte  in each line of the line:


	cut -b 1 file2.txt 




Other popular optoins are -c: selects by character, -d: selects by delimeter.
  and the -f: selects by field.



  Using the -b option with by adding numbers select other bytes:


	cut -b 7,8,9,10,11 file2.txt 

  
 Or if the bytes are sequential:


	cut -b 7-11 file2.txt




  Using the -d to set deleimter and the -f for the field:


	cut -d ":" -f 1 /etc/passwd 
