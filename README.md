---
published: false
---

# Marventa Analytics

Statische Rechtshinweise der Marth GbR (Marventa living). Die drei Seiten liegen in `index.html`, `datenschutz/index.html` und `impressum/index.html`. Sie verwenden das gemeinsame Stylesheet `assets/styles.css`. Ein Build ist nicht erforderlich.

Vorgesehene Privacy Notice URL für das Login-with-Amazon-Sicherheitsprofil: **`https://marventa.de/datenschutz/`**. Die Marth GbR hat die Veröffentlichung am 25. November 2026 freigegeben.

## Lokal ansehen

Im Projektordner mit installiertem Python 3 ausführen:

```powershell
py -m http.server 8000 --bind 127.0.0.1
```

Im Browser `http://127.0.0.1:8000/`, `http://127.0.0.1:8000/datenschutz/` oder `http://127.0.0.1:8000/impressum/` öffnen. Der lokale HTTP-Server löst Verzeichnislinks so auf wie der spätere Webhost. Mit Strg+C beenden.

## Prüfstand vom 25. November 2026

**Anbieter.** Name, Anschrift, die beiden vertretungsberechtigten Gesellschafter, USt-IdNr. und die Erklärung zur Verbraucherstreitbeilegung stammen aus dem von der GbR mitgeteilten Verkäuferimpressum. Die Suche im amtlichen Registerportal nach „Marth“ mit Sitz „Probsteierhagen“ ergab 0 Treffer. Das Impressum enthält daher keine Registerangabe. Die Reichweite des Suchergebnisses ist auf diese Kriterien begrenzt. Die Gesellschafter sind namentlich genannt. Eine Einzelvertretungsbefugnis wird nicht unterstellt. [Registerportal der Länder](https://www.handelsregister.de/rp_web/normalesuche/welcome.xhtml) · [§ 720 BGB](https://www.gesetze-im-internet.de/bgb/__720.html) · [§ 5 DDG](https://www.gesetze-im-internet.de/ddg/__5.html)

**Kontakt.** Das Impressum nennt E-Mail und geschäftliche Telefonnummer. Datenschutzanfragen gehen an `info@marventa.de`. Für Beschwerden am Unternehmenssitz ist das ULD Schleswig-Holstein zuständig. [Beschwerdestelle des ULD](https://www.datenschutzzentrum.de/formular/beschwerde.php)

**Website und Postfach.** GitHub beschreibt die Protokollierung der Besucher-IP zur Sicherheit und nennt für Pages keine feste Löschfrist. Fastly beschreibt die Auslieferung der Pages-Seiten. Für die E-Mail-Domain ergab die lesende MX-Abfrage `smtpin.rzone.de` (Priorität 5). STRATO führt dieses Ziel als eigenen Mailserver. Die GbR bestätigt, dass die Nachrichten bei STRATO bleiben. Diese Aussage über das Postfach stammt vom Betreiber. Der DNS-Eintrag belegt nur die Zustellung. [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection) · [Fastly](https://www.fastly.com/customers/github) · [STRATO zu seinen MX-Einträgen](https://www.strato.de/faq/domains/wie-kann-ich-bei-strato-meine-dns-eintraege-verwalten/)

**Auftragsverarbeitung beim Postfach.** Die GbR bestätigt einen Vertragsabschluss ab dem 18. Juli 2022. Für diese Verträge bezieht STRATO die Vereinbarung zur Auftragsverarbeitung automatisch ein. Eine Kopie ist unter **Kundendaten → Auftragsverarbeitung** abrufbar. [STRATO zur AVV](https://www.strato.de/faq/vertrag/fragen-zur-auftragsverarbeitungsvertrag-avv-und-der-neuen-eu-datenschutzgrundverordnung-dsgvo/)

### Vor der produktiven Amazon-Anbindung

Die Registrierung des LWA-Sicherheitsprofils und der erste Abruf echter Werbedaten sind zwei verschiedene Schritte. Die Datenschutzerklärung beschreibt die Anbindung als geplant.

- **[ZU PRÜFEN] Freigabe und Empfänger.** Nur eigene Werbeprofile anbinden. Die von Amazon tatsächlich erteilten Rechte und gelieferten Felder mit dem Analysezweck abgleichen. Für die geplante Auswertung sind keine zusätzlichen LWA-Berechtigungen für persönliche Profildaten vorgesehen. Für Deutschland als gewähltes Werbeland nennt die Ads-Vereinbarung Amazon Online Germany GmbH als Vertragspartnerin. Die zusätzlichen Richtlinien benennen für die dort definierten EU-Daten Amazon Europe Core S.à r.l. oder die jeweilige benannte Tochtergesellschaft als eigenständig Verantwortliche. Vor dem Start die Vereinbarungen des konkreten Werbekontos und die Rollen bei Login, API-Abruf und eigener Speicherung abgleichen. [Amazon Ads-Vereinbarung](https://advertising.amazon.com/terms) · [Amazon Ads-Richtlinien](https://advertising.amazon.com/de-de/resources/ad-policy/sponsored-ads-additional-policies) · [Ads-Autorisierung](https://advertising.amazon.com/API/docs/en-us/guides/account-management/authorization/authorization-grants)
- **[ZU PRÜFEN] Zugriff und Löschung in der separaten App.** Als Entwurf für die Implementierung: Zugriffstokens nur für ihre technische Laufzeit vorhalten, Refresh-Tokens geschützt speichern und beim Trennen des Kontos löschen. Keine Tokens in Berichte, Protokolle oder das Website-Repository schreiben. Als Ausgangspunkt Rohberichte mit Suchbegriffen höchstens 30 Tage für die Auswertung vorsehen, anschließend nur die für einen Vorjahresvergleich benötigten aggregierten Monatswerte bis zu 13 Monate behalten. Sicherungen mit definiertem Ablauf versehen und bei Wiederherstellung vollzogene Löschungen nachziehen. Diese Zeiträume sind Vorschläge für die Entwicklung. Der endgültige Plan muss zum Auswertungsbedarf und zu den dann geltenden Amazon-Bedingungen passen. Vor dem ersten Abruf auch Speicherort, Dienstleister, Transfergrundlagen und den Löschtest dokumentieren.
- **[ZU PRÜFEN] Personenbezug.** Das Interesse an sicherer Autorisierung und Budgetsteuerung gegen die Auswirkungen auf Kontoverwalter und gegebenenfalls in Suchbegriffen genannte Personen abwägen. Bei Daten aus Amazon-Berichten die Informationspflicht nach Art. 14 DSGVO beurteilen. Soweit sie greift, grundsätzlich binnen eines Monats informieren, bei früherer erster Kommunikation bzw. Offenlegung bereits zu diesem Zeitpunkt. Eine einschlägige Ausnahme begründen. [Art. 13 und 14 DSGVO](https://eur-lex.europa.eu/legal-content/DE/TXT/?uri=CELEX%3A32016R0679)

## Veröffentlichung über GitHub Pages und STRATO

DNS-Einstellungen bei STRATO werden manuell verwaltet.

1. **Repository erstellen.** Im vorgesehenen GitHub-Konto ein leeres öffentliches Repository, z. B. `marventa-legal`, anlegen. GitHub Free unterstützt Pages bei öffentlichen Repositorys. [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)

2. **Dateien hochladen.** Die drei HTML-Dateien mit ihren Verzeichnissen, `assets/`, `CNAME` und diese README im Branch `main` ablegen. Die Startdatei `index.html` und `CNAME` müssen direkt im Repository-Stamm liegen. `CNAME` enthält eine einzige Zeile mit `marventa.de`. Die README ist mit `published: false` für die Dokumentation im Repository vorgesehen.

3. **Pages aktivieren.** Unter **Settings → Pages → Build and deployment** die Quelle **Deploy from a branch** wählen. **main** und **/ (root)** auswählen und speichern. Den erfolgreichen Pages-Lauf unter **Actions** prüfen. Weitere Commits auf `main` können die öffentliche Website aktualisieren. [GitHub-Anleitung zur Veröffentlichungsquelle](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

4. **Domain bei GitHub zuordnen.** In **Settings → Pages → Custom domain** zunächst `marventa.de` speichern, bevor die Web-Adressen bei STRATO umgestellt werden. GitHub empfiehlt zusätzlich die Domainverifizierung in den Pages-Einstellungen des Benutzer- oder Organisationskontos. Dazu ausschließlich den von GitHub eigens benannten TXT-Eintrag anlegen und behalten. [Domain zuordnen](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) · [Domain verifizieren](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages)

5. **Web-Adressen bei STRATO setzen.** Zuerst den DNS-Bestand im Kunden-Login dokumentieren. **Bestehende MX-, SPF-, DKIM-, DMARC- und Autodiscover-Einstellungen dürfen nicht verändert werden.** Auch Mailhost-Adressen und Nameserver beibehalten. Vorab prüfen, ob ein MX-Ziel oder Postfachclient direkt `marventa.de` nutzt oder eine SPF-Regel die IP der Hauptdomain über den Mechanismus `a` einbezieht. Hängt der Mailbetrieb an der bisherigen Web-IP, die Umstellung bis zur Klärung mit dem Mailadministrator zurückstellen.

   Unter **Domains → Domainverwaltung → marventa.de → Zahnrad → DNS → A-Record** ausschließlich das Webziel der Hauptdomain bearbeiten. Die folgenden vier IPv4-Ziele stammen aus der offiziellen GitHub-Anleitung. Werte unmittelbar vor der Umstellung dort abgleichen. Unterstützt das STRATO-Paket mehrere A-Einträge, die vier Adressen als einzelne Werte für denselben Host setzen. Gibt es nur ein Eingabefeld für eine IPv4-Adresse, einen der dokumentierten Werte verwenden. GitHub verlangt für diese Variante mindestens einen A-Eintrag. [GitHub-DNS-Vorgaben](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) · [STRATO-DNS-Verwaltung](https://www.strato.de/faq/domains/wie-kann-ich-bei-strato-meine-dns-eintraege-verwalten/)

   | Host | Typ | IPv4-Adresse |
   | --- | --- | --- |
   | marventa.de | A | `185.199.108.153` |
   | marventa.de | A | `185.199.109.153` |
   | marventa.de | A | `185.199.110.153` |
   | marventa.de | A | `185.199.111.153` |

   Auch vorhandene **AAAA-Einträge der Hauptdomain** prüfen. Zeigen sie auf das frühere Webhosting, würden IPv6-Besucher dort landen. Nach Prüfung der Mailabhängigkeiten entweder die offiziellen GitHub-Pages-IPv6-Ziele konfigurieren oder veraltete reine Web-AAAA-Einträge entfernen. Für die Hauptdomain weder einen CNAME noch eine Wildcard einrichten. Den DNS-Gesamtreset bei STRATO vermeiden.

6. **Optional www einrichten.** Falls `www.marventa.de` ebenfalls zur Website führen soll, nur für die Subdomain `www` einen CNAME auf `<GitHub-Kontoname>.github.io.` anlegen. Den Platzhalter durch den Benutzer- oder Organisationsnamen ersetzen. Das Ziel enthält weder Protokoll noch Repository-Pfad. Vorher bestehende Dienste auf genau dieser Subdomain prüfen. Die primäre Domain in GitHub Pages bleibt `marventa.de`. [GitHub zu www und Hauptdomain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

7. **DNS prüfen.** Die Ausbreitung der Änderungen abwarten. Mit den folgenden lesenden PowerShell-Abfragen die Hauptdomain und, falls eingerichtet, `www` prüfen. A muss die ausgewählten Pages-Adressen liefern, AAAA bei Nutzung die vorgesehenen Pages-IPv6-Adressen. Die Mail-Einträge im STRATO-Konto mit dem dokumentierten Ausgangsstand vergleichen. [DNS-Prüfung bei GitHub](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

   ```powershell
   Resolve-DnsName marventa.de -Type A
   Resolve-DnsName marventa.de -Type AAAA
   Resolve-DnsName www.marventa.de -Type CNAME
   Resolve-DnsName marventa.de -Type MX
   ```

8. **HTTPS aktivieren.** Nach erfolgreicher DNS-Prüfung und Zertifikatsausstellung unter **Settings → Pages** die Option **Enforce HTTPS** aktivieren. Ist sie noch ausgegraut, die dortige DNS- und Zertifikatsmeldung prüfen und die Bereitstellung abwarten. [GitHub-Anleitung zu HTTPS](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)

9. **Datenschutz-URL abnehmen und bei Amazon eintragen.** In einem privaten Browserfenster `https://marventa.de/datenschutz/` direkt öffnen. Die Seite muss ohne Anmeldung und mit gültigem Zertifikat die Erklärung der Marth GbR anzeigen. Mit `curl.exe -I https://marventa.de/datenschutz/` HTTP 200 beim direkten HTTPS-Aufruf prüfen. Der Aufruf von `http://marventa.de/datenschutz/` soll auf dieselbe Adresse mit HTTPS führen. Anschließend Navigation zu Impressum und Startseite sowie den Rückweg prüfen. Erst nach erfolgreicher Abnahme im LWA Security Profile unter **Consent Privacy Notice URL** exakt `https://marventa.de/datenschutz/` eintragen. [Amazon-Anleitung zum Sicherheitsprofil](https://developer.amazon.com/docs/login-with-amazon/register-web.html)
