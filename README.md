# Vulnscan
Simple and Basic vulnerability scanner
Sure! Here's the complete README file content for you to copy-paste:

```markdown
# Web Application Vulnerability Scanner

A simple Python-based vulnerability scanner to identify common web application vulnerabilities like **SQL Injection** and **Cross-Site Scripting (XSS)**. This tool uses the `requests` and `BeautifulSoup` libraries to perform the scans.

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)

## Features

- Scans for **SQL Injection** vulnerabilities in form parameters.
- Tests for **Cross-Site Scripting (XSS)** vulnerabilities using common payloads.
- Handles both absolute and relative URLs.
- Detects and tests form inputs for vulnerabilities.

## Requirements

- Python 3.x
- Libraries: `requests`, `beautifulsoup4`

## Installation

### Step 1: Install Python

Ensure that you have **Python 3.x** installed. You can download and install it from the official website:  
[Python Official Downloads](https://www.python.org/downloads/)

### Step 2: Install Dependencies

Once Python is installed, you’ll need to install the required Python libraries using `pip`. Open your terminal (or command prompt) and run the following command:

```bash
pip install requests beautifulsoup4
```

This will install the necessary libraries to handle HTTP requests and parse HTML.

## Usage

### Step 1: Download or Clone the Repository

If you haven’t done so yet, you can **clone** this repository to your local machine using:

```bash
git clone https://github.com/yourusername/vuln-scanner.git
```

Alternatively, you can **download** the ZIP file from the GitHub repository and extract it.

### Step 2: Update Target URL

In the script `vuln_scanner.py`, replace the target URL with the URL of the web application you want to scan. For example:

```python
target_url = "http://example.com"  # Replace with the URL you want to scan
```

### Step 3: Run the Script

Open your terminal or command prompt, navigate to the folder where the script is located, and execute the script by running:

```bash
python vuln_scanner.py
```

The script will start scanning the specified URL for common vulnerabilities such as SQL Injection and XSS. It will print the results directly in the terminal.

### Step 4: View Results

Once the scan completes, you’ll see output in your terminal indicating whether **SQL Injection** or **XSS** vulnerabilities were detected for the tested parameters (e.g., `username` and `password`). For example:

```bash
Scanning http://example.com for vulnerabilities...

Found form with action: /login
Testing parameter: username
Testing SQL Injection on: http://example.com/login?username=' OR '1'='1
No SQL Injection vulnerability detected on http://example.com/login?username=' OR '1'='1
Testing XSS on: http://example.com/login?username=<script>alert('XSS')</script>
No XSS vulnerability detected on http://example.com/login?username=<script>alert('XSS')</script>
```

### Step 5: Analyze the Results

If any vulnerabilities are detected, the scanner will print messages indicating which parameters are vulnerable (e.g., `username`, `password`). If no vulnerabilities are detected, the script will also provide feedback stating that no issues were found.

## Contributing

Contributions are welcome! Here are some ways you can help:

1. **Add new vulnerability tests**: The current scanner tests for **SQL Injection** and **XSS**. You can contribute by adding tests for other vulnerabilities like **Cross-Site Request Forgery (CSRF)**, **Command Injection**, etc.
2. **Improve error handling**: The script can be enhanced to handle more edge cases and provide better feedback.
3. **Improve performance**: The script can be optimized to handle multiple concurrent tests and large-scale scans.

To contribute, please **fork** the repository and submit a **pull request**.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

**Ethical Use**: This tool is intended for educational purposes only. Always obtain explicit permission from the website owner before running security tests on any website.

**Legal Considerations**: Unauthorized testing of websites can be illegal. Use this tool responsibly and ensure that you have the necessary permissions to scan a website.
