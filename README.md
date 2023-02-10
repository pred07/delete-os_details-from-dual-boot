# delete-os_details-from-dual-boot
Windows environment

1. Run cmd in administrator mode.

2. type >> diskpart

3. type >> list volume

    (we can see volume names, assigned letters, label and so on.
     some volumes may not have assigned letters so we need to assing manually.)
     
4. (select volume name) 

    eg >> select volume 1 
    
5. (assign letter) 

    eg >> assign letter=m (a unique letter that must not be the assigned letter of other volumes)
    
6. Repeat step 4 then step 5 for all volumes with no letters assigned.

7. type >> exit 

8. (get into all volumes and check for dual boot details)
   (enter volume letter) 
   
    eg >> m:
    
9. type >> cd efi (if error occour chage volumes letter and try) eg >> n:

10.if it enters to efi 

    type >> dir (we can see dual boot os name)
    
11.(Delete it)

    (command -- rd (os_name) /s)
    
    eg >> rd ubuntu /s
    (enter y and continue)
    
    RESTART THE COMPUTER
