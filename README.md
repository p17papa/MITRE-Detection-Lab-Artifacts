# MITRE-Detection-Lab-Artifacts

Αποθετήριο για την πτυχιακή εργασία: **Συγκριτική αξιολόγηση IDS/IPS & SIEM** με σενάρια από **Atomic Red Team** και **MITRE Caldera** σε εργαστηριακό περιβάλλον **VirtualBox NAT**.

## Περιεχόμενα
- `datasets/pcaps/` : PCAP/PCAPNG datasets (Linux/Windows, Atomic & Caldera) + `SHA256SUMS.txt`
- `rules/snort/` : Custom κανόνες για **Snort 3**
- `rules/suricata/` : Custom κανόνες για **Suricata**
- `rules/wazuh/` : **Wazuh** `local_rules.xml` και snippets (FIM, auditd, tagging με MITRE)

## Πλαίσιο/Στόχοι
- Εμπειρική αξιολόγηση **Snort**, **Suricata**, **Wazuh** ως προς TTPs του **MITRE ATT&CK**.
- Ευθυγράμμιση SIDs/Rule IDs με TTPs για ξεκάθαρα **MITRE tags** και συσχέτιση στο SIEM.
- Καθαρή συλλογή κυκλοφορίας (pcaps) για offline ανάλυση και ανάπτυξη/ρύθμιση κανόνων.

## Δεδομένα (PCAPs)
| Αρχείο | Σενάριο | Στόχος |
|---|---|---|
| `atomic-linux-attacks.pcap` | Atomic Red Team (Discovery/Collection) | Linux (Ubuntu) |
| `atomic-windows-attacks.pcapng` | Atomic Red Team (Discovery/Exfil) | Windows 10 |
| `caldera-linux-ops.pcap` | MITRE Caldera (Discovery/C2) | Linux (Ubuntu) |
| `caldera-windows-ops.pcapng` | MITRE Caldera (Discovery/C2/Web) | Windows 10 |

> Επαλήθευση ακεραιότητας: `datasets/pcaps/SHA256SUMS.txt`.

## Χρήσιμες σημειώσεις
- Για **Suricata**: ενεργοποιούμε `EVE (eve.json)` και διασυνδέουμε με **Wazuh** (`<localfile>`), ώστε να γίνεται ενιαία απεικόνιση & tagging.
- Για **Snort 3**: `custom.rules` + include στο `snort.lua`.
- Για **Wazuh**: `local_rules.xml` με `if_sid/field alert.signature_id` για απευθείας mapping σε **MITRE TTPs**.

## Άδειες
- Κώδικας/κανόνες: MIT (βλ. `LICENSE`)
- Datasets (pcap/pcapng): **CC BY-NC 4.0** (βλ. `datasets/pcaps/LICENSE-CC-BY-NC-4.0.md`)

---
© 2025 p17papa
