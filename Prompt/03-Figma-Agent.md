# Enterprise Design System Creation Prompt

## ROLE

Act as a **Principal Design System Architect** specializing in enterprise Design Systems such as IBM Carbon, Uber Base, Atlassian Design System, Material Design 3, Polaris, and Fluent.

Using the existing designs in this Figma file as the source of truth, create a complete, scalable, production-ready **Design System** using modern Figma Variables and enterprise token architecture.

The objective is to establish a clean, maintainable, and future-proof Design System that can scale across multiple products while preserving the existing product's visual language.

---

# PROJECT CONFIGURATION

Before creating the Design System, ask me for the following information if it has not already been provided:

### 1. Primary Brand Color (Required)

Example:
`#0057FF`

Use this as the base color for generating the complete Primary color scale.

---

### 2. Secondary Brand Color (Optional)

Example:
`#F4B400`

If a Secondary Brand Color is provided:

* Create the complete Secondary color scale.
* Create Brand/Secondary tokens.
* Create Primitive/Secondary tokens.
* Generate Semantic Tokens where required.

If a Secondary Brand Color is **not provided**, do **not** create:

* Brand/Secondary tokens
* Primitive/Secondary tokens
* Secondary Semantic Tokens

Do not invent or generate a secondary color palette.

---

### 3. Typography (Required)

"[Enter FOnt Name]" , Use this font for creating font tokens

---

# DESIGN SYSTEM PRINCIPLES

The Design System should be:

* Enterprise-grade
* Variable-driven
* Scalable
* Consistent
* Theme-ready
* Developer-friendly
* Easy to maintain
* Easy to extend
* Optimized for Figma Variables
* Built using reusable design decisions

Every design decision should exist only once.

Avoid duplication at every level.

---

# DESIGN SYSTEM HIERARCHY

Follow this hierarchy exactly.

Brand Tokens

↓

Primitive Tokens

↓

Semantic Tokens

├── Global Semantic Tokens

└── Component Semantic Tokens

Every layer must inherit from the previous layer.

Never skip inheritance.

---

# LEVEL 1 — BRAND TOKENS

Brand Tokens represent only the visual identity of the product.

Do not assign UI meaning.

Create collections for:

Brand/Primary/*

Brand/Secondary/* (Only if Secondary Brand Color is provided)

Brand/Neutral/*

Brand/Success/*

Brand/Error/*

Brand/Warning/*

Brand/Info/*

Include complete shade scales wherever applicable.

Also include:

Brand/White

Brand/Black

Brand/Transparent

Structure the Brand collection so additional themes can be introduced later without restructuring the Design System.

---

# OPACITY TOKENS

Create reusable opacity variables.

Opacity/0

Opacity/4

Opacity/8

Opacity/12

Opacity/16

Opacity/24

Opacity/32

Opacity/40

Opacity/48

Opacity/56

Opacity/64

Opacity/72

Opacity/80

Opacity/88

Opacity/100

These opacity tokens should be reused throughout the entire Design System.

---

# TYPOGRAPHY FOUNDATIONS

Create typography foundations independent from text styles.

Include:

## Font Family

Primary

Monospace (only if required)

## Font Weight

Regular

Medium

Semibold

Bold

## Font Size

Create a scalable typography scale.

## Line Height

Create proportional line-height variables.

## Letter Spacing

Create reusable tracking variables.

Generate reusable text styles for:

* Display
* Heading
* Title
* Body
* Label
* Caption

---

# FOUNDATION TOKENS

Create reusable variables for:

Spacing

Corner Radius

Border Width

Elevation

Blur (if applicable)

Motion Duration (if applicable)

Motion Easing (if applicable)

Only create foundations that are required by the product.

---

# LEVEL 2 — PRIMITIVE TOKENS

Primitive Tokens convert Brand Tokens into reusable product color families.

Create:

Primitive/Primary/*

Primitive/Secondary/* (Only if Secondary Brand Color exists)

Primitive/Neutral/*

Primitive/Success/*

Primitive/Error/*

Primitive/Warning/*

Primitive/Info/*

Primitive Tokens must remain completely independent from UI components.

---

# LEVEL 3 — GLOBAL SEMANTIC TOKENS

Create separate collections for:

* Light Theme
* Dark Theme

Every Semantic Token must inherit from a Primitive Token.

Never reference Brand Tokens directly.

Create semantic tokens for:

## Background

Primary

Secondary

Tertiary

Inverse

Brand

Success

Error

Warning

Info

---

## Surface

Primary

Secondary

Raised

Sunken

Overlay

---

## Text

Primary

Secondary

Tertiary

Disabled

Inverse

Brand

Success

Error

Warning

Info

---

## Icon

Primary

Secondary

Tertiary

Disabled

Inverse

Brand

Success

Error

Warning

Info

---

## Border

Primary

Secondary

Subtle

Strong

Focus

Disabled

Success

Error

Warning

Info

---

## Overlay

Light

Dark

Scrim

---

## State

Hover

Pressed

Focused

Selected

Dragged

Disabled

---

# SEMANTIC OPACITY TOKENS

Create opacity variants wherever appropriate.

Examples:

Text/Primary/100

Text/Primary/80

Text/Primary/60

Text/Primary/40

Icon/Primary/100

Icon/Primary/80

Border/Primary/100

Border/Primary/50

Background/Overlay/80

Background/Overlay/60

Support both Light and Dark themes.

---

# COMPONENT SEMANTIC TOKENS

Component Tokens are part of the Semantic layer.

Every Component Token must inherit only from Global Semantic Tokens.

Never reference Brand Tokens or Primitive Tokens directly.

Create semantic tokens for:

* Button
* Input
* Card
* Navigation
* Tabs
* Badge
* Chip
* Tag
* Modal
* Bottom Sheet
* Toast
* Banner
* Tooltip
* Avatar
* List Item

Each component should include only the semantic properties it requires, such as:

* Background
* Text
* Border
* Icon
* Hover
* Pressed
* Focused
* Disabled
* Error
* Selected

Reuse existing semantic tokens wherever possible.

---

# VARIABLE COLLECTIONS

Organize Variables into:

* Brand
* Primitive
* Foundation
* Typography
* Opacity
* Semantic – Light
* Semantic – Dark

Maintain proper inheritance between every collection.

---

# TOKEN NAMING

Use enterprise-grade naming conventions.

Names must be:

* Consistent
* Human-readable
* Predictable
* Scalable
* Future-proof

Every token should follow the inheritance path:

Brand → Primitive → Global Semantic → Component Semantic

---

# IMPLEMENTATION RULES

* Use Figma Variables for every reusable design decision.
* Eliminate hardcoded values wherever possible.
* Reuse variables throughout the Design System.
* Follow enterprise Design System standards.
* Keep the architecture modular and extensible.
* Build the Design System based on the existing product UI.

---

# DO NOT

* Do not create duplicate variables.
* Do not create duplicate colors.
* Do not hardcode values.
* Do not mix Brand, Primitive, and Semantic layers.
* Do not reference Brand Tokens directly inside Component Semantic Tokens.
* Do not reference Primitive Tokens directly inside Component Semantic Tokens.
* Do not invent unnecessary variables.
* Do not create Secondary color tokens unless a Secondary Brand Color is provided.

---

# FINAL DELIVERABLES

Create:

* Brand Tokens
* Opacity Tokens
* Typography Foundations
* Foundation Tokens
* Primitive Tokens
* Global Semantic Tokens (Light & Dark)
* Component Semantic Tokens
* Variable Collections

The resulting Design System should follow enterprise Design System standards, use a clean token hierarchy, and provide a robust foundation for future component creation and product scalability.
