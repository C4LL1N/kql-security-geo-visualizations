# Entra ID – Geo Visualizations & KQL Queries

Ten katalog zawiera zapytania KQL oraz wizualizacje geolokalizacyjne oparte na danych z **Microsoft Entra ID**. Zapytania są przygotowane pod użycie w:

- Log Analytics Workspaces  
- Azure Monitor  
- Microsoft Sentinel Workbooks  
- Microsoft Defender for Cloud Apps  

Celem jest szybka analiza bezpieczeństwa logowań oraz anomalii lokalizacyjnych w środowisku tożsamości.

---

## 📌 Zawartość katalogu

### ✔️ `successful-logins.json`
Zapytanie generujące mapę z udanymi logowaniami (`ResultType == 0`), z geolokalizacją użytkowników:
- latitude / longitude  
- miasto  
- kraj  
- liczba logowań  
- etykieta użytkownik → lokalizacja

### ✔️ `failed-logins.json`
Mapa nieudanych logowań to samo co successfull login tylko, że nagtywne róznica ('ResultType>0'), pozwalająca wykrywać próby brute-force lub podejrzane lokalizacje.
## 🎯 Cel

Celem zapytań jest:

- identyfikacja nietypowych lokalizacji logowań  
- analiza ryzyka na podstawie geolokalizacji  
- szybkie mapowanie aktywności użytkowników i urządzeń  
- łatwe budowanie dashboardów opartych o dane Entra ID  

---

## 🚀 Jak używać

1. Skopiuj dowolne zapytanie `.kql`.
2. Jeśli chcesz Sentinel Workbook Użyj JSON Format w opcji Advanced Editor, aby dostać mapkę.
3. Otwórz **Log Analytics** lub **Sentinel Logs**.
4. Wklej zapytanie i uruchom.

---
