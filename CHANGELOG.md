# Changelog: world.opensemantic.quantities

Migration from SPARQL-based extraction to enriched QUDT JSON-LD (qudt-parsing).
QUDT version: 3.1.4

## Summary

| Metric | Count |
|--------|-------|
| Old items | 1369 |
| New items | 1369 |
| Removed | 0 |
| Added | 0 |
| Common | 1369 |

## Known Limitations

- Some QUDT quantity kinds have no `applicableUnit` linked (e.g., BloodGlucoseLevel variants).
  These appear as removed characteristics with no replacement, as the old code used different join logic.
- Duplicate units exist in QUDT (e.g., `unit:FemtoM` and `unit:FEMTOM`) causing duplicate enum entries.

## Item Changes by Type

| Type | Removed | Added |
|------|---------|-------|

## Removed Items

## Added Items

## Changed Items

