# 🔐 Laboratoire personnel de cybersécurité – 2025
**Auteur : Kamogne Taurto Taque Jean**

## 🎯 Objectifs du projet
Créer un environnement virtualisé reproduisant une PME sécurisée afin de :  
- Tester des outils de cybersécurité (IDS, SIEM, hardening)  
- Expérimenter l’automatisation et la surveillance réseau  
- Mettre en pratique les concepts vus en AEC (réseautique, firewall, gestion de logs)

## 🧱 Architecture du lab  

### 🔧 Équipements virtuels (VMware Workstation/ESXi)
- **pfSense** : pare-feu, NAT, VLANs, DHCP, règles firewall  
- **Serveur Linux (Debian)** : DNS, routage, Fail2ban, rsyslog, Ansible  
- **SIEM** : Splunk pour la collecte et la corrélation des logs  
- **IDS** : Snort (sur Debian ou pfSense)  
- **Checkmk** : supervision système et réseau  
- **Proxy** : Squid  
- **Clients** :  
  - Windows 10  
  - Ubuntu Desktop  
  - Kali Linux  
  - Debian minimal  
  - Metasploitable 2 pour les tests d’intrusion

## 🔐 Sécurité et surveillance
- Filtrage du trafic avec pfSense (règles par VLAN)  
- Détection d’intrusion avec Snort  
- Centralisation des logs avec rsyslog  
- Analyse avec Splunk (dashboards personnalisés)  
- Alertes et surveillance via Checkmk

## ⚙️ Automatisation
- Scripts Ansible pour :  
  - Installation automatique de paquets (fail2ban, squid, snort)  
  - Configuration de services  
  - Redémarrage planifié et mise à jour  
- **Objectif** : gain de temps, standardisation des déploiements

## 📈 Résultats observés
- Réseau segmenté et contrôlé  
- Monitoring centralisé en temps réel  
- Détection des tentatives de scan et d’attaque (Kali, Metasploitable)  
- Environnement stable et reproductible

## 💡 Leçons apprises
- Intégration d’outils SIEM et IDS en environnement restreint  
- Importance du durcissement système (fail2ban, firewall, logs)  
- Automatisation comme levier pour gérer la complexité  
- Capacité à diagnostiquer et corriger des erreurs réseau et sécurité

## 📁 Prochaines étapes
- Ajouter Wazuh pour compléter la solution SIEM  
- Intégrer Graylog ou ELK comme alternative  
- Créer un script d’installation complet pour GitHub

