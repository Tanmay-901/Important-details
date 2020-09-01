# Uninstall GRUB and use Windows bootloader  
Referance: [askubuntu](https://askubuntu.com/questions/429610/uninstall-grub-and-use-windows-bootloader)  
----------------------------------------------------------------
### Where `bootrec /fixmbr`, `bootsect /nt60` and the Ubuntu live with the `boot-repair` suggestions have failed, this has worked  
----------------------------------------------------------------
### follow these steps to remove Ubuntu completely from dual boot:  
(After deleting the partition in which ubuntu was installed)  
1. Run a cmd.exe process with administrator privileges  
2. Run `diskpart`  
3. Type: `list disk` then `sel disk X` where _X is the drive your boot files reside on_  
4. Type `list vol` to see all partitions (volumes) on the disk (the **EFI volume will be formatted in FAT**, others will be NTFS)   
5. Select the EFI volume by typing: `sel vol Y` where _Y is the SYSTEM volume_ (this is almost always the EFI partition)  
6. For convenience, assign a drive letter by typing: `assign letter=Z:` _)where Z is a free (unused) drive letter_  
7. Type `exit` to leave disk part  
8. While still in the cmd prompt, type: `Z:` and hit enter, where Z was the drive letter you just created.  
9. Type `dir` to list directories on this mounted EFI partition  
10. If you are in the right place, you should see a **directory called EFI**  
11. Type `cd EFI` and then `dir` to list the child directories inside EFI  
12. Type `rmdir /S ubuntu` to delete the ubuntu boot directory  


