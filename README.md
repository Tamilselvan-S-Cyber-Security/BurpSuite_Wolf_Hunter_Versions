# Wolf Hunter - Burp Suite Extension

**Developer:** S.Tamilselvan  
**Organization:** Cyber Wolf

## Overview

Wolf Hunter is a comprehensive vulnerability scanner extension for Burp Suite that automatically detects and reports various security vulnerabilities across all categories and security levels. It provides a GUI-based interface for API testing and vulnerability management.

## Features

### Vulnerability Detection
- **JWT Validation Issues** - Detects weak JWT tokens, missing validation, and security misconfigurations
- **Cookie Security** - Identifies insecure cookies, HttpOnly flags, Secure flags, and SameSite issues
- **CSRF Vulnerabilities** - Detects missing CSRF tokens and weak protection mechanisms
- **Path Traversal** - Identifies directory traversal vulnerabilities
- **Directory Forcing** - Discovers hidden directories and files
- **SQL Injection** - Detects all types of SQL injection vulnerabilities (union-based, error-based, blind, time-based)
- **Custom Payload Injection** - Supports custom payload injection for various attack vectors
- **API Security Testing** - Comprehensive API endpoint testing

### Results Management
- **Table View** - Organized display of all discovered vulnerabilities
- **Export Functionality** - Export findings to:
  - PDF format
  - CSV format
  - JSON format
  - Excel format

### Threat Modeling
- Categorizes vulnerabilities by security level
- Threat level classification
- Risk assessment


### Step 1: Load in Burp Suite

1. Open Burp Suite
2. Go to **Extensions** → **Installed**
3. Click **Add**
4. Select the generated JAR file from `wolf-hunter-1.0.0.jar`

## Usage

1. Start Burp Suite and ensure the extension is loaded
2. Navigate to the "Wolf Hunter" tab
3. Configure scan settings
4. Start passive and active scanning
5. Review findings in the results table
6. Export results as needed


# Wolf Hunter - New Features

##  Right-Click Context Menu Scanning

### Accessing the Context Menu
Right-click on any request/response in Burp Suite to access Wolf Hunter scan options.

### Menu Options

#### 1. **Scan Selected Items**
- Performs passive scanning on selected requests/responses
- Automatically detects vulnerabilities
- Captures full request/response details
- Adds findings to the results table

#### 2. **Deep Scan (Full Analysis)**
- Comprehensive analysis combining:
  - **Passive Scanning**: Analyzes existing request/response data
  - **Active Scanning**: Actively tests for vulnerabilities by injecting payloads
  - **Full Request/Response Capture**: Stores complete request and response details
- Provides the most thorough vulnerability detection

#### 3. **Scan For... (Specific Vulnerability Types)**
- **SQL Injection**: Targeted SQL injection testing
- **JWT Issues**: JWT token validation checks
- **CSRF**: CSRF protection analysis
- **Path Traversal**: Directory traversal detection
- **Cookie Security**: Cookie security analysis
- **All Vulnerabilities**: Complete scan for all types

#### 4. **Add Selected to Results**
- Manually add requests/responses to results table
- Useful for marking items for later analysis
- Creates info-level entries for manual review

##  Enhanced Vulnerability Details

### Full Request/Response Information
Each vulnerability now includes:

- **Full Request**: Complete HTTP request with headers and body
- **Full Response**: Complete HTTP response with headers and body
- **Request Headers**: All request headers
- **Response Headers**: All response headers
- **Response Status**: HTTP status code
- **Request Length**: Size of request body
- **Response Length**: Size of response body

### Detailed View Panel
When you select a vulnerability in the table:

- **Complete Details**: All vulnerability information in organized format
- **Evidence**: Full evidence of the vulnerability
- **Payloads**: Injection payloads used/ detected
- **Recommendations**: Security recommendations
- **Additional Information**: Full request/response data

## Auto-Scanning Features

### Passive Auto-Scanning
- Automatically scans all HTTP traffic passing through Burp Proxy
- Real-time vulnerability detection
- No manual intervention required
- Results appear automatically in the table

### Active Scanning
- Triggered via:
  - Right-click → "Deep Scan"
  - Manual scan button
- Injects payloads to test for vulnerabilities
- Tests for:
  - SQL Injection
  - Path Traversal
  - Custom Payload Injection
  - Directory Forcing

## Understanding Vulnerabilities

### Vulnerability Information Structure

Each vulnerability includes:

1. **ID**: Unique identifier
2. **Severity**: Critical, High, Medium, Low, Info
3. **Type**: Vulnerability category
4. **Title**: Brief description
5. **Description**: Detailed explanation
6. **URL**: Affected endpoint
7. **Method**: HTTP method (GET, POST, etc.)
8. **Parameter**: Affected parameter (if applicable)
9. **Payload**: Attack payload used
10. **Evidence**: Proof of vulnerability
11. **Recommendation**: How to fix
12. **Full Request/Response**: Complete traffic capture

### Color-Coded Severity

- **Critical**: Red background
- **High**: Orange background
- **Medium**: Yellow background
- **Low**: Green background

##  Usage Guide

### Basic Workflow

1. **Passive Scanning**:
   - Proxy traffic through Burp Suite
   - Vulnerabilities detected automatically
   - View in "Wolf Hunter" tab

2. **Right-Click Scanning**:
   - Select requests in Proxy/Repeater/Intruder
   - Right-click → "Wolf Hunter" → Choose scan type
   - Results appear in table

3. **Deep Analysis**:
   - Right-click → "Wolf Hunter" → "Deep Scan"
   - Full active + passive scanning
   - Complete request/response capture

4. **Review Findings**:
   - Click on vulnerability in table
   - View full details in Details panel
   - Review request/response tabs
   - Export findings as needed

### Best Practices

- **Use Deep Scan** for critical endpoints
- **Review Full Request/Response** for context
- **Export Results** regularly for documentation
- **Filter by Severity** to prioritize critical issues
- **Use Manual Add** to track items of interest

##  Export Features

Export vulnerabilities in multiple formats:

- **PDF**: Professional reports with detailed analysis
- **CSV**: Spreadsheet format for analysis
- **JSON**: For integration with other tools
- **Excel**: XLSX format with formatting

All exports include:
- Full vulnerability details
- Request/response information
- Recommendations
- Evidence and payloads

##  Future Enhancements

The extension is designed to be easily extensible:

- Add custom vulnerability scanners
- Create custom payload sets
- Integrate with other security tools
- Add more export formats
- Enhanced filtering and search

---

**Developer**: S.Tamilselvan  
**Organization**: Cyber Wolf 


## License

Copyright © S.Tamilselvan - Cyber Wolf 


