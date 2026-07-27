# Sequoia ↔ Aoikumo Audit Reference

## Purpose
This file stores known reconciliation logic between Sequoia and Aoikumo.

## Core Questions
When checking differences, answer:
1. Did treatments reduce?
2. Did entitlement disappear?
3. Was it absorbed?
4. Was it converted to another package?

## Classification
1. Normal Mumsrelle Net Difference
2. Baby Fair Deposit Holding
3. PNSG Internal Billing Receivable
4. Plush Migrated Liability
5. Partner / Cash Wallet Exception

## Matching Rules
- Exclude Sequoia Outlet / Grand Total rows
- Match Sequoia Customer Ref No. to Aoikumo Identification #
- Remove Aoikumo SER prefix when matching
- Matching priority:
  1. ID + treatment
  2. Name + treatment
  3. Fuzzy match

## Known Corrections
- Kai Ling 凯绫 = 凯绫
- Tan Guo Rui changed name to Sarah Yap
- Goh Pei Yi Jenny exists in Aoikumo

## Important Rule
No Aoikumo entitlement means no match and no approved exception/conversion evidence.
