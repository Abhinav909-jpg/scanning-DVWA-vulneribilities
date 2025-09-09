# scanning-DVWA-vulneribilities
My First Web Application Vulnerability Scanning Project

Project Objective
This project demonstrates my ability to set up a web server environment, configure a vulnerable web application, and use a professional-grade tool (OWASP ZAP) to identify common security vulnerabilities. This project was a hands-on learning experience that focused heavily on practical troubleshooting and problem-solving skills.

Tools Used
• Operating System: Kali LinuxWeb 
• Server: Apache2
• Database: MariaDB
• Vulnerable Application: Damn Vulnerable Web Application (DVWA)
• Vulnerability Scanner: OWASP ZAP (Zed Attack Proxy)

The Journey: A Troubleshooting Odyssey
The path to completing this project was not straightforward. It was a valuable lesson in persistence and Linux system administration. I had to solve several key challenges:
1. LAMP Stack Installation: Initial attempts to install Apache, PHP, and MariaDB failed due to outdated package names and broken dependencies. I learned to use sudo apt install with the correct package names (mariadb-server instead of mysql-server) and manage service dependencies.
2. Service Management: I discovered that services on Kali Linux do not start automatically after a reboot. I learned to manually start and check the status of my web and database servers using systemctl.
3. Git & SSL Errors: A major hurdle was a "certificate signer not trusted" error when attempting to clone the DVWA repository from GitHub. I debugged this by updating my system's ca-certificates and learned how to temporarily bypass SSL verification with git config --global http.sslVerify false for a specific user.
4. Web Application Configuration: After the DVWA files were cloned, I encountered a series of blank pages and database connection errors. I debugged this by:
• Fixing my PHP file's syntax (<?php phpinfo(); ?>).
• Editing the DVWA configuration file to use the root user for database access.
• Enabling PHP error reporting to reveal the underlying database connection issue.
• Finally, running the DVWA setup to create the necessary database tables.

Key Findings and Vulnerabilities
Using OWASP ZAP, I successfully performed an automated scan on the DVWA application and identified several vulnerabilities. Below are some of the key findings, with evidence captured from the scan:
1. Cross-Site Scripting (XSS)
2. Directory BrowsingDescription
3. Server Information Leakage

Conclusion
This project has been an invaluable learning experience. It taught me that real-world cybersecurity work is not just about using tools, but about understanding the underlying systems and having the persistence to troubleshoot complex problems. I am confident that the skills I have gained will be a strong foundation for my future in cybersecurity.
