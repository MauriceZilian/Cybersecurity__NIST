# 🔒 Arbeitsprobe: Analyse und Reaktion auf eine simulierte ICMP-Flood-Attacke gemäß NIST-Framework

## 📘 Szenario
Im Rahmen einer Übung zur Anwendung des NIST Cybersecurity Frameworks wurde bei einem fiktiven Unternehmen eine Sicherheitsstörung simuliert. Die interne Netzwerkkommunikation kam plötzlich vollständig zum Erliegen. Die Analyse ergab, dass der Vorfall durch eine Flood-Attacke mit ICMP-Paketen verursacht wurde – eine typische Form eines DDoS-Angriffs, bei der durch massenhafte, manipulierte Anfragen die Netzwerkressourcen überlastet werden.

## 🔍 Ziel der Übung
Ziel war es, typische Schutz-, Erkennungs- und Wiederherstellungsmaßnahmen zu erarbeiten und dabei realistische Prozesse und Werkzeuge der Cybersicherheit anzuwenden. Die nachfolgende Analyse folgt der Systematik des NIST Cybersecurity Frameworks:

---

## 🧩 Analyse gemäß NIST Cybersecurity Framework

### 1. Identifizieren (Identify)
Die Netzwerkanalyse zeigte ein stark erhöhtes Aufkommen von ICMP-Anfragen, die innerhalb kürzester Zeit zu einer Überlastung der Netzwerkverbindungen führten. Ursache war eine mangelnde Begrenzung von ICMP-Verkehr auf den Netzwerkschnittstellen sowie das Fehlen spezifischer Regeln zur Paketkontrolle.

### 2. Schützen (Protect)
Als präventive Maßnahme wurden mehrere Schutzmechanismen eingeführt:
- Begrenzung eingehender ICMP-Pakete durch neue Firewall-Regeln (Paketfilterung)
- Einführung eines Intrusion Detection Systems (z. B. Snort), das ICMP-Traffic mit ungewöhnlichem Frequenzmuster automatisch kennzeichnet
- Anpassung bestehender Zugriffskontrollen zur Reduktion von nicht benötigtem Netzwerkverkehr (Zugriffsrechte, Segmentierung)

### 3. Erkennen (Detect)
Zur frühzeitigen Erkennung ähnlicher Angriffe wurde das Monitoring-System um folgende Funktionen erweitert:
- Aktivierung von Source-IP-Validierung zur Erkennung von Spoofing-Versuchen
- Musterbasierte Alarmierung bei plötzlichem Anstieg von ICMP-Verbindungen
- Echtzeitüberwachung durch ein zentrales Logging-System mit SIEM-Funktionalitäten

### 4. Reagieren (Respond)
Im simulierten Ernstfall erfolgten folgende Reaktionen:
- Priorisierte Abschaltung nicht-kritischer Systeme zur Entlastung des Netzwerks
- Isolierung betroffener Bereiche zur Begrenzung der Auswirkungen
- Übermittlung des Vorfalls an das interne Incident-Response-Team mit anschließender Meldung an das Management

### 5. Wiederherstellen (Recover)
Die Wiederherstellung erfolgte stufenweise:
- Wiederinbetriebnahme kritischer Dienste nach Stabilisierung des Netzwerkverkehrs
- Nachträgliche Analyse der Logdaten zur Erkennung weiterer Auffälligkeiten
- Review und Anpassung der Notfallpläne für zukünftige Vorfälle

---

## 📘 Glossar – Fachbegriffe zur Cybersecurity-Arbeitsprobe

Dieses Glossar enthält zentrale Begriffe, die in der Analyse und Umsetzung von Sicherheitsmaßnahmen im Rahmen des NIST Cybersecurity Frameworks verwendet wurden.

### 🛡️ DDoS (Distributed Denial of Service)
Ein koordinierter Angriff auf ein IT-System, bei dem es durch massenhafte Anfragen gezielt überlastet und dadurch unbrauchbar gemacht wird.

### 📶 ICMP (Internet Control Message Protocol)
Ein Netzwerkprotokoll zur Übertragung von Diagnose- und Fehlermeldungen. Es wird häufig für Ping-Anfragen genutzt – kann jedoch auch missbraucht werden, etwa bei Flood-Angriffen zur Überlastung eines Netzwerks.

### 🔥 Firewall-Regel (Rate Limiting)
Eine Regel, die die maximale Anzahl von zulässigen Anfragen pro Zeiteinheit begrenzt. Im Kontext von ICMP-Angriffen kann so verhindert werden, dass ein System durch zu viele Pakete überlastet wird.

### 🧱 Segmentierung (Netzwerksegmentierung)
Die Aufteilung eines Netzwerks in mehrere logische oder physische Abschnitte (z. B. VLANs), um Sicherheitszonen zu schaffen.

### 🔐 Zugriffskontrolle (Access Control)
Richtlinien und technische Maßnahmen zur Begrenzung des Datenzugriffs auf autorisierte Personen oder Systeme.

### 📡 IDS/IPS (Intrusion Detection/Prevention System)
Ein System zur Erkennung (IDS) bzw. automatischen Abwehr (IPS) von Angriffen auf Netzwerke.

### 📊 SIEM (Security Information and Event Management)
Ein System zur zentralen Sammlung und Korrelation sicherheitsrelevanter Daten für Echtzeit-Erkennung und Analyse.

### 📈 Netzwerk-Monitoring
Die kontinuierliche Überwachung von Netzwerkaktivitäten zur Erkennung von Anomalien und potenziellen Angriffen.

### 💡 NIST Cybersecurity Framework
Ein Rahmenwerk zur Organisation von Cybersicherheitsprozessen in fünf Funktionsbereiche: Identify, Protect, Detect, Respond, Recover.

---

## 📝 Hinweise
Diese Übung wurde im Rahmen meiner persönlichen Vorbereitung auf ein duales Studium im Bereich Informatik durchgeführt. Alle Inhalte und Szenarien wurden eigenständig entwickelt und sind frei formuliert. Sie dienen der praktischen Anwendung von Cybersecurity-Wissen und zeigen meine Fähigkeit, strukturierte Sicherheitsanalysen durchzuführen.
