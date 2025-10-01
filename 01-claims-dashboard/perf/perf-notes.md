# Performance Tuning Notes

### Scenario
Initial dashboard load was slow (1.8 seconds on main page).

### Diagnosis
- Identified heavy DAX measure using SUMX over a large table.
- Multiple bi-directional relationships in the data model.

### Fix
- Replaced SUMX with a base measure on a pre-aggregated column.
- Converted relationships to single-direction.
- Added Date dimension for clean time intelligence.

### Result
- **Before:** ~1.8 seconds (see screenshot below)
- **After:** ~350 ms (see screenshot below)

---

[Placeholder for screenshot]
[Placeholder for screenhot]
