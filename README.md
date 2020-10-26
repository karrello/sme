# sme
Karrello for Sonor Music Editions

### Implementation

**Files**

- Paypal:  
  - `/assets/js/buttons.js`
  - `/assets/js/paypal-button.minjs`
- Karrello: `/assets/js/karrello.coffee`
- Includes:  
  - `/_includes/karrello/buy_box.html`
  - `_includes/karrello/cart.html`
- Style: in `/assets/css/stylesheet.sass` the `// KARRELLO` section
- Pages:  
  - `/assets/pages/cart.md`
  - `/assets/pages/checkout.md`
  - `/assets/pages/thankyou.md`
- Configuration: `/_data/karrello.yml`

**Code**

- Include scripts in `<head>`: `karrello.js` `buttons.js`
- Include style in `<head>`: `karrello.css`
- Body `data-title`:  
  `<body data-title="{{ page.title | slugify }}">`
- Cart link:  
  `<a href="{{ site.baseurl }}/cart" id="cart-link">View cart (<span>0</span>)</a>`
- Buy box in product page: `{%- include karrello/buy_box.html -%}`
- Remove `sandbox.` in `data-host` inside `karrello.coffee`

### Items Front Matter

```yml
---
author: Author
title: Title
volume: SME Volume
---

**Optional metadata**

- `soldout: true`
- `price: 0.00`
- `wholesale: 0.00`
```

### Configuration file: [`_data/karrello.yml`](https://github.com/karrello/sme/blob/main/_data/karrello.yml)

```yml
merchant: sb-vpvzq3424491@business.example.com

# Currency use three-character ISO-4217 codes
currency:
  code: EUR
  symbol: €

# Collections enabled to sell
collections:
  - catalog

# Items number for wholesale prices and shipping
wholesale:
  price: 3
  shipping: 6

# Max item quantity
max: 10

# Prices for every support
price:
  lp:
    few: 15
    many: 9
  dlp:
    few: 20
    many: 16

# Shipping prices
shipping:
  italy:
    few: 10
    many: 15
  europe:
    few: 15
    many: 20
  world:
    few: 20
    many: 40
```

### Paypal ocumentation

- [Archived **JavaScriptButtons** repository](https://web.archive.org/web/20161004203013/https://github.com/paypal/JavaScriptButtons)
- [Archived **HTML variables** Dev Docs](https://web.archive.org/web/20161227211543/https://developer.paypal.com/docs/classic/paypal-payments-standard/integration-guide/Appx_websitestandard_htmlvariables/)