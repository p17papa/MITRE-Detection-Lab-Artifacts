# — Custom detection rules

Αυτός ο φάκελος περιέχει τα custom detection rules που χρησιμοποιήθηκαν για
την αξιολόγηση MITRE/Atomic & CALDERA (network + host).

## Περιεχόμενα
| Filename               | Purpose / OS         | Notes |
|------------------------|----------------------|-------|
| snort_custom.rules     | Snort 3.x: Network rules (Linux + Windows) | Keep Snort-compatible syntax only; unique SIDs in range 240xxxx/230xxxx |
| suricata_custom.rules  | Suricata: Network rules (UA, large POST, filename indicators) | Use Suricata-only options here (distance/within/nocase) |
| wazuh_custom_R.xml     | Wazuh rules/decoders (host-level detection) | Host events: cron, bash_history, file creation |

