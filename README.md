# CTF-CyberSec_training
Welcome to my walkthrough of a Capture The Flag (CTF) challenge conducted in a simulated environment. The objective: **find 8 hidden flags by exploiting common system and network vulnerabilities**.

---

## Scenario

You’re placed in a virtual environment simulating real-world vulnerabilities. Your objective: find 8 flags hidden in different parts of the network through scanning, exploitation, password cracking, and traffic analysis.

---

##  Tools & Commands Used

| Tool         | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `nmap`       | Network mapping, port scanning, service version detection                   |
| `nikto`      | Web server vulnerability scanning                                           |
| `exiftool`   | Extracting metadata from images (used in Flag 1)                            |
| `fcrackzip`  | Password cracking for zip files using wordlists                             |
| `curl`       | HTTP request tool to fetch remote files                                     |
| `base64`     | Decoding encoded data from text/files                                       |
| `Wireshark`  | PCAP file analysis for flag extraction                                      |

---

## Flags Overview

| Flag | Description                                                      | Technique Used                        |
|------|------------------------------------------------------------------|----------------------------------------|
| 1 | Found in image metadata                                          | `exiftool`                             |
| 2 | Hidden in `robots.txt`                                           | `nikto` scan + URL discovery           |
| 3 | Inside a zip file cracked with `fcrackzip`                       | Wordlist attack using `rockyou.txt`    |
| 4 | Embedded in a messy script file                                  | Directory traversal                    |
| 5 | Retrieved from a secret directory                                | `curl`, `cat`                          |
| 6 | Extracted from a `.pcap` file using IP as password               | Wireshark + zip cracking               |
| 7 | Accessed via SSH-like login using flags 5 & 6                    | Credential reuse                       |
| 8 | Discovered through privilege escalation in system directories    | Python script execution                |

---


