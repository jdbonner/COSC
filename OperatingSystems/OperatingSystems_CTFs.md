# Windows_PowerShell
    Level 1:
    Primer_CLI(1)
    1.conhost.exe
    2.WSL
    3.Windows Terminal
    4.cmd.exe
    5.string
    6.(.NET)
    7.PowerShell version
    8.pwsh.exe
    9.PowerShell.exe
    Level 5:
    Windows_PowerShell_Basics(5)
    1.verb-noun
    2.get-command
    3.get-verb
    4.objects
    5.properties,methods
    6.get-member
    Windows_PowerShell_Alias(5)
    1.get-alias
    2.get-childitem {gci}
    Windows_PowerShell_Help(5)
    1.get-help
    2.-full
    3.update-help
    4.-online
    Windows_PowerShell_Interaction(5)
    1.start chrome
    2.(get-process chrome).kill()
    3.stop-process -name chrome
    Windows_PowerShell_CIMClasses(5)
    1.get-WMIobjectWin32_processor
    Windows_PowerShell_Logic(5)
    1.get-content
    2.measure-object
    Windows_PowerShell_REGEX(5)
    1.select-string
    Windows_PowerShell_Basics(5)
    7.(C:\Users\)
    Windows_PowerShell_Basics(10)
    8.> (get-process | get-member -membertype property).count
        value is: 52
    Windows_PowerShell_Alias(10)
    3. 3
    Windows_PowerShell_Help(10)
    5. > Get-Process Powershell
    Windows_PowerShell_CIMClasses(10)
    2. > Get-WMIObject WIN32_service | ?{$_.Name -like "legoland"} | select Description
    answer: i_love_legos
    Windows_PowerShell_Logic(10)
    3. > Get-Content words2.txt | Measure-Object -Word
        Answer: 5254 words
    4. > (Get-ChildItem | Measure-Object).count
        Answer: 925 files
    5. > Compare-Object -referanceobject (Get-Object old.txt) -differenceobject (get-content new.txt)
        Answer: Popeye
    6. > Get-Content words.txt | Sort-Object -descending | Selct-Object -index 21
        Answer: ZzZp
    7. > (Get-Content words.txt | Sort-Object | Get-Unique).count
        Answer: 456976
    Windows_PowerShell_Basics(10)
    9. > (Get-Process | Get-Member -membertype method).count
    Windows_PowerShell_Logic(10)
    8. > (Get-ChildItem -recurse | Where-Object {$_.PSIsContainer}).count
        Answer: 411
    Windows_PowerShell_REGEX(10)
    2.> (Get-Content words.txt |  select-string -allmatches "gaab").count
        Answer: 1
    3.> (Get-Content words.txt | Where-Object {$_ -match '(a|z)'}).count
        Answer: 160352
    4.> (Get-Content words.txt | Where-Object {$_ -match '(az)'}).count
        Answer: 2754
    Windows_PowerShell_Logic(15)
    9.
    Windows_PowerShell_REGEX(15)
    5.> (Get-Content words.txt | Where-Object {$_ -match '((aa)[a-g])'}).count
        Answer: 357
#-----------------------------------------------------------------------------------------------

# Windows_PowerShell_Profiles

    Question 1-2: Level of Precendence Powershell Profiles
    
    1.All Users, All Hosts            $PsHome\Profile.ps1
    2.All Users, Currnet Host         $PsHome\Microsoft.PowerShell_profile.ps1
    3.Current User, All Hosts         $Home\[My]Documents\Profile.ps1
    4.Current User, Current Host      $Home\[My ]Documents\WindowsPowerShell\Profile.ps1

    Question 3: Which PowerShell variable stores the current user's home directory?
    
    > $home
    Question 4: Which PowerShell variable stores the installation directory for PowerShell?
    
    > $PSHome
    Question 5: Which PowerShell variable stores the path to the "Current User, Current Host" profile?

    > $profile
    Question 6: What command would you run to view the help for PowerShell Profiles?

    > get-help about_profiles
    Question 7: What command would tell you if there was a profile loaded for All Users All Hosts?
    Flag is the full command syntax

    > Test-Path -Path $PROFILE.AllUsersAllHosts
    Question 8: Challenge only allows ONE attempt
    Malware is running on the primary PowerShell profile on the File-Server. Based on PowerShell profile order of precedence 
    (what is read first), find the correct flag.
    The flag is the string after the #, without the preceding space.

    > I wasted my attemt.
#--------------------------------------------------------------------------------------------
    *Fuck Linux
# Linux_Basics
    Level 0:
    0.
    Level 5:
    Linux Basics(5)
    1.ls
    2.ls -hl
    3.| -pipe
    4.man -k
    Linux Basics LFS Hierarchy(5)
    _./ :(absolute path of the root(main) directory)
    2./etc :(absolute path to the default location for configuration files)
    3./bin :(Directory containing executable programs(binaries) needed in single user mode)
    4./usr/bin
    5./sbin :(binaries only root can access)
    6.> man --path cat
        Answer: /usr/share/man/man1/cat.1.gz
    Level 10:
    Linux basics(10)
    5.
    > man -k digest
    > echo "OneWayBestWay" | sha512sum
        Answer: a81bc463469ee1717fc9e388e3799c653f63a3de5e9496b5707b56488b046cbf75665235d316c
        5c0053a597dc7d40c917a2d9006fe35e9cb47766c05ac71989b
    6. 
    > file Encrypted
    > unzip Encrypted
    > file cipher
    > file symmetric
    > cat cipher
    > cat symmetric
        gives you the key & the Hashing Algoritm
    > openssl AES128 -d -in cipher
        ^use the key that was enumerated from the symmetric file
            Anwser: DeCrypt
    Linux Basics LFS Hierarchy(10)
    7.
    Linux Basics users and Groups(10)
    1.
    2.
    3.
    4.
    Linux Basics Permisions(10)
    1.
    2.
    3.
    4.
    5.
    6.
    7.
    8.
    9.
    10.
    Linux Basics Regular Expressions(10)
    1.
    2.
    3.
    4
    Linux Basics Reformat(10)
    1.
    2.
    Linux Basics Bash Logic(10)
    1.
    2.
    Level 15:
    Linux Basics Regular Expressions(15)
    1.
    2.
#---------------------------------------------------------------------------------------------

# Windows_Registry
    Level 1:
    1.HKLM\HARWARE
    2.HKLM\SOFTWARE
    3.HKLM\SYSTEM\CurrentControlSet\Services 
    4.0x0
    5.HKLM\SYSTEM\CurrentControlSet\Services
    6.0x2
    7.0x3
    8.HKLM, HKU
    9.Get-PSDrive
    10.regedit
    Level 5:
    1.HKLM
    2.HKU
    3.HKCU
    4.HKEY_USERS\S-1-5-21-2881336348-3190591231-4063445930-1002 
    5.Get-ChilItem
    6.Get-Item
    Level 10:
    7.HKLM:\SOFTWARE\MICROSOFT\WINDOWS\CURRENTVERSION\RUN *All CAPS*
    8.HKCU:\SOFTWARE\MICROSOFT\WINDOWS\CURRENTVERSION\RUN
    9.HKLM:\SOFTWARE\MICROSOFT\WINDOWS\CURRENTVERSION\RUNONCE
    10.HKCU:\SOFTWARE\MICROSOFT\WINDOWS\CURRENTVERSION\RUNONCE
    Level 15:
    11.
            *As andy.dwyer
     > reg query hklm\software\microsoft\windows\currentversion\run
     Answer: malware.exe
    12.
        *As student
     > reg query hkcu\software\microsoft\windows\currentversion\run
     Answer: C:\botnet.exe
    13.
    14.
    *As student
     > reg query hkcu\software\microsoft\windows\currentversion\runonce
     Answer: C:\worm.exe
    15.
        *As student
    > reg query HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\USBSTOR
        Answer: SanDisk9834
    16.
    17.
#---------------------------------------------------------------------------------------------

# Start_Windows_Alternate_Data_Stream
    Level 1:
    1.file system
    2.Clusters
    3.MFT-(Master File Table)
    4.attributes
    5.$DATA
    6.$LOGGED_UTILITY_STREAM
    7.$SECURITY_DESCRIPTOR
    8.0x80
    9.1024 bytes
    10.Explicit
    11.Inherited
    12.read
    13.List Folder Contents (folders only)
    14.modify
    15.full control
    16.$STANDARD_INFORMATION
    17.fsutil fsinfo drives
    Level 5:
    1.directory
    2.hidden
    3.Get-ChildItem -Force
    4.Get-FileHash -Algorithm sha512
    5.Get-Acl
    6.hosts
    Level 10:
    7.BUILTIN\Users
    8.
    9.
    10.
    11.
    12.
    Level 15:
    13.
    14.
#---------------------------------------------------------------------------------------------

# Windows_Boot_Process
    Level 1:
    Primer_Boot_Process(1)
    1.sector
    2.partition
    3.volume
    4.diskpart
    5. ?(multiple choice)
    6.HAL(multiple choice)
    7.driver
    8.UEFI and BIOS
    9.ntoskrnl.exe
    10.bootmgr and winload.exe
    11.bootmgr
    12.BCD
    13.TPM
    14.Winload.exe
    15.Ntoskrnl.exe
    16.0x2
    17.smss.exe
    18.session 0
    19.secure boot
    20.
    21.HKLM\Software\Microsoft\Windows\CurrentVersion\RunServices
    22.local logon
    23.userinit.exe
    24.Winlogon.exe
    25.Lsass.exe
    26.Last Known Good Configuration
    27.Kerberos
    28.Key Distribution Center
    29.logon
    Primer_Kernel(1)
    1.hybrid
    2.monolithic
    3. 6.1
    4. 10
    5.
    Level 5:
    Windows_Boot_INIT(5)
    1.System
    2. 4
    3.smss
    4. 0
    5.lsass
    6.services
    7.winlogon
    8.userinit
    9.winload.exe
    10.BIOS
    11.hiberfil.sys
    12.winresume.exe
    Level 10:
    windows_Boot_Remediate(10)
    1.
    2.
    3.
    4.
    5.
#---------------------------------------------------------------------------------------------
# Start_Linux_Boot_Process

#---------------------------------------------------------------------------------------------
# Start_Windows_Process

#---------------------------------------------------------------------------------------------
# Start_Windows_UAC

#---------------------------------------------------------------------------------------------
# Start_Windows_Services

#---------------------------------------------------------------------------------------------
# Start_Linux_Process

#---------------------------------------------------------------------------------------------
# Start_Windows_Auditing_and_Logging

#---------------------------------------------------------------------------------------------
# Start_Linux_Auditing_and_Logging

hello
#---------------------------------------------------------------------------------------------
# Start_Windows_Analysis
this is a random input(It Merged)
#---------------------------------------------------------------------------------------------
# Start_Windows_active_Directory
