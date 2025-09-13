# Security Advisory: Information Disclosure in Sider AI (Sider Fusion)

**Advisory ID:** Pending CVE Assignment  
**Discovered by:** [M. Furqan Patel](https://www.linkedin.com/in/furqanpatel)  
**Date Reported to Vendor:** September 8, 2025  
**Vendor Acknowledgment:** September 9, 2025  
**Public Disclosure Date:** September 13, 2025  

---

## Summary

A vulnerability was discovered in the **Sider AI Web Platform (Sider Fusion)** where the system intermittently reveals **internal backend function calls** in responses to user queries.  
This behavior constitutes an **information disclosure vulnerability**.

---

## Vulnerability Details

- **Type:** Information Disclosure  
- **CWE:** [CWE-200: Exposure of Sensitive Information to an Unauthorized Actor](https://cwe.mitre.org/data/definitions/200.html),  
  [CWE-209: Information Exposure Through an Error Message](https://cwe.mitre.org/data/definitions/209.html)  
- **Impact:** Attackers may gain knowledge of backend function names and logic such as  

- print(default_api.suggest_tool(tool_name="search", reason="User is asking for the meaning of a command"))

This information could be used for reconnaissance or as a stepping stone for further exploitation.  
- **Affected Component(s):** Response handling / output sanitization  
- **Attack Vector:** Remote, via the public web platform  

---

## Proof of Concept (Evidence)


https://github.com/user-attachments/assets/9bd7d577-a552-4ccc-86c0-feac27421069


---

## Impact

While no direct sensitive data (e.g., user credentials, system keys) were disclosed, the leakage of **internal logic and API calls** may provide attackers with insights into the platform’s architecture.  
This increases the risk of more severe exploits in the future.  

- **CVSS v3.1 Base Score (proposed):** 4.3 (Low)  
- Vector: AV:N/AC:L/PR:N/UI:R/S:U/C:L/I:N/A:N  

---

## Timeline

- **2025-09-08**: Vulnerability reported to Sider AI  
- **2025-09-09**: Vendor acknowledged receipt but did not confirm the issue  
- **2025-09-13**: Public disclosure of advisory (pending CVE assignment)  

---

## Credits

This issue was discovered and reported by **M. Furqan Patel**  
- [LinkedIn](https://www.linkedin.com/in/furqanpatel)  

---

## References

- CVE ID: *Pending Assignment*  
- This GitHub advisory (first public reference)  
