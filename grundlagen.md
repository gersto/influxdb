# Grundlagen zu InfluxDB2 + FluxQL

im folgenden sollen die Grundlagen und die folgenden Begriffe erklärt werden:
- Bucket
- Retention Time
- Measurement
- Field
- Value
- Tag
- Point
- Schema
- Task
- ...

Original Dokumentation unter [https://docs.influxdata.com/](https://docs.influxdata.com/)

Nach erfolgreicher Installation kann man die Webseite der InfluxDB unter dem Link https://<IP-InfluxDB-Server:8086/signin
erreichen. Zugangsdaten während der Installation

![influxdb01](pictures/influxdb01.jpg)

Verwaltung über die Browseroberfläche (neu in InfluxDB 2)

![influxdb02](pictures/influxdb02.jpg)

Man kann über diese Oberfläche auch **Dashboards** anlegen (eventuell Ersatz für Grafana)

## Buckets

unter **Load Data -> Buckets** sieht man 2 Systembuckets (_monitoring und _tasks) und ein während der Installation angelegtes Bucket

![influxdb03](pictures/influxdb03.jpg)

Je Bucket kann man eine sogenannte **Retension Time** konfigurieren. Beim Anlegen eines Buckets kann man auswählen
wann die Daten gelöscht werden sollen (z.B. Never oder Older Than 30 days oder ...). Die Retension Time kann bei
InfluxDB 2 nur je Bucket vergeben werden. Falls du Daten hast die nie gelöscht werden sollen und Daten die nach einer
bestimmten Zeit gelöscht werden sollen. brauchst du dafür verschiedene Buckets.

![influxdb04](pictures/influxdb04.jpg)
