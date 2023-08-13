# File-Integrity-Monitoring-tool
Simple Powershell script implementing a FIM (File Integrity Monitoring) solution. It prints out if a certain monitored file diverges from a previously set up baseline. Two baseline files are created: one for hashes and one for file size. Whenever a file has been changed, the new hash and file size is printed.
