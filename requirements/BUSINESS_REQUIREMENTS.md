# Crestline Inventory Decision Support System
## Business Requirements & Solution Specification

**Portfolio Case Study: Version 1.0**

---

# 1. Document Purpose

This document defines the business requirements and solution scope for the Crestline Inventory Decision Support System.

Crestline Distribution Ltd is a **fictional case-study company**. The document is therefore a portfolio requirements specification, not a signed client contract or production implementation document.

---

# 2. Business Context

Crestline operates a multi-warehouse distribution model and needs better visibility into:

- Inventory levels
- Demand
- Stockout exposure
- Excess inventory
- Supplier performance
- Warehouse allocation
- Purchasing decisions
- Working-capital implications

The business needs a decision-support mechanism that can evaluate alternative operating conditions before management commits to a purchasing or inventory action.

---

# 3. Problem Statement

Management currently faces a trade-off:

### Understocking

Can lead to:

- Lost sales
- Stockouts
- Poor service levels
- Emergency procurement

### Overstocking

Can lead to:

- Excess working capital
- Storage costs
- Slow-moving inventory
- Purchasing inefficiency

The solution must therefore support **balanced inventory decisions**, rather than optimizing for inventory reduction alone.

---

# 4. Business Objectives

The solution should enable management to:

1. Monitor inventory value and position.
2. Identify stockout exposure.
3. Identify excess or slow-moving inventory.
4. Evaluate supplier and purchasing conditions.
5. Compare warehouse inventory positions.
6. Evaluate demand scenarios.
7. Test procurement cost scenarios.
8. Evaluate bulk-purchase decisions.
9. Assess potential working-capital implications.
10. Make purchasing and rebalancing decisions using explicit assumptions.

---

# 5. Functional Requirements

## FR-01: Inventory Visibility

The solution shall display inventory position across the modeled warehouse network.

---

## FR-02: Warehouse Analysis

The solution shall allow management to compare inventory and utilization indicators across:

- Lagos Main
- Lagos Annex
- Ibadan
- Abuja
- Port Harcourt

---

## FR-03: Demand Analysis

The solution shall use historical sales information to support demand analysis and planning.

---

## FR-04: Stockout Analysis

The solution shall identify products or conditions associated with elevated stockout exposure.

---

## FR-05: Excess Inventory Analysis

The solution shall identify inventory that may represent excess or slow-moving stock based on the documented methodology.

---

## FR-06: Supplier Analysis

The solution shall support review of supplier-related factors such as:

- Cost
- Lead time
- Delivery performance
- Sourcing risk

where the relevant data is available.

---

## FR-07: Scenario Analysis

The solution shall allow the user to select predefined scenarios and recalculate relevant outputs.

Required scenarios:

1. Base Case
2. Supplier Crisis
3. Demand Spike
4. Demand Decline
5. Cost Shock
6. Naira Slide
7. Bulk Deal

---

## FR-08: Executive Dashboard

The solution shall provide an executive dashboard showing the most important inventory and scenario KPIs.

---

## FR-09: Validation

The solution shall include checks confirming that scenario changes propagate correctly through calculations and dashboard outputs.

---

# 6. Non-Functional Requirements

## Accuracy

Calculations should be formula-driven and traceable.

## Usability

A decision-maker should be able to select a scenario without modifying underlying formulas.

## Transparency

Important assumptions should be visible and documented.

## Reproducibility

The workbook should recalculate from the provided source data and assumptions.

## Maintainability

The model should separate:

- Raw/loaded data
- Calculations
- Assumptions
- Scenario logic
- Presentation

where practical.

---

# 7. Scenario Requirements

## Base Case

Represents the reference operating condition.

Used as the comparison point for all other scenarios.

---

## Supplier Crisis

Represents deterioration in supplier availability or lead time.

The model should allow management to assess:

- Inventory exposure
- Reorder implications
- Alternative sourcing requirements
- Potential service-level risk

---

## Demand Spike

Represents an increase in demand.

The model should show implications for:

- Inventory requirements
- Stockout risk
- Purchasing
- Working capital

---

## Demand Decline

Represents a decrease in demand.

The model should show implications for:

- Replenishment
- Excess inventory
- Working capital
- Purchasing commitments

---

## Cost Shock

Represents an increase in procurement cost.

The model should show implications for:

- Purchase cost
- Inventory value
- Margin
- Purchasing decisions

---

## Naira Slide

Represents an adverse currency movement affecting relevant procurement costs.

The model should show the effect on:

- Unit cost
- Inventory value
- Purchasing timing
- Financial exposure

---

## Bulk Deal

Represents a discounted supplier purchase.

The decision should compare:

```text
Purchase Discount
        VS
Incremental Holding / Inventory Cost
```

The model should not assume that a discount is automatically beneficial.

---

# 8. Decision Rules

The system should support management decisions such as:

### Purchase

Purchase when projected demand and inventory position justify additional stock.

### Delay

Delay purchasing when current inventory is sufficient and the scenario does not justify additional working-capital exposure.

### Rebalance

Transfer inventory when one warehouse has excess while another has elevated demand or stockout exposure.

### Review Supplier

Investigate suppliers with materially poor cost, lead-time, or delivery characteristics.

### Reject Bulk Deal

Reject a bulk discount when incremental holding and working-capital costs outweigh the purchase benefit.

---

# 9. KPI Requirements

The executive dashboard should surface relevant measures such as:

- Inventory Value
- Stockout Exposure
- Excess Inventory
- Warehouse Utilization
- Demand
- Forecast
- Holding Cost
- Scenario Impact
- Working-Capital Effect

Exact KPI definitions should remain aligned with the final workbook formulas.

---

# 10. Business Impact Measurement

Because this is a synthetic portfolio case study, no production business outcome is claimed.

For a real implementation, the following baseline and post-implementation measures should be tracked:

- Inventory value
- Inventory turns
- Stockout rate
- Lost-sales value
- Excess inventory value
- Holding cost
- Purchase price variance
- Forecast accuracy
- Warehouse utilization
- Month-end reporting time

---

# 11. Acceptance Criteria for a Real Implementation

A production implementation should demonstrate:

1. Scenario selector works.
2. Scenario outputs recalculate correctly.
3. Dashboard values match calculation outputs.
4. Source data refreshes successfully.
5. Validation checks pass.
6. Key assumptions are documented.
7. User permissions are appropriate.
8. Error handling is documented.
9. Baseline KPIs are recorded.
10. Post-implementation KPIs can be compared against baseline.

---

# 12. Scope

### In Scope

- Inventory analysis
- Demand analysis
- Warehouse analysis
- Supplier analysis
- Scenario modeling
- What-If analysis
- Executive reporting
- Validation

### Out of Scope

- Automatic purchase-order submission
- Live ERP integration
- Automated supplier contracting
- Production deployment
- Real-time inventory synchronization
- Guaranteed financial outcomes

---

# 13. Governance

A real implementation would require:

- Data ownership
- Model ownership
- Assumption approval
- Change control
- Version control
- User access control
- Periodic validation

---
