# Aoikumo Reference

## Purpose
This section stores Aoikumo POS, sales order, entitlement, and wallet handling references.

## Known Rules
- Aoikumo was used from 2026-02 onward.
- Sequoia retains older 2025 data.
- Cash Wallet handling:
  1. Manual Transaction recharge
  2. Pay with Cash Wallet
  3. For refund to wallet: Void original SO → backfill → create new SO for Wallet purchase

## Audit Use
When checking Sequoia vs Aoikumo:
- Use Sequoia as the base for historical entitlement comparison unless a newer rule states otherwise.
- Confirm whether missing entitlement is due to partner/CW exception, migration, conversion package, or true missing record.
