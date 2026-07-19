---
title: Document ID Glossary
category: Documentation
keywords:
- document ID
- document number
- document identifier
- unique ID
---

# Document ID

## Definition

A Document ID is a unique alphanumeric code assigned to each document within a quality management system, enabling unambiguous identification and cross-referencing.

## Overview

Document IDs are the backbone of document management. Each document (TDS, COA, SDS, SOP, white paper) receives a unique ID that stays with it throughout its lifecycle, regardless of revision.

## Technical Explanation

**Document ID Structure (RPL Peptide Example):**

| Code Section | Meaning |
|---|---|
| RPL | Company prefix |
| TM | Document type (Technical Manual) |
| WP | White Paper |
| TDS | Technical Data Sheet |
| COA | Certificate of Analysis |
| SDS | Safety Data Sheet |
| -001 | Sequence number |

**Examples:**
- RPL-WP-PUR-001 = White Paper, Purity topic, version 001
- RPL-TM-BPC-001 = Technical Manual, BPC-157, version 001

**Properties:**
- Unique (no two documents share the same ID)
- Persistent (ID remains the same across revisions)
- Structured (encodes document type and topic)
- Searchable (enables cross-referencing)

## Importance in Peptide Documentation

Document IDs enable efficient cross-referencing within the documentation ecosystem. White papers can reference TDS documents by ID, COAs reference batch numbers, and quality system audits track document IDs.

## Related Terms

- [Revision](./revision.md)
- [Version Control](./version-control.md)
- [Document Traceability](./document-traceability.md)

## Frequently Asked Questions

**Q: Can I use a Document ID to find related documents?**
A: Yes. The Document ID structure allows you to identify document type and topic. For example, documents with "BPC" in the ID are related to BPC-157.

**Q: Does the Document ID change when a document is revised?**
A: No. The Document ID is permanent. Only the version/revision number changes. This ensures all references to the document remain valid.
