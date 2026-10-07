# RFD: Sci-Fi Concept Storefront for the GMI Hy Image Challenge

**Status:** Draft  
**Owner:** Isayah Culbertson  
**Target:** GMI Cloud / Hy Image 3.5 Commercial Challenge  
**Working title:** `WORK OBJECTS_01`  
**Category:** Commercial / Brand System / Product Visualization  
**Deployment:** Vercel

## 1. Summary

Build a premium, Nike-like concept storefront for fictional sci-fi technology and fashion products generated with AI.

The experience should feel like a real high-end product brand: large editorial imagery, sparse typography, strong product identity, model photography, detailed product pages, and controlled motion. It is intentionally **not an ecommerce application**. Products are not purchasable; there is no cart, checkout, inventory, or fake transaction flow.

The core thesis is:

> **A storefront for products that do not exist yet, presented as though they already belong in the world.**

AI generation will be performed through a **GMI Cloud MCP server**, with Hy Image 3.5 used as the primary visual-generation system for challenge-relevant assets.

## 2. Goals

- Demonstrate Hy Image 3.5 as part of a complete commercial brand system rather than as an isolated image generator.
- Build a coherent fictional sci-fi product collection with repeatable visual identity.
- Generate consistent front, rear, gear-only, materials, detail, and campaign imagery.
- Present the collection through a polished storefront deployed on Vercel.
- Preserve generation provenance so the challenge workflow is auditable.
- Create an experience with premium fashion/technology mystique without implying that the fictional products can actually be purchased.

## 3. Non-Goals

The MVP will not include:

- cart
- checkout
- payments
- inventory
- shipping
- preorder flows
- fake prices
- user accounts
- a production commerce backend

The project is a **commercial visualization and brand-system experiment**, not an online store.

## 4. Creative Direction

The visual direction is:

**Sexy × Technical × Functional × Mysterious**

“Sexy” should come from silhouette, confidence, materiality, lighting, styling, and presence. It should not rely on explicit presentation, fetish framing, or provocative posing.

The desired result is closer to premium sportswear, luxury-tech, and editorial campaign photography.

### Design principles

- strong product silhouettes
- tactile materials
- restrained typography
- generous negative space
- confident adult models
- clear product identity
- technical detail without UI clutter
- realistic studio photography
- minimal cyberpunk clichés
- no anime styling for the core storefront campaign

## 5. Nike-Like Storefront Philosophy

“Nike-like” refers to the interaction and presentation philosophy, not direct imitation.

Desired characteristics:

- full-bleed hero imagery
- large product photography
- minimal navigation
- sparse editorial typography
- immersive product storytelling
- polished transitions
- strong mobile presentation
- product pages that feel like launches rather than catalog records

The project must not use Nike branding, logos, trademarks, product names, or pixel-copy Nike’s site.

## 6. Product Universe

The storefront presents fictional near-future products across several categories.

### Apparel

- technical coats
- adaptive outerwear
- performance bodysuits
- utility garments
- performance footwear

### Wearable technology

- helmets
- masks
- sensing systems
- augmented eyewear
- wearable compute
- environmental monitoring gear

### Personal equipment

- modular packs
- field equipment
- precision tools
- portable power systems
- communications devices

### Future expansion

- robots
- inspection systems
- scientific equipment
- autonomous field devices
- Mapped Assembly / OpenIndustries-generated physical products

The first release should stay intentionally small. Three strong products are better than a large inconsistent catalog.

## 7. Initial Collection

Working collection name:

## `SYSTEM_01`

### LOOK/01 — Technical Exploration System

A premium black, white, and gold technical outfit.

Core elements:

- technical stretch bodysuit
- water-resistant utility parka
- metallic thermal lining
- adjustable webbing harness
- modular thigh pouch
- reinforced platform boots
- anodized metal hardware

Required image set:

1. front model view
2. rear model view
3. gear-only view
4. materials / features infographic
5. editorial campaign image

### VEIL/01 — Adaptive Face System

A speculative wearable sensing and environmental interface.

Potential concepts:

- adaptive face coverage
- integrated optics
- environmental sensing
- modular filtration
- communications interface

### FIELD/01 — Personal Field System

A modular pack and equipment system intended for:

- exploration
- field engineering
- creative production
- scientific work
- travel

## 8. Product Page Experience

Example route:

```text
/products/look-01
```

Suggested page flow:

```text
Hero
 ↓
Product name + one-line statement
 ↓
Front view
 ↓
Back view
 ↓
Gear-only view
 ↓
Material details
 ↓
Feature callouts
 ↓
Ideal activities
 ↓
Editorial campaign image
 ↓
Related products
```

The page should feel like a product launch rather than a technical specification sheet.

## 9. Product Data Model

Each product should be represented as structured metadata.

```text
Product
  id
  name
  collection
  category
  tagline
  description
  materials[]
  features[]
  activities[]
  images[]
  generation_metadata
```

Example activity tags for `LOOK/01`:

- Urban exploration
- Travel days
- Creative production
- Convention / expo wear
- Night events
- Editorial shoots

## 10. GMI Cloud MCP Integration

All challenge-relevant AI image generation should be routed through a **GMI Cloud MCP server**.

Conceptual flow:

```text
Developer / Agent
        │
        ▼
GMI Cloud MCP Server
        │
        ▼
Hy Image 3.5
        │
        ▼
Generated Asset
        │
        ▼
Generation Metadata
        │
        ▼
Storefront
```

Expected MCP-driven workflows include:

```text
generate_product_hero()
generate_model_front()
generate_model_back()
generate_product_only()
generate_material_detail()
generate_infographic()
generate_campaign_image()
```

Exact tool names will depend on the GMI MCP server interface.

## 11. Generation Provenance

Each generated asset should preserve enough metadata to reproduce or audit the workflow.

Recommended fields:

```text
provider
model
prompt
timestamp
input_references
generation_id
mcp_tool
product_id
asset_role
```

Example:

```json
{
  "product": "LOOK-01",
  "asset_type": "front_model",
  "provider": "gmi-cloud",
  "model": "hy-image-3.5-preview",
  "references": [
    "look-01-concept",
    "look-01-material-reference"
  ]
}
```

This metadata does not need to be prominently visible on the public storefront.

## 12. Consistency Benchmark

A central technical experiment is whether one product can maintain a coherent identity across different commercial image roles.

```text
Design
  ↓
Front
  ↓
Back
  ↓
Gear only
  ↓
Detail
  ↓
Infographic
  ↓
Editorial scene
```

For `LOOK/01`, consistency should be evaluated across:

- coat geometry
- gold lining
- bodysuit paneling
- harness placement
- pouch placement
- boot design
- palette
- hardware language

This turns the project into a useful benchmark as well as a commercial artifact.

## 13. Asset Roles

Generated assets should use explicit roles:

```text
hero
model_front
model_back
product_only
detail
materials
infographic
editorial
environment
```

## 14. Storefront UX

### Homepage

The homepage should be visually sparse and image-led.

Example:

```text
SYSTEM_01

OBJECTS FOR
THE WORLD AHEAD.

[Full-screen campaign image]

EXPLORE COLLECTION
```

### Collection page

```text
SYSTEM_01

LOOK/01
Technical Exploration System

VEIL/01
Adaptive Face System

FIELD/01
Personal Field System
```

### Product page

The product page should initially reveal very little technical information.

Example:

> **LOOK/01**  
> Built for motion beyond familiar environments.

Detailed materials and feature information appear farther down the page.

## 15. AI Disclosure

The site should preserve mystique without misleading visitors into believing fictional goods are available for purchase.

Suggested footer or About disclosure:

> **A speculative product collection created through generative design and visualization.**

Challenge-specific copy may include:

> **Visualized using Hy Image 3.5 through GMI Cloud.**

## 16. Technical Architecture

```text
Next.js
TypeScript
Tailwind CSS
Framer Motion
        │
        ├── Static product metadata
        ├── Generated image assets
        └── Generation provenance
        │
        ▼
      Vercel
```

GMI generation should be decoupled from the public request path:

```text
GMI Cloud MCP
      │
      ▼
Hy Image 3.5
      │
      ▼
Generated assets + metadata
      │
      ▼
Next.js storefront
      │
      ▼
Vercel
```

The deployed site should serve optimized assets rather than invoking the model for every visitor request.

## 17. Suggested Repository Layout

```text
/
├── app/
│   ├── page.tsx
│   ├── collection/
│   ├── products/
│   │   └── [slug]/
│   └── about/
├── components/
│   ├── ProductHero.tsx
│   ├── ProductCard.tsx
│   ├── ProductGallery.tsx
│   ├── MaterialGrid.tsx
│   ├── FeatureCallout.tsx
│   └── CollectionHero.tsx
├── content/
│   └── products/
├── public/
│   └── products/
│       ├── look-01/
│       ├── veil-01/
│       └── field-01/
├── generation/
│   ├── prompts/
│   ├── references/
│   └── metadata/
└── rdf.md
```

## 18. Visual System

Primary palette:

```text
Black
White
Graphite
Silver
```

Accent:

```text
Champagne gold
```

Preferred photography:

- neutral studio backgrounds
- full-body front and rear views
- gear-only compositions
- macro material shots
- sharp product silhouettes
- controlled editorial lighting

Avoid:

- generic neon cyberpunk
- excessive holographic UI
- anime presentation for the main commercial campaign
- inconsistent product geometry
- inconsistent human anatomy
- overly sexualized poses

## 19. Model Presentation

The model exists to demonstrate the product.

Desired hierarchy:

```text
Product
  +
Human context
  +
Fashion
```

The model should appear confident, stylish, adult, and premium. Front and rear images should behave like professional apparel lookbook photography.

## 20. Challenge Deliverable

The GMI submission should link directly to the deployed Vercel site.

The project should demonstrate:

- image generation
- reference-conditioned generation
- product consistency
- model consistency
- fashion photography
- materials visualization
- infographic generation
- ad creative
- brand-system design
- commercial presentation

Potential submission title:

> **SYSTEM_01 — A Storefront for Products That Don't Exist Yet**

Potential description:

> SYSTEM_01 is a speculative commercial storefront built around AI-generated near-future products. Rather than presenting isolated AI images, the project uses Hy Image 3.5 through a GMI Cloud MCP workflow to build complete product identities across front and rear model photography, gear imagery, materials, technical details, and campaign visuals. The resulting collection is presented through a premium editorial storefront inspired by modern athletic and technology brands.

## 21. MVP

The challenge MVP requires:

### Website

- homepage
- collection page
- one polished product page
- Vercel deployment

### Initial product

- `LOOK/01`

### Visual assets

- front view
- back view
- gear-only view
- materials infographic
- one campaign hero

### Integration

- working GMI Cloud MCP generation workflow
- generation metadata retained for each challenge asset

## 22. Stretch Goals

After the MVP:

- three complete products
- animated hero transitions
- short campaign video
- interactive material inspection
- multi-angle product presentation
- alternate colorways
- additional collection drops
- generated environments
- OpenIndustries / Mapped Assembly-designed physical products
- CAD → GMI visualization pipeline

Longer-term pipeline:

```text
Mapped Assembly / OpenIndustries
            ↓
Structured physical design
            ↓
CAD / reference representation
            ↓
GMI Cloud MCP
            ↓
Hy Image
            ↓
Commercial product campaign
            ↓
Vercel storefront
```
