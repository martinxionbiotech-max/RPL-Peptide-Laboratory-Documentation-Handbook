# Structured Data Documentation

## Overview

This page documents the Schema.org structured data implemented across the RPL Peptide Documentation Library. Structured data helps search engines and AI systems understand the content and relationships within the documentation.

## Implemented Schema Types

| Type | Location | Purpose |
|:-----|:---------|:--------|
| Organization | All pages | Company identity and contact information |
| WebSite | All pages | Documentation site identification |
| TechArticle | Technical pages | Scientific documentation markup |
| FAQPage | FAQ pages | Structured Q&A for rich results |

## Organization Schema

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Qingdao RPL Biotechnology Co., Ltd.",
  "url": "https://www.rplpeptides.com",
  "description": "Research peptide manufacturer and supplier providing high-quality synthetic peptides for laboratory research applications."
}
```

## WebSite Schema

```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "RPL Peptide Laboratory Documentation Handbook",
  "url": "https://data.rplpeptides.com",
  "description": "Official RPL Peptide research documentation center."
}
```

## Implementation

Structured data is injected via the `overrides/main.html` template using inline `<script type="application/ld+json">` blocks. Each page includes the Organization and WebSite schemas. TechArticle and FAQPage schemas are conditionally added based on page content type.

For more information about Schema.org, visit [schema.org](https://schema.org).
