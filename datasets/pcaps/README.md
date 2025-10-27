# PCAP/PCAPNG Datasets

Το παρόν αποθετήριο περιέχει **pcap/pcapng** αρχεία που δημιουργήθηκαν σε εργαστηριακό περιβάλλον (VirtualBox) κατά τη διάρκεια της πτυχιακής μελέτης.

Τα αρχεία αντιστοιχούν σε εκτελέσεις **Atomic Red Team** και **MITRE Caldera** επιθέσεων σε **Windows 10** και **Ubuntu 22.04** στόχους, με σκοπό την καταγραφή και ανάλυση δικτυακής κίνησης για κάθε σενάριο.
Επιπλέον εδώ υπάρχουν και adversary profiles που μπορούν να γίνουν κατευθείαν import στο Caldera (`.yaml` αρχεία)
---

## 📂 Περιεχόμενα

| **Αρχείο** | **Σενάριο / Πλαίσιο Εκτέλεσης** | **Στόχος (OS)** |
|-------------|----------------------------------|------------------|
| `atomic-linux-attacks.pcap` | Atomic Red Team — *Discovery / Collection* | Linux (Ubuntu 22.04) |
| `atomic-windows-attacks.pcapng` | Atomic Red Team — *Discovery / Exfiltration / Impact* | Windows 10 |
| `caldera-linux-ops.pcap` | MITRE Caldera — *Discovery / Command & Control (Sandcat)* | Linux (Ubuntu 22.04) |
| `caldera-windows-ops.pcapng` | MITRE Caldera — *Discovery / Command & Control (Sandcat)* | Windows 10 |


---

## 📘 Περιγραφή

Κάθε αρχείο `.pcap` / `.pcapng` περιέχει την πλήρη δικτυακή κίνηση που καταγράφηκε κατά την εκτέλεση των TTPs από τα εργαλεία Atomic Red Team ή Caldera.  
Τα δεδομένα χρησιμοποιήθηκαν για **offline ανάλυση** με Snort/Suricata και **ενσωμάτωση αποτελεσμάτων** στο Wazuh SIEM.

---

Για επαλήθευση ακεραιότητας: δείτε `SHA256SUMS.txt`.
