# RLCS Documentation (Retail Logistics Control System)

## Architecture

+----------+     +----------+     +-----------+
| Module 1 | --> | Module 2 | --> | Module 3  |
+----------+     +----------+     +-----------+
|                                |
+----------+                      +-----------+
| Module 4 | <------------------- | Module 5  |
+----------+                      +-----------+

InventoryItem <- PerishableItem, ElectronicsItem, FragileItem

## State and scope tracking

| Name | Kind | Where |
|---|---|---|
| checked_count | nonlocal | create_stock_audit_filter |
| total_system_items | global | InventoryItem counter |
| _InventoryItem__stock | mangled | InventoryItem |

## Module compliance checklist
- [x] Unit 1 loops and arithmetic (Depreciation, storage fee calculations, interactive CLI)
- [x] Unit 2 parser and closures (Semicolon log parser, nonlocal tracking filters)
- [x] Unit 3 comprehensions (Reverse catalog indexing, duplicate item queue filtration)
- [x] Unit 4 file I/O (Safe in-place ledger editing with dual-file error handling)
- [x] Unit 5 OOP (Base item abstractions, name mangling, custom structural sub-exceptions)
