<br>

### tr - translate or delete characters

<br>

  The tr command when used with echo:

	echo "Hello World" | tr [a-z] [A-Z]


  The two sets of brackets are ranges that are from a-z and one is lowercase and the other
  is uppercase. The second set will replace the first set so HelloWorld changes to all 
  uppercase.

<br>

  Files can also be redirected using stdin using tr command:
  

	tr [a-z] [A-Z] < file2.txt

<br>

  To delete characters using the -d option:

	echo "Hello World" | tr -d [a-z]


  By removing the second set of brackets the  -d option just deletes the lowercase
  characters.

<br>

  The -s option will remove duplicate charaters:

	at packages.list | tr -s "l"

<br>

  Another method change case with tr instead of using ramges:

	cat file2.txt | tr [:lower:] [:upper:]

<br>

  This method will delele all the alphabet characters:


	cat file2.txt | tr -d [:alpha:]

<br>

  This method will replace chraters with other chatacters:

	cat file2.txt | tr "D" "p"



  
