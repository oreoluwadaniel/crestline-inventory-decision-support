# Crestline Inventory Decision Support

**An Excel inventory planning model that lets purchasing teams test demand, supply, cost, and FX scenarios before committing working capital.**

Crestline is a fictional five-warehouse distributor in Nigeria. The model is built around a simple business question:

> **If conditions change next month, what happens to inventory, service levels, cost, and cash?**

Instead of reporting only what happened, the workbook lets a manager change the assumptions and see the likely operational and financial impact.

## The business problem

Inventory creates two competing risks.

**Too much stock:** cash is tied up, storage costs rise, and excess inventory becomes harder to move.

**Too little stock:** service levels fall, stockouts increase, and sales can be lost.

The right decision depends on demand, supplier lead times, procurement cost, warehouse capacity, and the level of risk the business is willing to accept.

Crestline's model brings those factors together so purchasing decisions can be tested before money is committed.

---

## What the model does

A scenario selector controls the assumptions used throughout the workbook.

The model currently includes seven operating scenarios:

| Scenario | Business question |
|---|---|
| Base Case | What happens under current assumptions? |
| Supplier Crisis | What if supplier lead times double? |
| Demand Spike | What if demand increases by 30%? |
| Demand Decline | What if demand falls by 15%? |
| Procurement Cost Shock | What if procurement costs rise by 12%? |
| FX Stress | What if imported costs increase by 20% from FX pressure? |
| Bulk Deal | Does a large supplier discount still make sense after considering inventory and working capital? |

The **Bulk Deal** scenario is particularly useful because a lower unit price does not automatically mean a better purchasing decision.

The model tests the full consequence:

**Discount → larger order → higher inventory → storage cost → working capital tied up → service and financial impact**

---

## Executive view

The dashboard recalculates against the selected scenario and shows:

- Inventory value
- Inventory turnover
- Days of inventory
- Fill rate
- OTIF
- Excess stock
- Annual cost impact
- Average inventory
- Change versus the Base Case

A scenario comparison table also shows the assumptions behind each case, so the user can see **what changed before interpreting the result**.

---

## How it works

```text
Raw operational data
        ↓
Inventory calculations
        ↓
Demand analysis
        ↓
Scenario engine
        ↓
Scenario impact calculations
        ↓
Executive dashboard
