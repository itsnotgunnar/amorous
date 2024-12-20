# Amorous.ps1

**Amorous.ps1** is a PowerShell script designed to search through files on a Windows system for potential sensitive information. It looks for patterns like usernames, passwords, API keys, and other secrets that might be stored in various types of files. The goal is to help you quickly identify where sensitive data might be hiding so you can take steps to secure it.

## How It Works

1. **File Search**:  
   The script scans through your system, looking for files that match a wide range of common file extensions and keywords related to sensitive data. This includes text files, configuration files, logs, and more.

2. **Keyword & Pattern Matching**:  
   Once it finds files of interest, it checks their content for known patterns—like lines that look like passwords or API tokens. By using a variety of pre-defined regular expressions, it catches both obvious and subtle credentials.

3. **Optional Custom Words**:  
   You can optionally provide a file that contains additional custom keywords to search for. If you do, it will include these in its search. If not, that’s okay—it will still run perfectly fine with its built-in patterns.

4. **Logging & Output**:  
   The script writes its findings to log files in a designated directory. You’ll get a summary of what it found, making it easier to review and act on the results.

## Why Use It?

- **Security Auditing**: Get a quick overview of where potential secrets might be stored.
- **Compliance Checks**: Identify sensitive information before audits or compliance reviews.
- **Breach Prevention**: Spot insecure data storage before attackers do.

## Getting Started

1. **Prerequisites**:  
   - PowerShell (built-in on Windows).
   - Administrator privileges are recommended if you want to scan system directories.

2. **Running the Script**:  
   Open a PowerShell window and run:
   
   ```powershell
   .\amorous.ps1 # -w "C:\Path\to\customWords.txt"
   ```

3. **Reviewing Results**:
   After the script completes, it will tell you where the log files are located. Check these logs to see what was found and take steps to secure or remove any sensitive information.

## Notes

- The script may take time to complete, especially if scanning the entire C:\ drive.
- This was created to sweep CTF machines to isolate files that are out of the norm.
- Tweaking extensions and words to search for is encouraged, though not needed
