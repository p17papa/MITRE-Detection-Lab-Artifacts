# Custom Detection Rules

- `rules/snort/` : Snort 3 rules (π.χ. custom.rules, classification.config, snort.lua include hints)
- `rules/suricata/` : Suricata rules (π.χ. custom.rules, suricata.yaml fragments)
- `rules/wazuh/` : Wazuh local rules (π.χ. local_rules.xml), FIM/auditd snippets

> Συμβουλή: κρατάμε SIDs/Rule IDs ευθυγραμμισμένα με τα MITRE TTPs, ώστε να γίνεται tagging/correlation στο SIEM (Wazuh).
