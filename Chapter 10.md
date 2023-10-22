## Uncovering the Hidden: Directory Scanning

---

Directory scanning is an essential technique used in the realm of cybersecurity to discover hidden or non-linked directories and files within a web server. It unveils the unseen structure of the web application, which might contain sensitive information or poorly protected assets. Let’s delve into one of the robust commands used for directory scanning, exploring dirsearch and dissecting a typical command to understand its intricacies.

### 1. **The Tool: dirsearch**

dirsearch is a simple command line tool designed to brute force directories and files in websites. It's equipped with a suite of options to tailor the scanning process according to your needs. To be clear, this command is definitely overkill for most CTF challenges you will encounter as it will take a very long time and challenges are usually setup in a way to be fast for learning.

### 2. **Breaking Down the Command**


```
dirsearch -u $target -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -f -e php,tar.gz,config,conf,zip,rar,txt,sh,py -H "X-Custom-IP-Authorization: 127.0.0.1"`
```

- **`-u $target`**:
    
    - The `-u` flag specifies the URL of the target website.
    - `$target` is a placeholder for the actual target URL, e.g., [http://example.com](http://example.com/).
- **`-w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt`**:
    
    - The `-w` flag specifies the wordlist to be used for the brute force process.
    - In this case, a wordlist from DirBuster is utilized.
- **`-f`**:
    
    - This flag forces dirsearch to perform a full scan, ignoring any previously saved scans or data.
- **`-e php,tar.gz,config,conf,zip,rar,txt,sh,py`**:
    
    - The `-e` flag specifies the file extensions dirsearch should look for.
    - Multiple extensions are provided, separated by commas, enabling a wide search for various file types.
- **`-H "X-Custom-IP-Authorization: 127.0.0.1"`**:
    
    - The `-H` flag allows for custom headers to be added to the requests sent by dirsearch.
    - In this instance, a custom IP authorization header is added, which may be useful in bypassing certain IP-based restrictions on the target server.

The simplified version of this command will be:
```
dirsearch -u example.com
```

Keep in mind however you can simply add on custom wordlists or extensions we discussed previously.
### 3. **Why is Directory Scanning Important?**

- **Uncovering Hidden Resources**: There could be poorly protected or hidden directories and files which are not linked within the main application.
- **Identifying Potential Vulnerabilities**: Certain directories or files might expose sensitive information or have weaker security configurations.
- **Information Gathering**: Collecting a comprehensive list of directories and files to build a better understanding of the web application's structure.

### 4. **Additional Resources**:

- **Other Tools**:
    
    - **DirBuster**: A java application designed to brute force directories and files names on web/application servers.
    - **Gobuster**: A Go-based tool used for brute-forcing URIs (directories and files) in web sites.
- **Wordlists**:
     - **SecLists**: A collection of multiple types of lists used during security assessments, collected in one place.