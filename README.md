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

<img width="738" height="705" alt="image" src="https://github.com/user-attachments/assets/1cf79606-7fd7-4627-b974-1eba9d515f82" />

<img width="1266" height="430" alt="image" src="https://github.com/user-attachments/assets/ae43b8f1-2e6c-4c5d-a6c0-706e35a75791" />

<img width="542" height="472" alt="image" src="https://github.com/user-attachments/assets/25c6e1dc-3644-4056-a217-17b06fba3ce4" />

<img width="1259" height="554" alt="image" src="https://github.com/user-attachments/assets/cbb1f1df-49e5-4bd6-a318-16451330b3a4" />

<img width="656" height="473" alt="image" src="https://github.com/user-attachments/assets/2237508f-e3e6-4ff2-b321-aa7a6b193869" />

<img width="1061" height="620" alt="image" src="https://github.com/user-attachments/assets/b7faa9b1-d757-4618-b6a5-2b62b5145eab" />




# 2.2 Zenmap (Network Discovery & Port Scanning)

Zenmap, the official graphical user interface (GUI) for Nmap, was used for active network discovery and vulnerability mapping: 


•	Operational Scope: Executed various scan profiles (such as Intense Scan, Ping Sweep, and Quick Scan).

•	Key Findings: Successfully identified live hosts, open TCP/UDP ports, running service versions, and underlying operating systems. 

# Evidences

<img width="481" height="385" alt="image" src="https://github.com/user-attachments/assets/8885576e-4978-40c7-8a1c-b2e0540a53a7" />

<img width="681" height="684" alt="image" src="https://github.com/user-attachments/assets/f1a2fc9f-6028-4bc9-9bd1-23c49d30012f" />

<img width="1365" height="723" alt="image" src="https://github.com/user-attachments/assets/b381314e-9c8f-4a07-9559-9f146425eb06" />


 
# 2.3 Google Hacking Database (GHDB) & Google Dorking

Search engine reconnaissance was conducted utilizing advanced operators via the Google Hacking Database (GHDB): 


•	Technique: Deployed specialized search strings ("Google Dorks") combining parameters like site:, inurl:, intitle:, and filetype:.

•	Target Scope: Located exposed configuration files, directory listings, login portals, error logs, and sensitive documentation indexed unintentionally by search engines.

# Evidences

<img width="1247" height="631" alt="image" src="https://github.com/user-attachments/assets/e63e81f3-12c7-4f9e-9cf7-583a4c301e4e" />

<img width="1287" height="520" alt="image" src="https://github.com/user-attachments/assets/e3c57582-f6d6-45a4-bd1a-84bd58146d27" />

<img width="810" height="377" alt="image" src="https://github.com/user-attachments/assets/8b3c159c-c8d3-47ae-9c9f-92ee9161d79c" />


# 2.4 theHarvester (Open Source Intelligence & OSINT)

theHarvester was utilized to aggregate publicly available intelligence regarding the target organization's external attack surface;
theHarvester -d targetdomain.com -l 300 -b all -f report.html
•	Data Sourcing: Gathered email addresses, employee names, virtual hostnames, and subdomains by querying multi-source data repositories (including public search engines, PGP key servers, and Certificate Transparency logs).

# Evidences

<img width="838" height="666" alt="image" src="https://github.com/user-attachments/assets/372566f4-3760-4773-b3c2-9df4c8f73e93" />

<img width="549" height="709" alt="image" src="https://github.com/user-attachments/assets/b51a2014-cda2-43fb-a8ce-47132b1b2492" />



# 3. Summary of Findings:

1.	Attack Surface Visibility: Passive OSINT tools like theHarvester and GHDB proved that organizations often leak significant internal metadata (naming conventions, employee emails, and tech stacks) publicly.

2.	Perimeter Misconfigurations: Zenmap scans revealed instances where unnecessary management ports and outdated services were left exposed to the internet.

3.	Defense-in-Depth Necessity: Reconnaissance highlighted that security begins before exploitation; securing DNS zones, configuring robust robots.txt files, and hiding software version banners drastically reduce an attacker's preliminary intelligence yield.

# 4. Conclusion

Week 2 successfully reinforced the foundational steps of penetration testing. By combining command-line utilities, GUI-based scanners like Zenmap, intelligence gatherers like theHarvester, and advanced search queries via the Google Hacking Database, a thorough and comprehensive target profile was compiled. These insights form the crucial prerequisite phase for vulnerability assessment and exploitation phases in subsequent weeks.

