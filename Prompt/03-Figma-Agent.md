# Enterprise Design System Creation Prompt

## ROLE

Act as a **Principal Design System Architect** specializing in enterprise Design Systems such as IBM Carbon, Uber Base, Atlassian Design System, Material Design 3, Polaris, and Fluent.

Using the existing designs in this Figma file as the source of truth, create a complete, scalable, production-ready **Design System** using modern Figma Variables and token architecture.

The objective is to establish a clean, maintainable, and future-proof Design System that can scale across multiple products while preserving the existing visual language.

Do not redesign the UI. Instead, extract reusable design decisions and organize them into a structured Design System.

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

```
Brand Tokens
        ↓
Primitive Tokens
        ↓
Semantic Tokens
    ├── Global Semantic Tokens
    └── Component Semantic Tokens
```

Every layer must inherit from the previous layer.

Never skip inheritance.

---

# LEVEL 1 — BRAND TOKENS

Brand Tokens represent the visual identity of the product.

They contain only raw brand colors.

Do not assign UI meaning.

Organize colors into:

Brand/Primary/*
Brand/Secondary/*
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

Structure the Brand collection so additional themes (such as Red Theme or Gold Theme) can be added later without changing the architecture.

---

# OPACITY TOKENS

Create reusable opacity variables.

Examples:

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

Opacity variables should be shared throughout the Design System.

---

# TYPOGRAPHY FOUNDATIONS

Create typography foundations independent from text styles.

Include:

## Font Families

Primary

Secondary

Monospace

## Font Weights

Regular

Medium

Semibold

Bold

## Font Sizes

Create a scalable typography scale based on the existing designs.

## Line Heights

Create proportional line-height variables.

## Letter Spacing

Create reusable tracking variables.

Typography foundations should be reusable throughout the system.

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

Only create foundations that are required by the existing product.

---

# LEVEL 2 — PRIMITIVE TOKENS

Primitive Tokens convert Brand Tokens into reusable product color families.

Create:

Primitive/Primary/*

Primitive/Secondary/*

Primitive/Neutral/*

Primitive/Success/*

Primitive/Error/*

Primitive/Warning/*

Primitive/Info/*

Primitive Tokens should remain independent from any UI component.

Never create Button, Card, Input, Text, Border or Background tokens here.

---

# LEVEL 3 — GLOBAL SEMANTIC TOKENS

Create separate collections for:

* Light Theme
* Dark Theme

Every Semantic Token must inherit from a Primitive Token.

Never reference Brand Tokens directly.

## Background

Background/Primary

Background/Secondary

Background/Tertiary

Background/Inverse

Background/Brand

Background/Success

Background/Error

Background/Warning

Background/Info

---

## Surface

Surface/Primary

Surface/Secondary

Surface/Raised

Surface/Sunken

Surface/Overlay

---

## Text

Text/Primary

Text/Secondary

Text/Tertiary

Text/Disabled

Text/Inverse

Text/Brand

Text/Success

Text/Error

Text/Warning

Text/Info

---

## Icon

Icon/Primary

Icon/Secondary

Icon/Tertiary

Icon/Disabled

Icon/Inverse

Icon/Brand

Icon/Success

Icon/Error

Icon/Warning

Icon/Info

---

## Border

Border/Primary

Border/Secondary

Border/Subtle

Border/Strong

Border/Focus

Border/Disabled

Border/Success

Border/Error

Border/Warning

Border/Info

---

## Overlay

Overlay/Light

Overlay/Dark

Overlay/Scrim

---

## State

State/Hover

State/Pressed

State/Focused

State/Selected

State/Dragged

State/Disabled

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

Organize tokens by component.

Create tokens for:

## Button

Primary

Secondary

Tertiary

Ghost

Link

Include:

Background

Text

Border

Icon

Hover

Pressed

Focused

Disabled

---

## Input

Background

Text

Placeholder

Border

Focus

Error

Disabled

Label

Helper Text

---

## Card

Background

Border

Title

Subtitle

Shadow

---

## Navigation

Background

Text

Icon

Indicator

---

## Tabs

Active

Inactive

Indicator

---

## Badge

Background

Text

Border

---

## Chip

Background

Text

Border

---

## Tag

Background

Text

Border

---

## Modal

Background

Header

Border

Overlay

---

## Bottom Sheet

Background

Header

Handle

Border

---

## Toast

Background

Text

Icon

---

## Banner

Background

Text

Icon

---

## Tooltip

Background

Text

---

## Avatar

Background

Text

Border

---

## List Item

Background

Text

Icon

Border

---

# VARIABLE COLLECTIONS

Organize Variables into clean collections such as:

* Brand
* Primitive
* Foundation
* Typography
* Opacity
* Semantic – Light
* Semantic – Dark

Maintain clear inheritance between collections.

---

# TOKEN NAMING

Use enterprise-grade naming conventions.

Names must be:

* Consistent
* Human-readable
* Predictable
* Scalable
* Future-proof

Ensure every token follows a logical inheritance path from Brand → Primitive → Global Semantic → Component Semantic.

---

# IMPLEMENTATION RULES

* Use Figma Variables for every reusable design decision.
* Eliminate hardcoded colors wherever possible.
* Eliminate duplicate values.
* Reuse variables across the entire Design System.
* Follow modern enterprise Design System standards.
* Keep the system modular and extensible.
* Preserve the existing visual language while improving structure and maintainability.

---

# DO NOT

* Do not redesign existing screens.
* Do not invent new visual styles.
* Do not create duplicate variables.
* Do not create duplicate colors.
* Do not hardcode values.
* Do not mix Brand, Primitive, and Semantic layers.
* Do not reference Brand Tokens directly inside Component Semantic Tokens.
* Do not reference Primitive Tokens directly inside Component Semantic Tokens.
* Do not create unnecessary variables.
* Do not build components until the token architecture has been fully established.

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

The resulting Design System should reflect enterprise Design System standards, be fully variable-driven, and provide a solid foundation for future component creation and product scalability.
