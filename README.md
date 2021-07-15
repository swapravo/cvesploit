# cvesploit

## Filter SearchSploit using CVE-IDs / dpkg status file

<br/>

### CVE Mode
#### Vulnerablitiy Scanners often return the CVE-IDs in their scans.
<br/>

    ./cvesploit CVE-2018-11776

    CVE-2018-11776
        Apache Struts 2.3 < 2.3.34 / 2.5 < 2.5.16 - Remote Code Execution (1)                          exploits/linux/remote/45260.py
        Apache Struts 2.3 < 2.3.34 / 2.5 < 2.5.16 - Remote Code Execution (2)                       exploits/multiple/remote/45262.py
        Apache Struts 2 - Namespace Redirect OGNL Injection (Metasploit)                            exploits/multiple/remote/45367.rb

<br/>

### Status file Mode
#### dpkg --status -> debsecan -> searchploit -> exploits in one go!
#### dpkg --status does not require privileges
<br/>

    dpkg --status > stats
    ./cvesploit stats

    ...
    CVE-2014-6277
        Binary File Descriptor Library (libbfd) - Out-of-Bounds Crash                                    exploits/linux/dos/35081.txt
        GNU bash 4.3.11 - Environment Variable dhclient                                                exploits/linux/remote/34860.py
        dhclient 4.1 - Bash Environment Variable Command Injection (Shellshock)                        exploits/linux/remote/36933.py

    CVE-2014-6278
        GNU bash 4.3.11 - Environment Variable dhclient                                                exploits/linux/remote/34860.py
        Apache mod_cgi - 'Shellshock' Remote Command Injection                                         exploits/linux/remote/34900.py
        dhclient 4.1 - Bash Environment Variable Command Injection (Shellshock)                        exploits/linux/remote/36933.py
        Cisco UCS Manager 2.1(1b) - Remote Command Injection (Shellshock)                           exploits/hardware/remote/39568.py
        Sun Secure Global Desktop and Oracle Global Desktop 4.61.915 - Command Injection (Shellshock)  exploits/cgi/webapps/39887.txt
    ...
<br/>
