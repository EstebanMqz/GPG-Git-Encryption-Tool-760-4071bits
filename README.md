<div align="center"><h2><b>3072-bit RSA public GPG Encryption keys</h2></div></b>

---
<div align="left">


[![Windows](https://img.shields.io/badge/Windows-0078D6?style=flat&logo=windows)](https://www.microsoft.com/en-us/windows/) &nbsp; [![GPG Encryption](https://img.shields.io/badge/GPG_Encryption-0093D6?style=flat&amp;logo=gnu-privacy-guard&amp;logoColor=white)](https://www.gnupg.org/)

</div>

There are plenty of time consuming encryption programs, nevertheless git provides most of the best encryptions right from your terminal. <br>
This is due to the fact of git file(s) processing efficiency as you already know. <br>

A file anyone must be wanting to encrypt if using Windows OS might be the .crd: <br>

``` cmd
rem Back Up @ PATH
rundll32.exe keymgr.dll,KRShowKeyMgr %USERNAME%.crd 
rem Read saved .crd
rundll32.exe keymgr.dll,KRShowKeyMgr PATH.crd
rem Encrypt.crd...
```

GPG 3072-bit <i>(high)</i> encryption: <br>

1. <b>Create</b> encryption GPG key

``` bash
gpg --gen-key # Create GPG key with default options.
gpg --full-generate-key # Create GPG key with advanced options.
gpg --list-keys # Retrieve GPG (Confirm).  
```
<br>

Either if selecting <i>Advanced / Default</i> options <i><b>Encryption key</i></b> <br>
the user will be prompted among others for: <br>

+ `<Name>`
+ `<Email>`
+ `<Passphrase>`

<br>

+ <i>key(s) deletion:  <br><br>

    ``` bash
    gpg --delete-keys #Delete public keys.
    gpg --delete-secret-keys #Delete secret keys.
    ```

</i>
<br>

1. Add encryption key to Environment <b>PATH</b> for further use:

``` bash
which gpg # Obtain key PATH.
export PATH=$PATH:/usr/bin/ && echo $PATH # Export GPG keys to System Env & confirm.   
```

<br>

3. <b>GPG file(s) encryption</b> with key:

``` bash
gpg --encrypt --recipient <Email> <path/filename>
git rm <filename> -f #Keep Encrypted GPG file(s).
```
<br>

+ <i>&#9729; Cloud Back-up:

    ``` bash
    gpg --decrypt Key.crd.gpg > Key.crd
    rundll32.exe keymgr.dll,KRShowKeyMgr PATH.crd
    ```
    
</br></i>

###### References:
<font size="2"><i>Extensions</i></font><br>
+ [Git Windows crd](https://github.com/microsoft/Git-Credential-Manager-for-Windows)
+ [.crd](https://github.com/microsoft/Git-Credential-Manager-for-Windows)<br>
+ [.gpg](https://www.gnupg.org/gph/en/manual/x110.html)



