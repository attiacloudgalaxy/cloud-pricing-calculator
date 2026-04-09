# Cloud Pricing Calculator — Kilo Skill

An AI agent skill for calculating accurate cloud infrastructure costs using GCP and Azure retail pricing APIs. Query SKUs, filter by regions/instance types, convert pricing units (units/nanos to dollars), and generate cost estimates.

## What This Skill Does

- **Azure Pricing**: Query Azure Retail Prices API, calculate monthly costs, compare regions
- **GCP Pricing**: Query GCP Cloud Billing API, convert units/nanos, apply Windows surcharges
- **Inventory Validation**: Validate disk exports, VM mappings, detect RAM mismatches
- **Cost Analysis**: 3-Year TCO, dual-run cost modeling, RI/CUD comparison
- **BOQ Generation**: Generate proposal-ready Bills of Quantities

## When to Use

Trigger this skill when a user asks about:
- Cloud pricing for GCP or Azure resources
- SKU lookups by service type, region, or instance family
- Converting pricing API responses (units/nanos) to dollar amounts
- Comparing costs between regions or instance types
- Validating disk inventory exports or VM-to-cloud mappings
- Migration or Disaster Recovery cost analysis

## Quick Start

Install as a Kilo/Kilocode skill:

```bash
# Copy to local skills directory
cp -r skills/cloud-pricing-calculator ~/.kilo/skills/
```

Or reference directly via the Kilo Marketplace.

## Included Resources

### Scripts
| Script | Purpose |
|--------|---------|
| `azure_pricing.py` | Query Azure Retail Prices API |
| `gcp_pricing.py` | Query GCP Cloud Billing API |
| `price_calculator.py` | Convert units/nanos to dollar amounts |
| `disk_inventory_validator.py` | Validate Azure disk CSV exports |
| `vm_mapping_validator.py` | Validate Azure-to-GCP VM mappings |

### References
| Reference | Purpose |
|-----------|---------|
| `gcp_service_ids.md` | GCP service ID mappings |
| `gcp_regions.md` | GCP region code mappings |
| `azure_regions.md` | Azure region name mappings |
| `azure_disk_skus.md` | Azure managed disk tier mappings |
| `sku_patterns.md` | Common SKU filtering patterns |

## Real-World Origin

This skill was battle-tested during real-world multi-cloud DR and migration engagements, covering Azure-to-GCP pricing validation across multiple regions including Germany West Central and me-central2 (Dammam). It encodes hard-won lessons on nanos conversion, Windows license surcharges, SKU availability gaps, and inventory validation.

## License

Apache License 2.0 — see [LICENSE](LICENSE).
