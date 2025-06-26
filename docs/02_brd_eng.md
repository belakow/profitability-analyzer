# 2. Business Requirements Document (BRD)

## 2.1. Project Name

**Profitability Analyzer** - a module for analyzing trip profitability

## 2.2. Business Owner

Commercial Director of Trans-Atlas LLC - Anatolii Prylutskyi

## 2.3. Stakeholders

| Role                    | Name / Department           | Interest                                |
|-------------------------|-----------------------------|------------------------------------------|
| Business Analyst        | Dmytro Beliakov             | Needs analysis, requirements development |
| Head of Logistics       | Kryzhanovskyi O.            | Trip optimization                        |
| Chief Accountant        | Kruchkovska V.              | Cost control                             |
| Commercial Director     | Prylutskyi O.               | Financial results                        |
| IT Department Developer | Mandziuk D.                 | Technical implementation                 |

## 2.4. Business Objectives

- Identify unprofitable trips before execution
- Include all relevant costs during planning
- Provide a real-time margin evaluation tool
- Make informed trip decisions based on clear rules

## 2.5. Scope

**Included in the project:**
- Creation of a cost calculator (formulas, logic)
- Profitability model using a Decision Table
- Visual interface (prototype or real MVP)
- Documentation: BRD, SRS, Wireframe, Business Rules

**Not included in the project:**
- Full integration with Bitrix CRM
- Changes to client acquisition business processes
- Changes to transportation directions

## 2.6. High-Level Features

- Input trip parameters: route, tonnage, expected revenue
- Auto-fill cost data based on business rules
- Margin calculation
- Output message: "Profitable / Unprofitable"

## 2.7. Success Criteria

- At least 90% of low-margin trips are identified before execution
- Interface usage time per trip does not exceed 5 minutes
- No changes required in other systems for implementation
