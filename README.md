# MITM Attack Lab — Ασφάλεια Δικτύων Υπολογιστών

> ⚠️ **Educational coursework.** Όλες οι επιθέσεις που περιγράφονται στην αναφορά
> εκτελέστηκαν αποκλειστικά σε **απομονωμένο εικονικό δίκτυο** (Oracle VirtualBox,
> Host-Only network) με VMs που ελέγχονταν πλήρως από τον συγγραφέα (Kali Linux
> attacker, Ubuntu victim, pfSense gateway). Καμία πραγματική υποδομή, τρίτο
> πρόσωπο ή δίκτυο παραγωγής δεν επηρεάστηκε.

## Περιγραφή

Ομαδική εργασία εξαμήνου για το μάθημα **Ασφάλεια Δικτύων Υπολογιστών**
(Πανεπιστήμιο Αιγαίου, Τμήμα Μηχανικών Πληροφοριακών και Επικοινωνιακών
Συστημάτων, Διδάσκων: Α. Φακής). Αντικείμενο της εργασίας ήταν η πρακτική
εξοικείωση με τεχνικές Man-in-the-Middle σε ελεγχόμενο εργαστηριακό
περιβάλλον, καθώς και η ανάλυση της κίνησης δικτύου και η τεκμηρίωση μέτρων
άμυνας.

## Network Topology

![Network Topology](docs/network-topology.svg)

## Περιεχόμενα

| Αρχείο | Περιγραφή |
|---|---|
| [`docs/Semester_Assignment.pdf`](docs/Semester_Assignment.pdf) | Η εκφώνηση της εργασίας από τον διδάσκοντα |
| [`docs/Anafora_3212020204.pdf`](docs/Anafora_3212020204.pdf) | Η τελική γραπτή αναφορά (screenshots, ανάλυση, troubleshooting log) |

## Φάσεις που καλύπτονται στην αναφορά

1. **ARP Spoofing & Packet Capture** — ARP cache poisoning με Bettercap, capture σε Wireshark, plaintext HTTP credentials
2. **DNS Spoofing & Website Cloning** — Credential harvesting με SET, spoofed DNS replies
3. **HTTPS Downgrade / SSL Stripping** — Σύγκριση vulnerable vs. HSTS-protected στόχων
4. **Rogue Certificate Injection** — Δημιουργία self-signed CA με OpenSSL, εγκατάσταση σε trust store, ανάλυση TLS trust model
5. **Session Hijacking μέσω Cookie Theft** — Θεωρητική ανάλυση (cookie visibility, Secure/HttpOnly flags)
6. **DHCP Starvation & Rogue DHCP Server** — Θεωρητική τεχνική ανάλυση
7. **Ανάλυση Επιθέσεων & Μέτρα Άμυνας** — 6 προτεινόμενες άμυνες (DAI, HSTS, certificate pinning, DNSSEC, DHCP snooping/802.1X, κ.ά.)

## Εργαλεία

Bettercap · Wireshark · Social Engineering Toolkit (SET) · OpenSSL · Apache2 · VirtualBox (Kali Linux / Ubuntu / pfSense)

## Σημείωση

Η αναφορά περιέχει screenshots με δοκιμαστικά (dummy) credentials που
χρησιμοποιήθηκαν αποκλειστικά εντός του απομονωμένου lab, σύμφωνα με τις
οδηγίες της εκφώνησης.
