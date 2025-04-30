# DP-700_LAB06
# Analyseer gegevens in een Data Warehouse met Microsoft Fabric

Deze oefening leidt je door het analyseren van gegevens in een relationele Data Warehouse-omgeving binnen Microsoft Fabric. In tegenstelling tot een Lakehouse biedt een Data Warehouse volledige SQL-mogelijkheden, inclusief invoegen, bijwerken en verwijderen van gegevens.

> ⏱️ **Duur**: ongeveer 30 minuten  
> ⚠️ **Voorwaarde**: Een Microsoft Fabric-proefabonnement is vereist

---

## 🏗️ Werkruimte aanmaken

1. Ga naar [Microsoft Fabric Home](https://app.fabric.microsoft.com/home?experience=fabric).
2. Meld je aan met je organisatie-account.
3. Klik op **Werkruimten** (🗇) > **Nieuwe werkruimte**.
4. Geef je werkruimte een naam en kies een licentietype met Fabric-capaciteit (Trial, Premium of Fabric).

---

## 🏢 Data Warehouse aanmaken

1. Klik op **Maken** > **Warehouse** onder "Data Warehouse".
2. Geef het een unieke naam.
3. Wacht totdat het magazijn is aangemaakt.

---

## 📦 Tabellen maken en gegevens invoegen

1. Open het T-SQL-tegel en voer de **CREATE TABLE** opdracht uit om `DimProduct` aan te maken.
2. Gebruik vervolgens een **INSERT INTO** opdracht om voorbeeldgegevens toe te voegen.
3. Kopieer en voer het script uit van:  
   `https://raw.githubusercontent.com/MicrosoftLearning/dp-data/main/create-dw.txt`  
   Hiermee worden extra tabellen aangemaakt:  
   - `DimCustomer`  
   - `DimDate`  
   - `DimProduct`  
   - `FactSalesOrder`

---

## 🔗 Datamodel definiëren

1. Open de **Model Layouts** weergave.
2. Leg relaties vast:
   - `FactSalesOrder.ProductKey` → `DimProduct.ProductKey`
   - `FactSalesOrder.CustomerKey` → `DimCustomer.CustomerKey`
   - `FactSalesOrder.SalesOrderDateKey` → `DimDate.DateKey`
3. Zorg dat alle relaties `Many to One (*:1)` zijn en enkelvoudige kruislingsfiltering gebruiken.

---

## 🔍 SQL-query’s uitvoeren

1. Gebruik een JOIN tussen `FactSalesOrder` en `DimDate` om verkopen per maand en jaar op te sommen.
2. Breid de query uit met `DimCustomer` om verkopen per regio toe te voegen.
3. Maak een **weergave (view)** `vSalesByRegion` op basis van deze aggregaties.
4. Controleer de resultaten via `SELECT`-opdrachten op de aangemaakte view.

---

## 🧩 Visuele query maken

1. Kies **Nieuwe visuele query**.
2. Voeg `FactSalesOrder` en `DimProduct` toe.
3. Merge ze via `ProductKey`.
4. Filter bijvoorbeeld op `Cable Lock` binnen `ProductName`.
5. Exporteer of visualiseer de resultaten.

---

## 📊 Rapport maken

1. Verberg irrelevante kolommen in het model (bijvoorbeeld ID’s of alternatieve sleutels).
2. Maak een nieuw rapport via **Nieuw rapport**.
3. Voeg een **SalesTotal**-grafiek toe.
4. Koppel het met `Category` van `DimProduct`.
5. Wijzig de visualisatie naar **gegroepeerde staafdiagram**.
6. Geef de titel: *"Total Sales by Category"*.
7. Sla het rapport op als `Sales Report`.

---

## 🧹 Opruimen

1. Navigeer terug naar je werkruimte.
2. Ga naar **Werkruimte-instellingen**.
3. Kies **Verwijder deze werkruimte** om alle bijbehorende objecten te verwijderen.

---

## ✅ Resultaat

Na het voltooien van deze oefening heb je:

- Een Data Warehouse ingericht in Microsoft Fabric.
- Tabellen aangemaakt en gevuld via T-SQL.
- Relaties gelegd tussen feit- en dimensietabellen.
- Query’s geschreven en gevisualiseerd, zowel tekstueel als visueel.
- Een rapport gebouwd op basis van je dataset.

---

> 📘 Dit lab is onderdeel van de Microsoft Fabric leertrajecten.


![Schermafbeelding 2025-04-30 105045](https://github.com/user-attachments/assets/9f35bebf-c001-470e-b64c-662236aa04e5)


![Schermafbeelding 2025-04-30 105757](https://github.com/user-attachments/assets/f4cc55a9-f036-4a26-bcb6-8d5cd7d53f9e)



![Schermafbeelding 2025-04-30 105947](https://github.com/user-attachments/assets/1c479ec4-c8a9-4bb1-b8b6-f5b88b5b53ef)



![Schermafbeelding 2025-04-30 115752](https://github.com/user-attachments/assets/e6eb0905-a820-4aba-9703-750c10ec6f20)




![Schermafbeelding 2025-04-30 122835](https://github.com/user-attachments/assets/3faf34af-b40c-43ef-8ffa-c3965a52cdbe)



![Schermafbeelding 2025-04-30 123825](https://github.com/user-attachments/assets/a409167d-f518-4acd-bf83-ef55631600b9)


![Schermafbeelding 2025-04-30 124040](https://github.com/user-attachments/assets/4c8cd88c-4803-4ee2-ae0a-95cd4d5882f5)





![Schermafbeelding 2025-04-30 124113](https://github.com/user-attachments/assets/9fc37f1b-66b6-4a20-a2ea-091bd8225a1c)


![Schermafbeelding 2025-04-30 124306](https://github.com/user-attachments/assets/fae107a3-a6a2-4607-9326-d0ad11abd3e3)

![Schermafbeelding 2025-04-30 124452](https://github.com/user-attachments/assets/e2af48d9-8a12-47cd-950d-6bf3cdd8444a)

![Schermafbeelding 2025-04-30 125050](https://github.com/user-attachments/assets/ce6679e8-f853-49c5-995e-b0fcbca6bbff)


![Schermafbeelding 2025-04-30 125852](https://github.com/user-attachments/assets/22fc8d2f-cab0-49ae-9e14-bc311915bdc3)



![Schermafbeelding 2025-04-30 130041](https://github.com/user-attachments/assets/22cb4ccb-5833-49fa-a53d-8463586837b8)



![Schermafbeelding 2025-04-30 130124](https://github.com/user-attachments/assets/7ea8619f-5a8e-4a4c-8f9d-d17addac9e43)


![Schermafbeelding 2025-04-30 130618](https://github.com/user-attachments/assets/b94c514b-4b34-4c77-bebb-02bbd3816ef2)



![Schermafbeelding 2025-04-30 130711](https://github.com/user-attachments/assets/83e168e0-1b15-4b11-a9d5-74a537c6dc5e)








