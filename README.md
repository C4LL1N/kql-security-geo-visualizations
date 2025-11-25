# kql-security-geo-visualizations

Zbiór zapytań KQL oraz wizualizacji geolokalizacyjnych (map) dla środowiska Microsoft Entra ID, Azure Monitor, Microsoft Sentinel i Microsoft Defender. Repozytorium ma na celu ułatwienie analizy bezpieczeństwa poprzez mapowanie logów na podstawie lokalizacji użytkowników, urządzeń i incydentów.

---

## 🔍 Zakres repozytorium

Repo zawiera:

- Mapy logowań Entra ID (udanych i nieudanych)
- Mapy alertów bezpieczeństwa
- Mapy działań Defendera i Sentinel
- Szablony map dla Workbooków i Log Analytics
- Zapytania geolokalizacyjne wykorzystujące:
  - `LocationDetails.geoCoordinates.latitude`
  - `LocationDetails.geoCoordinates.longitude`
  - `city`
  - `countryOrRegion`

Każda wizualizacja jest przygotowana tak, aby można ją uruchomić bezpośrednio w **Log Analytics Workspaces**, **Microsoft Sentinel Workbooks**, lub **Azure Monitor**.

Celem repo jest:

uproszczenie wizualizacji danych bezpieczeństwa,

szybkie wykrywanie anomalii geolokalizacyjnych,

budowanie własnych dashboardów geograficznych,

analiza podejrzanych logowań i incydentów w skali globalnej.

