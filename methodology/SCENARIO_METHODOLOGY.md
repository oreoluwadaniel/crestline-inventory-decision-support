# Crestline Scenario & What-If Methodology

## 1. Purpose

This document explains how the Crestline inventory decision-support model should be interpreted and validated.

The central principle is:

> **Scenario analysis is a decision-support tool, not a prediction of guaranteed future outcomes.**

---

# 2. Scenario Framework

Each scenario modifies one or more business assumptions.

```text
Base Data
   ↓
Scenario Assumptions
   ↓
Recalculation
   ↓
Scenario KPIs
   ↓
Comparison with Base Case
   ↓
Decision
```

---

# 3. Scenario Set

| Scenario | Primary Question |
|---|---|
| Base Case | What does the current modeled position look like? |
| Supplier Crisis | What happens if supplier availability/lead time deteriorates? |
| Demand Spike | What happens if demand increases? |
| Demand Decline | What happens if demand decreases? |
| Cost Shock | What happens if procurement costs rise? |
| Naira Slide | What happens if currency pressure raises relevant costs? |
| Bulk Deal | Does a discount justify additional inventory? |

---

# 4. Base Case

The Base Case is the reference scenario.

All other scenarios should be evaluated relative to it.

For each scenario:

```text
Scenario KPI − Base KPI
```

should be used to understand the modeled change.

---

# 5. Demand Scenarios

## Demand Spike

The model increases demand according to the scenario assumption.

Potential effects:

- Higher projected consumption
- Higher reorder requirements
- Greater stockout exposure
- Higher inventory requirement
- Higher working-capital requirement

## Demand Decline

The model decreases demand according to the scenario assumption.

Potential effects:

- Lower replenishment requirement
- Lower stockout pressure
- Greater excess-inventory risk
- Reduced purchasing requirement

---

# 6. Supplier Crisis

A supplier crisis scenario should represent deterioration in one or more supplier conditions.

Potential variables include:

- Lead time
- Availability
- Supplier concentration
- Procurement cost

The scenario is useful for testing whether the current inventory buffer is sufficient.

---

# 7. Cost Shock

A cost-shock scenario changes procurement cost assumptions.

The analysis should distinguish between:

### Unit-cost effect

Change in purchase price.

### Inventory-value effect

Change in the value of inventory held.

### Margin effect

Potential effect on commercial economics if selling prices are not adjusted.

---

# 8. Currency Scenario

The Naira Slide scenario represents an adverse currency environment affecting relevant procurement costs.

The scenario should be interpreted as:

> **A stress test of procurement and inventory economics under currency pressure.**

It is not a currency forecast.

---

# 9. Bulk Deal Analysis

The bulk-deal scenario evaluates whether purchasing additional units at a discount creates net economic value.

The basic decision framework is:

```text
Purchase Discount
       +
Potential Avoided Future Cost
       −
Incremental Holding Cost
       −
Working-Capital Cost
       −
Obsolescence / Slow-Movement Risk
       =
Net Scenario Effect
```

A positive discount does not automatically mean the deal is economically attractive.

---

# 10. Inventory Value

Inventory value should be calculated consistently using the methodology implemented in the workbook.

The documentation should use the same definition throughout:

```text
Inventory Quantity × Applicable Unit Cost
```

where appropriate.

Any alternate valuation method should be explicitly documented.

---

# 11. Excess / Slow-Moving Inventory

The final model should use **one clearly documented definition** for excess or slow-moving inventory.

Do not mix:

- 90-day rules
- 180-day rules
- Months-of-cover rules

without explicitly distinguishing them.

If the workbook uses months of cover as the final methodology, portfolio documentation should use that methodology consistently.

---

# 12. Stockout Exposure

Stockout exposure should be interpreted as a modeled risk indicator.

It is not automatically equivalent to realized lost sales.

Where a lost-sales log exists, distinguish:

```text
Observed / recorded lost sales
```

from:

```text
Modeled future stockout exposure
```

---

# 13. Warehouse Analysis

Warehouse-level analysis can support:

- Utilization comparison
- Inventory concentration
- Rebalancing
- Transfer opportunities
- Service-level analysis

A warehouse with high utilization is not automatically inefficient.

The decision should consider:

- Demand
- Inventory value
- Capacity
- Product mix
- Service requirements

---

# 14. Financial Scenario Interpretation

All financial outputs in this portfolio project should be labeled as one of:

### Observed

Directly present in the supplied synthetic dataset.

### Calculated

Derived mathematically from observed data.

### Modeled

Produced by applying assumptions or business rules.

### Illustrative

Used to demonstrate potential business impact.

Avoid presenting modeled or illustrative values as realized savings.

---

# 15. Validation Framework

Before publishing or presenting the workbook:

### Test 1 — Base Case

Confirm the Base Case loads correctly.

### Test 2 — Scenario Change

Select each scenario individually.

### Test 3 — KPI Propagation

Confirm relevant KPIs change where expected.

### Test 4 — Dashboard Consistency

Confirm dashboard values match the underlying calculations.

### Test 5 — Reset

Return to Base Case and confirm original values return.

### Test 6 — Formula Integrity

Check for:

- Errors
- Broken references
- Unexpected blanks
- Circular references

### Test 7 — Refresh

Run the workbook's refresh process and confirm outputs remain valid.

---

# 16. Interpretation Rules

The model should not be interpreted as:

> "This is exactly what will happen."

It should be interpreted as:

> **"Under these assumptions, this is the modeled consequence."**

That distinction is central to responsible decision modeling.

---

# 17. Recommended Decision Output

Every scenario should ultimately answer:

### What changed?

Identify the changed assumption.

### What happened?

Show the KPI impact.

### Why does it matter?

Explain the operational/financial trade-off.

### What should management do?

Provide a recommendation supported by the model.

---
