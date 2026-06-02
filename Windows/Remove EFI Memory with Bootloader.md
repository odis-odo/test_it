
After deleting the Linux partition when removing a dual boot on the same drive  boot up **CMD** as an admin  

1. Type `bcdedit /enum firmware` and hit enter.
2. Look for the Linux Partition Identifier. Ex `EFI\linuxdistro\shimx64.efi`
3. Highlight the Identifier `{#######-}` and copy it with right click
4. `bcdedit /delete {#######-}`  <-----Pasted code from step 3. Include the {} brackets as well.