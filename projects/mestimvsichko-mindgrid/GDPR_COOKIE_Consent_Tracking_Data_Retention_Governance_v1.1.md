# GDPR-COOKIE-01 v1.1 — Consent, Tracking & Data Retention Governance Plan

**Project:** Mestimvsichko.bg  
**Assigned To:** WP Site Care GPT + PM Assistant + Content/Client Relations GPT  
**Scope:** Planning + staging implementation only  
**Live:** HOLD  
**Legal status:** Technical/compliance preparation, not legal certification  
**Editable Drive document:** https://docs.google.com/document/d/1Kv6AKmHQUVikLSTkEG7Y7pxUmHZV6e0fl85Is-NRVIY/edit?usp=drivesdk

---

## PM Control Status

This file registers the GDPR/cookie governance artifact in the PM/control repository for `projects/mestimvsichko-mindgrid/`.

The full editable working version has been created in Google Drive under the configured `Mestimvsichko.bg` folder. The Drive document contains the operational checklist and governance plan for consent, tracking, data retention, request-system storage mapping, YouTube embed handling, and staging audit preparation.

No implementation repository changes were made. No live or staging site changes were made.

---

## Summary

The GDPR/cookie workstream is necessary because the site uses or may use:

- Google Analytics / GA4;
- Google Tag Manager;
- YouTube embeds;
- future Meta Pixel;
- future Google Maps;
- future reCAPTCHA;
- contact/request forms that process personal data;
- potential photo uploads through the request flow.

The correct scope is not just a cookie banner. The required work is:

1. Cookie/consent governance.
2. GTM/GA4 consent-control setup.
3. External-media blocking before consent.
4. Request-system data storage mapping.
5. Retention matrix and manual deletion/anonymization SOP.
6. Privacy notice around forms and photo uploads.
7. Staging audit before live changes.

---

## Tracking & Script Inventory

| Service | Status | Category | Consent control |
|---|---:|---|---|
| GA4 | Active/Future | Analytics | Yes / Consent Mode |
| GTM | Active/Future | Consent infrastructure | Special handling; must not bypass CMP |
| YouTube | Active | External media | Block before external-services consent |
| Meta Pixel | Future | Marketing | Marketing consent only |
| Google Maps | Future | External service | Consent or static fallback |
| reCAPTCHA | Future | Security/external | Separate assessment required |
| Contact Form 7 | Future/Planned | Functional form | No cookie consent if no tracking; privacy notice required |
| WP Mail SMTP / logs | Future | Operational | Retention policy required |
| Embedded reviews/widgets | Future | External/social proof | Block before consent |
| Google Fonts CDN | Avoid/TBD | External dependency | Prefer local fonts |

---

## Storage Mapping Required for MindGrid Request System

The next audit must confirm:

- whether requests are stored as `mgrs_request` CPT;
- exact post meta keys for contact and request fields;
- whether address/access details are stored;
- whether uploaded photos are WP attachments or custom file paths;
- whether automatic cleanup exists;
- which admin roles/capabilities can access requests;
- whether export exists;
- whether delete/anonymize exists;
- whether email notifications contain personal data;
- whether mail/form/debug logs keep submission content.

---

## Working Retention Matrix

This is a PM working framework, not final legal policy.

| Data | Purpose | Working retention | After retention |
|---|---|---:|---|
| Unaccepted inquiries | Reply to request | 6 months | Delete/anonymize |
| Accepted/completed requests | Organization + traceability | 12 months after completion | Delete/anonymize unless dispute |
| Uploaded photos | Volume/access assessment | 30–90 days after closure | Delete |
| Email notifications | Operational communication | Mailbox policy | Cleanup/archive policy |
| Analytics consent logs | Consent proof | 6–12 months or CMP policy | Automatic cleanup |
| Contact form logs | Debug/deliverability | 7–30 days | Delete |
| Error/debug logs | Technical diagnostics | 7–30 days | Delete/rotate |
| Accounting documents | Legal accounting | Separate statutory rules | Outside website scope |
| Backups | Disaster recovery | 30–90 days | Rotation/delete |

---

## Cookie Banner Requirements

Bulgarian banner must include:

- „Приемам всички“;
- „Отказвам всички“;
- „Настройки“;
- links to privacy policy and cookie policy;
- easy access to change consent later.

Categories:

- Необходими — always active;
- Аналитични — unchecked by default;
- Маркетингови — unchecked by default;
- Външни услуги — unchecked by default.

---

## Consent Mode v2 Requirements

Default EU/EEA state before consent:

| Parameter | Default |
|---|---|
| `analytics_storage` | denied |
| `ad_storage` | denied |
| `ad_user_data` | denied |
| `ad_personalization` | denied |
| `functionality_storage` | as needed / denied unless necessary |
| `security_storage` | granted only if strictly necessary |

QA must include browser devtools, Tag Assistant, GA4 DebugView, consent revoke test, and incognito test.

---

## Form Privacy Notice

Recommended notice around submit area:

> С изпращането на заявката предоставяте данни за контакт и информация за услугата, необходими за обработка на запитването. Ако качите снимки, те ще се използват само за преценка на обема, достъпа и условията за изпълнение. Не качвайте снимки, съдържащи лични документи, банкови данни или чувствителна информация. Заявката не представлява автоматична оферта или автоматична резервация.

---

## Recommendation

Use **CMP + GTM governance** on staging first:

1. CMP plugin/config setup.
2. No external scripts before consent.
3. YouTube placeholder.
4. GA4 only through consent-controlled setup.
5. Meta Pixel disabled until client approval.
6. MGRS storage audit before live.
7. Retention policy to be validated by client/legal reviewer before publication.

---

## Next PM Task

**GDPR-COOKIE-02 — Staging Audit Checklist Execution**

Scope:

- staging only;
- no live changes;
- inspect active scripts and cookies;
- document GA4/GTM/YouTube/Maps/Meta state;
- inspect request-system storage;
- choose CMP/plugin configuration before implementation.

Minimum output:

`GDPR_COOKIE_Staging_Audit_v1.md`
