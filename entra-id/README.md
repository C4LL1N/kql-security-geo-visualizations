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

<img width="1451" height="611" alt="proof" src="https://github.com/user-attachments/assets/c1eacc75-70a0-458f-8c9f-fe370f988374" />


### ✔️ `EntraIDAuthenticationFailures.json`
Mapa nieudanych logowań to samo co successfull login tylko, że nagtywne róznica ('ResultType>0'), pozwalająca wykrywać próby brute-force lub podejrzane lokalizacje.
## 🎯 Cel

Celem zapytań jest:

- identyfikacja nietypowych lokalizacji logowań  
- analiza ryzyka na podstawie geolokalizacji  
- szybkie mapowanie aktywności użytkowników i urządzeń  
- łatwe budowanie dashboardów opartych o dane Entra ID  

---

## 🚀 Jak używać

1. Skopiuj dowolny `.json`.
2. Sentinel Workbook Użyj JSON Format w opcji Advanced Editor, aby dostać mapkę.
3. Możesz z póżniej skopiować `.kql`.
4. Otwórz **Log Analytics** lub **Sentinel Logs**.
5. Wklej zapytanie i uruchom.

---
