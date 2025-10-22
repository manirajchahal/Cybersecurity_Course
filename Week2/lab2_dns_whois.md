# Lab 2: DNS and WHOIS Reconnaissance

## Objective
Learn to gather information about domains using DNS and WHOIS tools.

## Prerequisites
- Understanding of DNS concepts
- Command-line experience

## Background
DNS (Domain Name System) translates domain names to IP addresses. WHOIS provides registration and ownership information about domains. Both are essential tools for reconnaissance.

## Tasks

### Task 1: DNS Enumeration
1. Query A records: `dig example.com A`
2. Query MX records: `dig example.com MX`
3. Query NS records: `dig example.com NS`
4. Query TXT records: `dig example.com TXT`
5. Perform a reverse DNS lookup: `dig -x 8.8.8.8`

### Task 2: WHOIS Lookup
1. Look up a domain: `whois example.com`
2. Identify:
   - Registrar
   - Creation date
   - Expiration date
   - Name servers
   - Registrant information (if available)

### Task 3: Subdomain Discovery
Research and document methods to discover subdomains:
1. Using search engines (Google dorks)
2. Using online tools like DNSDumpster
3. Certificate transparency logs

### Task 4: Information Analysis
Choose a real domain (your school or a public organization) and:
1. Gather DNS information
2. Gather WHOIS information
3. Create a report with findings
4. Identify potential security concerns

## Commands Reference
```bash
dig [domain] [record-type]    # DNS lookup
nslookup [domain]              # Alternative DNS lookup
host [domain]                  # Simple DNS lookup
whois [domain]                 # Domain registration info
```

## DNS Record Types
- **A**: IPv4 address
- **AAAA**: IPv6 address
- **MX**: Mail exchange servers
- **NS**: Name servers
- **TXT**: Text records (SPF, DKIM, etc.)
- **CNAME**: Canonical name (alias)
- **SOA**: Start of authority

## Deliverables
1. Complete DNS and WHOIS reports for at least 2 domains
2. Document interesting findings
3. Answer the questions below

## Questions
1. What security information can you learn from TXT records?
2. Why is WHOIS privacy important?
3. How can DNS information be used in social engineering attacks?
4. What is DNS enumeration and why is it useful in penetration testing?
5. What are the ethical considerations when gathering this information?

## Practice Domains
Safe domains to practice on (public, well-known):
- google.com
- github.com
- cloudflare.com

## Additional Resources
- [DNSDumpster](https://dnsdumpster.com/) - Online DNS reconnaissance
- [VirusTotal](https://www.virustotal.com/) - Shows DNS records and more
