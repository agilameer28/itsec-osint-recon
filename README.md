### Summary
Conducted passive Open-Source Intelligence (OSINT) reconnaissance on a public bug-bounty domain to map external attack surfaces without triggering intrusion detection systems.

### Environment
* **Tools:** ICANN Lookup, DNSDumpster, crt.sh
* **Concepts:** Passive Reconnaissance, DNS Record Analysis (A, MX, TXT), Certificate Transparency Logs.

### Diagnostic / Execution Steps
1. Queried WHOIS databases via ICANN to verify domain ownership and registrar data.
2. Analyzed DNS records using DNSDumpster to map email infrastructure (MX) and identify third-party hosting providers.
3. Leveraged Certificate Transparency (CT) logs via crt.sh to discover undocumented subdomains (e.g., dev/staging environments).
4. Compiled infrastructure footprint data passively, ensuring zero direct contact with the target network.

### Evidence
![DNS Mapping](evidence/dnsdumpster-recon.png)

### Lessons Learned
Publicly available DNS and certificate data provides a comprehensive roadmap of an organization's network before a single packet is sent to the target. Securing internal portals requires strict attack surface management.
