<br>

using the -f option with sort will sort the contents alphabetically:

	sort -f file.txt

<br>

using the -u option will remove duplicated file names:

	sort -u /var/log/syslog | wc -l


using the wc (word count) and the -l will show the number of lines.

<br>

using the -R will move the file contents at random every time its run:

	sort -R file.txt

<br>

using the -n option will sort the contents numerically if they are numbered:

	sort -n file.txt


