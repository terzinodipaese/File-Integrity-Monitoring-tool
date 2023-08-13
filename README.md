# File Integrity Monitoring tool
Simple Powershell script implementing a FIM (File Integrity Monitoring) agent. It prints out if a certain monitored file diverges from a previously set up baseline. Two baseline files are created: one for hashes and one for file size. Whenever a file has been changed, the new hash and file size is printed.

Possible new features: 1) possibility to choose the hash algorithm, possibility to choose the files and/or directories to be monitored, possibility to set the monitoring frequency (read the file every 30 seconds, for instance), 2) possibility to set server IP address and port to which send the alerts, 3) implement a client-server protocol for sending the alert to a central server, for better visibility to the entire network. The alert message format can be whatever, but it has to include the following information: baseline hash, new hash, baseline size, new size (especially useful for monitoring log files, we don't expect log files to reduce in size), client IP address where detection happened, the absolute path of the tampered file, the user who made the edit, the type of modification (changed file, deleted file, new file created), last modification timestamp (just for changed files), alert timestamp (when detection happened), plain text content of the file monitored (hash is not very human-readable), 4) implement a server-side query language for getting useful stats on the data contained in the alerts and make data aggregation.
