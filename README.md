# Warehouse tools

Small Python utilities for warehouse order and shipping workflows.

Run the tests with `python3 -m unittest discover -s tests -v`.

## Shipping

`shipping_quote(weight_kg, zone, service="standard")` returns a delivery quote.

- **Zones**: `local` or `regional`
- **Services**: `standard` (default) or `express` ($7 surcharge over standard)
- **weight_kg** must be positive

The command-line entry point prints a quote:

```
python -m warehouse.cli 2.0 local
python -m warehouse.cli 2.0 regional --service express
```
