# Week 02 - Linux Commands

## 1. Count CSV Lines
`wc -l module-01/data/orders_oct2026.csv`

## 2. Count Log Lines
`wc -l module-01/data/app_2026-10.log`

## 3. Count WARN Messages
`grep -c "| WARN" module-01/data/app_2026-10.log`

## 4. Count DEBUG Messages
`grep -c "| DEBUG" module-01/data/app_2026-10.log`

## 5. Count ERROR Messages on October 10
`grep "^2026-10-10" module-01/data/app_2026-10.log | grep -c "| ERROR |"`

## 6. Find Dates with the Most WARN Messages
`grep "| WARN" module-01/data/app_2026-10.log | cut -c1-10 | sort | uniq -c | sort -rn`

## 7. Count bKash Orders
`grep -c ",bKash," module-01/data/orders_oct2026.csv`

## Bonus 1. Count auth Component ERROR Messages
`grep "| ERROR |" module-01/data/app_2026-10.log | grep -c "| auth"`

## Bonus 2. Find Dates with the Fewest ERROR Messages
`grep "| ERROR |" module-01/data/app_2026-10.log | cut -c1-10 | sort | uniq -c | sort -n`
