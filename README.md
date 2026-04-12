# Log Analysis Project

## Description
This project demonstrates basic log analysis using Linux command-line tools.

## Tools Used
- Linux (WSL)
- grep
- wc

## Tasks Performed
- Searched for failed login attempts
- Identified suspicious activity in logs
- Counted number of errors

## Findings
- Multiple failed login attempts for admin and root users
- Possible brute force attack detected

## Example Commands
grep "ERROR" logs.txt  
grep "Suspicious" logs.txt  
grep "ERROR" logs.txt | wc -l
