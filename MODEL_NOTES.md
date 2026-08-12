# Model Notes

## Decision model

```text
Inventory and demand inputs
          |
          v
Baseline inventory position
          |
          v
Scenario selection
          |
          +--> service level
          +--> stock position
          +--> inventory value
          +--> working-capital exposure
          |
          v
Scenario comparison
          |
          v
Management decision
```

## Controls

The model separates actual historical values from scenario outputs. Scenario outputs are estimates based on the selected assumptions and should not be presented as actual performance.

The bulk-purchase case is assessed on total economic cost, not only the lower unit price. Holding cost and inventory exposure therefore remain part of the decision.

## Validation priority

Scenario outputs should be checked against known baseline values before a scenario is used for a management decision.
