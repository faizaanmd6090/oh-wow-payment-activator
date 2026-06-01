# oh-wow-payment-activator

Static GitHub Pages site that serves a single embedded admin page for the
[`oh-wow-payment-customization`](https://dev.shopify.com/dashboard) Shopify app.

## Purpose

Provides the `application_url` target for the `oh-wow-payment-customization`
Shopify app. When opened from inside Shopify Admin, it uses App Bridge Direct
API access to call `paymentCustomizationCreate` and activate the
`hide-dealer-bank-transfer` Shopify Function for the OH WOW Cycles store.

## Behavior

- Hides the manual payment method named `Dealer Bank Transfer` for any customer
  that does not have the `wholesale` tag.
- Customers with the `wholesale` tag still see `Dealer Bank Transfer`.

## Deploy

This repo serves a single `index.html` via GitHub Pages from the `main` branch.
No build step required.

## Scopes used

- `read_payment_customizations`
- `write_payment_customizations`
