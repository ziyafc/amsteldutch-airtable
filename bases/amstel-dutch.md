# Amstel Dutch

**Base ID:** `app8UfvWnkJWFKUpt`  
**Permission Level:** Create

## Overview

Simple product launch tracking database.

---

## Tables

### 1. Product Launches

**Table ID:** `tblnUG1lqNMIlLzdJ`

#### Fields

| Field Name | Type | Description | Options |
|------------|------|-------------|--------|
| Product Name | `singleLineText` | Name of the product | - |
| Status | `singleSelect` | Launch status | Not started, At risk, On track, Completed |
| Launch date | `date` | Scheduled launch date | Local format |
| Owner | `singleCollaborator` | Person responsible | - |
| Description | `richText` | Product description | - |

#### Views

- Grid view (`viwfS11RBmKUYXQL3`)

---

## Relationships

This base has no inter-table relationships.

---

## Usage Notes

- Ideal for tracking product launches with status workflow
- Status colors: Red (Not started), Yellow (At risk), Orange (On track), Green (Completed)