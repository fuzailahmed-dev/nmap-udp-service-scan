# Nmap UDP Service & Version Scan (-sU -sV)

## Objective
To perform UDP service and version detection on an authorized lab machine using Nmap and understand how UDP-based services respond during reconnaissance.

---

## Tool Used
- Nmap 7.95
- Kali Linux
- VMware Workstation
- Target: Authorized lab machine (Metasploitable)

---

## Command Executed
```bash
nmap -sU -sV -Pn -n --top-ports 50 LAB_MACHINE

| Port | Protocol | State | Service | Version         |
| ---- | -------- | ----- | ------- | --------------- |
| 53   | UDP      | Open  | DNS     | ISC BIND 9.4.2  |
| 111  | UDP      | Open  | RPCBind | RPC #100000     |
| 137  | UDP      | Open  | NetBIOS | Windows NetBIOS |
| 2049 | UDP      | Open  | NFS     | NFS 2–4         |

Observations

UDP scans are significantly slower than TCP scans.
Many UDP ports appear as open|filtered due to lack of response.
Misconfigured UDP services can expose critical information.

Learning Outcome

Learned UDP enumeration techniques
Understood service & version detection
Improved reconnaissance analysis skills




