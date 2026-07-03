# Technical State

## Architecture Summary

- Platform: WordPress site with custom plugin.
- Plugin: `mindgrid-request-system`
- Shortcode: `[mindgrid_request_flow]`
- CPT: `mgrs_request`
- Admin menu: `MindGrid Requests`
- Submission path: standard POST through `admin-post.php`
- Current pricing state: demo-only indicative estimate, not final pricing.

## Current Plugin Capabilities

- Admin CPT foundation exists.
- Request entity/admin detail foundation exists.
- Frontend five-step request flow exists.
- Real backend submission exists.
- Bulgarian Mestimvsichko field set exists.
- Live estimate panel exists.
- Review screen estimate card exists.
- Server-side estimate recalculation exists.
- Estimate is saved only in submission summary.

## Current Demo Flow

1. Каква услуга ви трябва?
2. Адрес и достъп
3. Какво трябва да се премести?
4. Допълнителни услуги
5. Контакт и удобен момент

## Explicit Non-Capabilities

- No payment integration.
- No Stripe/payment buttons.
- No real calendar/booking engine.
- No Google Maps production integration.
- No AI integration.
- No external APIs.
- No real automatic final offer.
- No full WordPress site GitHub migration at this stage.

## Environment Status

- Staging demo page: `https://staging.mestimvsichko.bg/podrobna-zayavka/`
- Demo status: GO for client discussion.
- Production/live status: HOLD.

## Technical Risks

- Client may expect calendar/payment based on demo discussion.
- Demo estimate can be misunderstood as final price if disclaimers are not repeated.
- Changing the stable demo before meeting can create avoidable regression risk.
- Translation/i18n implementation can affect SEO, slugs, menus, forms, and layout.

## QA Status

- Latest known RC: `v0.6.0-rc.1`
- Known result: demo estimate preview and live estimate panel accepted for client discussion.
- Next QA need: after any new PM-approved change.
