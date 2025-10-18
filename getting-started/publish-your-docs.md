---
icon: globe-pointer
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# MySQL Account erstellen

Wenn du die Einrichtung auf der Beentrichter-Seite abgeschlossen hast, kannst du ganz einfach einen eigenen MySQL-Account erstellen. Folge einfach diesen Schritten:

{% stepper %}
{% step %}
### Terminal öffnen

Öffne das MySQL-Terminal, mit dem folgendem Befehl:

```sql
mysql -u root
```
{% endstep %}

{% step %}
### Benutzer erstellen

Erstelle einen neuen Benutzer, indem du den folgenden Befehl eingibst. Achte darauf, dass du `deinnutzername` und `deinsicherespasswort` mit deinen eigenen Angaben ersetzt:

```sql
CREATE USER 'deinnutzername'@'localhost' IDENTIFIED BY 'deinsicherespasswort';
```
{% endstep %}

{% step %}
### Benutzerrechte erteilen

Gib dem neuen Benutzer alle Rechte, damit er mit der Datenbank arbeiten kann. Mache dies wie folgt:

```sql
GRANT ALL PRIVILEGES ON *.* TO 'deinnutzername'@'localhost' WITH GRANT OPTION;
```
{% endstep %}

{% step %}
### Terminal verlassen

Nun kannst du das MySQL-Terminal verlassen in dem du einfach das eingibst:

```sql
exit
```
{% endstep %}
{% endstepper %}
