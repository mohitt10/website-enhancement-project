# RIBBON SYSTEM SETUP GUIDE

## METHOD 1 — SCROLLSPY / SECTION SCROLLER  (Scroller.json)

### Use When

* Long pages with multiple sections
* Clicking button scrolls to section
* Active button changes while scrolling

Examples:

* Administration page
* Admissions sections
* Documentation sections

---

## Setup

### 1. Ribbon Buttons

For EVERY button:

#### CSS Class

```text
ribbon-btn
```

#### Link

```text
#section-id
```

Example:

```text
#chairman
#registrar
#deans
```

---

### 2. Target Sections

For EVERY target section/container:

#### CSS ID

```text
chairman
registrar
deans
```

DO NOT include `#`

---

### 3. Sticky Ribbon (Optional)

Ribbon container → CSS Class:

```text
sticky-ribbon
```

---

## Behavior

* Clicking button scrolls to section
* Active button changes while scrolling
* All sections remain visible normally

---

---

# METHOD 2 — TABS / PILLS (Tabs.json)

## Use When

* Only one content block visible at a time
* Clicking button switches content
* No scrolling behavior

Examples:

* UG / PG / MBA tabs
* FAQs
* Pricing tabs
* Feature tabs

---

## Setup

### 1. Ribbon Buttons

For EVERY button:

#### CSS Class

```text
ribbon-btn
```

#### Link

```text
#content-id
```

Example:

```text
#ug-content
#pg-content
#mba-content
```

---

### 2. Content Containers

For EVERY content section/container:

#### CSS Class

```text
tab-content
```

#### CSS ID

```text
ug-content
pg-content
mba-content
```

DO NOT include `#`

---

### 3. Sticky Ribbon (Optional)

Ribbon container → CSS Class:

```text
sticky-ribbon
```

---

## Behavior

* Only active content visible
* Other sections hidden
* Active button highlighted
* No scrolling

---

# MAIN DIFFERENCE

| Feature                        | Scrollspy | Tabs |
| ------------------------------ | --------- | ---- |
| Scrolls page                   | YES       | NO   |
| Multiple sections visible      | YES       | NO   |
| Active updates while scrolling | YES       | NO   |
| Content switching              | NO        | YES  |
