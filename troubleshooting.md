# Troubleshooting

[← Tips and workflows](tips-and-workflows.md) · [Guide home](README.md) · [Next: FAQ →](faq.md)

## Studio does not appear

Confirm the extension is enabled at `chrome://extensions`, the popup says **active**, and its enabled switch is on. Reload the Marketplace tab. Studio appears on seller product edit pages; Bulk Editor appears on **Manage Listings** under `/merchants/.../store/products`. It does not appear on the Marketplace home page.

## Chrome cannot load the extension

**Load unpacked** needs the folder containing `manifest.json`. A source archive needs a successful `npm run build` first; choose `dist` afterward. See [installation](installation.md).

## License activation fails

Check the key for typing mistakes and confirm internet access. **This license key was not accepted** means the licensing service rejected it. **The license server is unreachable** means the connection or service failed; retry later. If rejection persists, contact the product seller. Do not post a key in a public issue. The direct official product and renewal links are pending confirmation.

## Translation is unavailable or incomplete

Translation requires the browser's built-in Translator capability. If Studio reports it unavailable, fill language fields manually. If only some fields translated, inspect the progress and warnings: language pack downloads, translation failures or field-length limits can leave fields unchanged. See [Languages and translation](languages-translation.md).

## Changes were not saved

In Studio, click **Update listing**. In Bulk Editor, finish **Review changes** and confirm **Save Changes** or **Publish Selected**. Read Marketplace errors in **Original** if needed. If the underlying listing changed after review, rerun the review before saving.

## A product did not publish

Read its queue status, correct required fields, then check the product directly on Marketplace. **Retry Failed** reruns failed products after review. Verify a one-item publication before trying a large batch. See [Review and publishing](review-publishing.md).

## Image upload failed

Check file type, size and dimensions in [Image tools](image-tools.md). Inspect the intended product and queue in [Bulk Image Editor](bulk-image-editor.md). Check Marketplace's uploader response; a prepared or queued image is not proof of upload. Switch to **Original** for the site's uploader if the Studio handoff fails.

## Templates or history disappeared

Check that you use the same Chrome profile and merchant account. These records live in extension storage and can disappear when that storage is cleared or the extension is removed. History keeps the latest record per product. See [Publishing history](publishing-history.md).

## Data and support

The extension uses your signed-in Marketplace session for product operations. Licensing sends the key or license token and installation ID to `marketplace-studio.didyacool.workers.dev`. Templates, variable sets and publishing history live locally in Chrome. The extension does not ask for your Second Life password.

For support, share the extension version, Marketplace page type and exact error text. Keep license keys, tokens and private store data out of public reports.

Need a license? The direct official product link is pending confirmation. See [activation](license-activation.md).
