## Identifying the Invisible: Software Enumeration and Detection

---

Peeling back the layers of a domain's structure further, it becomes imperative to identify the software running on each subdomain or alternative port discovered. Knowing the software and its version helps in understanding the potential vulnerabilities that could be exploited. This chapter delves into various tools and methodologies to identify software on target systems.

### 1. **Software Detection Tools:**

#### a. **Wafw00f**:

- **Purpose**: To identify and fingerprint Web Application Firewall (WAF) products protecting a website.
- **Usage**:
```
wafw00f http://targetsite.com
```

#### b. **WhatWeb**:

- **Purpose**: To identify what software, plugins, and themes a website is using.
- **Usage**:
```
whatweb http://targetsite.com
```

#### c. **httpx**:

- **Purpose**: A fast and multi-purpose HTTP toolkit to run multiple probers using retryablehttp library, it's designed to maintain the result reliability with increased speed.
- **Usage**:

```
httpx -u $target -title -tech-detect -status-code -cl -ct -location -rt -lc -wc -server -method -ip -cname -cdn -probe -silent
```

### 2. **Probing Individual Subdomains and Ports:**

After identifying subdomains and alternative ports, it's crucial to probe each to understand what software or service is running.

- **Procedure**:
    1. Utilize the aforementioned tools on each subdomain and port.
    2. Document the software and versions identified.

### 3. **Handling Forbidden Pages (403 Errors):**

Encountering a 403 Forbidden error is common and might indicate restricted access or a different path for the actual content.

- **Directory Scanning**:
    - Tools like DirBuster or dirsearch can help identify hidden directories or file paths.
    - Once a path is identified, it can be appended to the subdomain for further probing using httpx or other tools.

### 4. **In-Depth Analysis**:

For a thorough understanding, it is advisable to:

- **Run Multiple Tools**: Different tools might provide varying levels of information.
- **Manual Analysis**: Sometimes manual interaction with the web application may reveal more about the software running.

### 5. **Further Resources**:

- **Online Platforms**:
    
    - **BuiltWith**: Provides detailed information about the technologies used on a website.
    - **Wappalyzer**: Another platform to identify technologies on websites.
- **Community Resources**:
    
    - **GitHub Repositories**: Often contain custom scripts and tools for software enumeration.

---

Identifying the software running on discovered subdomains and ports is a stepping stone to understanding the security posture of a domain. The tools and methodologies discussed here equip you with the necessary skills to delve deeper into the software landscape of your target. The subsequent chapters will build upon this knowledge, guiding you on how to leverage this information to further assess the security of the domain.