# 🔒 Arbeitsprobe: Analyse und Reaktion auf eine simulierte ICMP-Flood-Attacke gemäß NIST-Framework

## 📘 Szenario
Im Rahmen einer Übung zur Anwendung des NIST Cybersecurity Frameworks wurde bei einem fiktiven Unternehmen eine Sicherheitsstörung simuliert. Die interne Netzwerkkommunikation kam plötzlich vollständig zum Erliegen. Die Analyse ergab, dass der Vorfall durch eine Flood-Attacke mit ICMP-Paketen verursacht wurde. Dies ist eine typische Form eines DDoS-Angriffs, bei der durch massenhafte, manipulierte Anfragen die Netzwerkressourcen überlastet werden.

---

## 🔍 Ziel der Übung
Ziel war es, typische Schutz-, Erkennungs- und Wiederherstellungsmaßnahmen zu erarbeiten und dabei realistische Prozesse und Werkzeuge der Cybersicherheit anzuwenden. Die nachfolgende Analyse folgt der Systematik des NIST Cybersecurity Frameworks:

---

## 🧩 Analyse gemäß NIST Cybersecurity Framework

### 1. Identifizieren (Identify)
Die Netzwerkanalyse zeigte ein stark erhöhtes Aufkommen von ICMP-Anfragen, die innerhalb kürzester Zeit zu einer Überlastung der Netzwerkverbindungen führten. Ursache war eine mangelnde Begrenzung von ICMP-Verkehr auf den Netzwerkschnittstellen sowie das Fehlen spezifischer Regeln zur Paketkontrolle.

---

### 2. Schützen (Protect)
Als präventive Maßnahme wurden mehrere Schutzmechanismen eingeführt:
- Begrenzung eingehender ICMP-Pakete durch neue Firewall-Regeln (Paketfilterung)
- Einführung eines Intrusion Detection Systems (z. B. Snort), das ICMP-Traffic mit ungewöhnlichem Frequenzmuster automatisch kennzeichnet
- Anpassung bestehender Zugriffskontrollen zur Reduktion von nicht benötigtem Netzwerkverkehr (Zugriffsrechte, Segmentierung)

---

### 3. Erkennen (Detect)
Zur frühzeitigen Erkennung ähnlicher Angriffe wurde das Monitoring-System um folgende Funktionen erweitert:
- Aktivierung von Source-IP-Validierung zur Erkennung von Spoofing-Versuchen
- Musterbasierte Alarmierung bei plötzlichem Anstieg von ICMP-Verbindungen
- Echtzeitüberwachung durch ein zentrales Logging-System mit SIEM-Funktionalitäten

---

### 4. Reagieren (Respond)
Im simulierten Ernstfall erfolgten folgende Reaktionen:
- Priorisierte Abschaltung nicht-kritischer Systeme zur Entlastung des Netzwerks
- Isolierung betroffener Bereiche zur Begrenzung der Auswirkungen
- Übermittlung des Vorfalls an das interne Incident-Response-Team mit anschließender Meldung an das Management

---

### 5. Wiederherstellen (Recover)
Die Wiederherstellung erfolgte stufenweise:
- Wiederinbetriebnahme kritischer Dienste nach Stabilisierung des Netzwerkverkehrs
- Nachträgliche Analyse der Logdaten zur Erkennung weiterer Auffälligkeiten
- Review und Anpassung der Notfallpläne für zukünftige Vorfälle

---


## 📝 Hinweise
Diese Übung wurde im Rahmen meiner persönlichen Vorbereitung auf ein duales Studium im Bereich Informatik durchgeführt. Sie dient der praktischen Anwendung von Cybersecurity-Wissen und zeigen meine Fähigkeit, strukturierte Sicherheitsanalysen durchzuführen.
