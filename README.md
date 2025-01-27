# XML-Testing Automation
An interactive and flexible tool for automating penetration testing and bug bounty tasks focused on XML vulnerabilities, including XXE, XML Injection, XSS, and File Disclosure. Designed for ease of use with real-time results and clear Proof of Concept (PoC) for vulnerabilities.

# Features
# XML Vulnerability Testing:
XXE (XML External Entity) Injection
XML Injection and malformed structures
XSS and script injection
Path traversal and file disclosure
# Payload Options:
Use built-in default payloads for quick testing.
Support for custom payloads loaded from a file.
Wayback Integration (Newly Added Feature):
Automatically search the Wayback Machine for live XML files related to a given domain.
Display results dynamically as files are discovered.

# Installation
Clone the repository
```bash git clone https://github.com/yourusername/xml-pentest-tool.git```

Navigate to the tool directory
```bash cd xml-pentest-tool```

Install Python dependencies
```bash pip install -r requirements.txt```

# Install Waybackurls (Required for Wayback Integration):
 Ensure Go is installed. If not, install it using:
```bash sudo apt install golang```

Install Waybackurls
```bash go install github.com/tomnomnom/waybackurls@latest```

Add Waybackurls to your PATH
```bashexport PATH=$PATH:$(go env GOPATH)/bin```

Run the tool:
```bash python3 xml_pentest_tool.py```

# Example 

Choose input type:
1. Load XML from a file
2. Test a URL endpoint
3. Search for XML files using Wayback Machine
4. Exit the tool
Enter your choice (1, 2, 3, or 4): 3

🔍 Searching Wayback Machine for XML files on domain: example.com
✅ Found 5 XML files. Displaying live:
[1] http://example.com/sitemap.xml
[2] http://example.com/filelist.xml
[3] http://subdomain.example.com/wp-sitemap.xml
...


![image](https://github.com/user-attachments/assets/47a7a1c8-eb57-4ea7-b134-7344d196c9ea)
![image](https://github.com/user-attachments/assets/1bfbdc93-6b40-4aea-9287-e5dd553cdd06)
![image](https://github.com/user-attachments/assets/97d39180-25e9-4c9e-8394-80df6149b8dc)
