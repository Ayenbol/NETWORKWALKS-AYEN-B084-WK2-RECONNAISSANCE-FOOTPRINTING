# NETWORKWALKS-AYEN-B084-WK2-RECONNAISSANCE-FOOTPRINTING
WEEK 2 PROJECTS REPORT

# Penetration Testing & Ethical Hacking: Week 2 Final Report
Focus Area: Reconnaissance, Footprinting, OSINT, and Network Scanning

# Environment: Kali Linux


# 1. Executive Summary
During Week 2 of the cybersecurity and penetration testing program, the primary objective was to master Information Gathering (Reconnaissance and Footprinting). Reconnaissance is the critical initial phase of any penetration test or security assessment, divided into passive reconnaissance (collecting data without direct interaction) and active reconnaissance (interacting with target infrastructure).

This report documents the hands-on implementation and findings using key Kali Linux utilities, Zenmap, the Google Hacking Database (GHDB), and theHarvester. 


# 2. Tools Breakdown
#b2.1 Kali Linux Built-in Utilities (Domain & Web Footprinting)
Before launching deep scans, core Kali command-line utilities were utilized to footprint target domains and map their digital perimeter:


•	whois: Queried domain registration databases to determine registrar details, creation/expiration dates, and administrative contact records. 

•	whatweb: Fingerprinted web applications to identify content management systems (CMS), server technologies, web frameworks, and analytics tools.

•	nslookup & dnsrecon: Performed DNS enumeration to discover associated IP addresses, mail servers (MX records), and subdomain structures. 

•	wafw00f: Detected the presence of Web Application Filters (WAFs) protecting target web assets. 

# Evidences

# 2.2 Zenmap (Network Discovery & Port Scanning)

Zenmap, the official graphical user interface (GUI) for Nmap, was used for active network discovery and vulnerability mapping: 


•	Operational Scope: Executed various scan profiles (such as Intense Scan, Ping Sweep, and Quick Scan).

•	Key Findings: Successfully identified live hosts, open TCP/UDP ports, running service versions, and underlying operating systems. 

# Evidences

 
# 2.3 Google Hacking Database (GHDB) & Google Dorking

Search engine reconnaissance was conducted utilizing advanced operators via the Google Hacking Database (GHDB): 


•	Technique: Deployed specialized search strings ("Google Dorks") combining parameters like site:, inurl:, intitle:, and filetype:.

•	Target Scope: Located exposed configuration files, directory listings, login portals, error logs, and sensitive documentation indexed unintentionally by search engines.

# Evidences


# 2.4 theHarvester (Open Source Intelligence & OSINT)

theHarvester was utilized to aggregate publicly available intelligence regarding the target organization's external attack surface;
theHarvester -d targetdomain.com -l 300 -b all -f report.html
•	Data Sourcing: Gathered email addresses, employee names, virtual hostnames, and subdomains by querying multi-source data repositories (including public search engines, PGP key servers, and Certificate Transparency logs).

# Evidences

# 3. Summary of Findings:

1.	Attack Surface Visibility: Passive OSINT tools like theHarvester and GHDB proved that organizations often leak significant internal metadata (naming conventions, employee emails, and tech stacks) publicly.

2.	Perimeter Misconfigurations: Zenmap scans revealed instances where unnecessary management ports and outdated services were left exposed to the internet.

3.	Defense-in-Depth Necessity: Reconnaissance highlighted that security begins before exploitation; securing DNS zones, configuring robust robots.txt files, and hiding software version banners drastically reduce an attacker's preliminary intelligence yield.

# 4. Conclusion

Week 2 successfully reinforced the foundational steps of penetration testing. By combining command-line utilities, GUI-based scanners like Zenmap, intelligence gatherers like theHarvester, and advanced search queries via the Google Hacking Database, a thorough and comprehensive target profile was compiled. These insights form the crucial prerequisite phase for vulnerability assessment and exploitation phases in subsequent weeks.

