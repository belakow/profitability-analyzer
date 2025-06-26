# 3. Software Requirements Specification (SRS)

## 3.1. Purpose of the Document

This document describes the software requirements for the “Profitability Analyzer” module - a system for analyzing trip profitability. The system should enable a logistics specialist or analyst to accurately evaluate trip profitability before execution.

---

## 3.2. Scope of Application

The system is used by the logistics department of a transportation company for freight planning. Users input basic trip parameters, after which the system automatically calculates the total cost, expected margin, and indicates profitability.

---

## 3.3. Users

| Role              | Description                                           |
|-------------------|-------------------------------------------------------|
| Logistician       | Main user, inputs trip parameters                     |
| Department Head   | Makes decisions about executing the trip              |
| Analyst           | Analyzes the effectiveness of the system              |

---

## 3.4. Functional Requirements

| #   | Requirement                                                                 | Priority |
|-----|-----------------------------------------------------------------------------|----------|
| F1  | The system shall accept input of trip parameters: route, mileage per country, tonnage, cargo, delivery cost | High     |
| F2  | The system shall automatically calculate all costs based on predefined business rules | High     |
| F3  | The system shall compute revenue, total expenses, and margin (%)            | High     |
| F4  | The system shall display a profitability indicator: `✅ Profitable` / `⚠️ Unprofitable` | High     |
| F5  | The user shall be able to manually adjust cost rates (e.g., fuel price, exchange rate) | Medium   |
| F6  | The system shall log the history of trip calculations (date, parameters, result) | Low      |
| F7  | Data shall be stored in a format convenient for analysis (.xlsx/.csv)       | Medium   |

---

## 3.5. Non-Functional Requirements

| #   | Requirement                                                                                 | Priority |
|-----|----------------------------------------------------------------------------------------------|----------|
| N1  | The interface must be intuitive and usable without technical training                        | High     |
| N2  | Calculation time must not exceed 5 seconds                                                   | High     |
| N3  | The system should be extensible - new cost types can be added without code refactoring       | Medium   |
| N4  | Support for import/export of trip templates (CSV, Excel formats)                             | Medium   |
| N5  | Adaptation for desktop devices (mobile support optional)                                     | Low      |

---

## 3.6. Constraints

- The system is not connected to GPS or telematics in the first version.
- Costs are entered based on averages or manually.
- Data validation is minimal at this stage (number formats, units).

---

## 3.7. Example User Scenario (User Flow)

1. User opens the calculation module.
2. Inputs:
   - Route: Ivano-Frankivsk (UA) - Dresden (DE)
   - Distance: Ukraine – 204 km; Poland – 683 km; Germany – 110 km
   - Fuel price: 1.6 €/L
   - Cargo: Furniture
   - Tonnage: 12 tons
   - Client price: €1800
3. System:
   - Calculates expenses: fuel, depreciation, tolls, idle time
   - Displays cost: €1420
   - Calculates margin: €380 (21%)
   - Displays result: ✅ Profitable

---

## 3.8. Acceptance Criteria

- The system correctly calculates total cost from 5+ expense types
- Clearly displays profitability status
- Allows changing parameters and receiving updated results
