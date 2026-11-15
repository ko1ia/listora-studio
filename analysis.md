# Marketplace editor analysis

The starting directory contained no project files or Git repository. The supplied HTML is a saved existing listing edit page at `/merchants/:merchant/store/products/:product/edit`. Its main form is `#edit_product` inside `#product-edit`. It uses `method=post`, `_method=put`, `authenticity_token`, and a native **Update** submit button. The extension must leave this form intact.

## Confirmed controls

The form has direct controls for SKU, version, status, maturity, mesh, permissions, redelivery, usage, avatar compatibility, six localized title/feature/description/keyword groups, price, land impact, video URL, SLurl, and quantity. English fields include `product_en-US_name` and `product_en-US_description`. The snapshot specifies maximum lengths of 120 for titles and 80 for each feature. Inline page data specifies description 5000 and keywords 200.

Category is represented by hidden taxonomy fields and a site chooser. Images use a site uploader, while GIF and PDF use file inputs. Related items, demo items, listing enhancements, and revenue distributions use separate site controls or dialogs. The saved HTML shows these controls but does not prove all associated production JavaScript behavior.

Quick Fill uses the existing `#copy-product-link` trigger and `#copy-product-chooser` modal. Its search form is `#copy-product-search-form` with `related_type=copy-product`; the selected listing is handled by Marketplace's own JavaScript. Studio invokes the trigger and rereads native field values after a result click. The snapshot does not contain the site's JavaScript bundle, so the live modal and copy request still require browser verification.

The saved page also contains `.modal` dialogs for category selection, related and demo items, image upload, distributions, and listing enhancements. Studio applies CSS to these existing dialogs only under `body.ms-page`; it does not move them or replace site JavaScript. The saved HTML verifies selectors and structure, while open/close and asynchronous actions still require live browser verification.

## First stage architecture

`src/content.ts` identifies the edit URL and form, creates a separate Studio UI, and mirrors known controls. `src/studio.css` styles the compact dark UI and widens the page only while Studio is active. `public/manifest.json` limits injection to Marketplace product editor URLs. `scripts/build.mjs` generates an unpacked extension in `dist` by bundling TypeScript and copying the local stylesheet. The native form is hidden only while Studio is active; it is never removed or serialized into a custom network request. The user's Update action invokes the original submit control without switching views.

## Remaining risks

The provided HTML confirms the existing listing form, but does not show a new listing page or prove live submission. The new listing path is detected if it uses `#new_product` inside `#product-edit`; browser verification is needed. Native controls or site handlers can change. If a required control is missing, the Studio simply omits its mirror and the Original view remains available. The snapshot check verifies mounting and text synchronization; it does not exercise live Marketplace requests.
