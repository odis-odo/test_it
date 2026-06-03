
Print the fifth column (a.k.a. field) in a space-separated file:  

```bash
awk '{print $5}' path/to/file
```

<br>

Selecting columns from output of a command:

```bash
ls -lh | awk '{ print $5,"\t", $9}'
```  

- `"\t"` is the tab charater to space out the row in the output.

<br>

Filtering rows from output of command matching keyword:

```bash
ls -lh | awk '/keyword/ { print $5,"\t", $9 }'
```  

<br>

Searching for two key words using  `&&`:  

```bash
awk '/bandit/ && /Level/ {print}' over_the_wire.txt 
```  

This will search for bandit and Level and will print the lines they are on.  

<br>  

Displaying the last column with a field seperator and pattern searching:  

```bash
awk -F "/" '/^\// {print $NF}' /etc/shells 
```  

- `-F "/"` is the field sperator using the `/` to sperate the fields
- `'/^\//'` is searching the pattern ` ^/` but needs  `\` in front of the outer slashes to escape it.
- `{print $NF}` this will print the last field using the `$NF` variable





