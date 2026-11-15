# Review, save and publish

[← Description tools](description-tools.md) · [Guide home](README.md) · [Next: Publishing history →](publishing-history.md)

In Bulk Editor, **Review changes** compares each selected product's current Marketplace values with the local draft, including expanded variables and missing required fields. The lower **Publish Selected** button also opens this review; it does not bypass it.

> **Screenshot placeholder:** Review changes panel comparing one demonstration product before and after (`images/review-publishing.png`).

1. Check the selected product list and every proposed field, including names, price, category, permissions, features and Demo Item changes.
2. Resolve warnings. If Marketplace data changed since the draft was loaded, rerun the review instead of forcing an older value over it.
3. Choose **Save Changes** to update products without listing them, or **Publish Selected** to save and request listing.
4. Watch the sequential queue. It processes one product at a time and shows Review, Save, Publish and Verify stages.
5. Read the result for each product. Open Marketplace's **Listed** view or the product page to confirm what is live.

**Stop after current item** stops after the in-progress product. Completed products are not rolled back. **Retry Failed** reviews failed products again; inspect their errors and proposed changes before retrying.

Publication uses Marketplace's current listing form and verifies the product in **Listed**; a successful request alone does not count as published. The request has been exercised with local page fixtures, but a live Marketplace publication response has not been captured in this repository. Start with one noncritical listing and verify it in your own store before a large batch.

**Example:** Save two Luna Dress variants first, inspect them on Marketplace, then publish one and confirm that it appears in Listed before publishing the other.

Need a license? The direct official product link is pending confirmation. See [activation](license-activation.md).
