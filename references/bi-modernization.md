# Modernizing an existing BI report

Use this guide when a team redesigns, migrates, or replaces a BI report already in use. A visual-only assignment can end with visual acceptance. If the report will replace an existing asset, include its maintenance workflow in the deliverable.

## Start with the maintainer's next change

Ask the owner to walk through a real change. What do they open or download, where do they edit source queries or measures, and which published item receives the result? Record the owner, required editable artifact, and destination in the task's acceptance criteria. Inspect the current artifact and its connection before choosing an architecture.

| What the owner needs | Delivery and decisive check |
| --- | --- |
| Owns the report and the data transformations in one file | For Power BI, start from the complete source model and queries. If using PBIP to integrate pages, reopen the intended PBIX in Desktop, open a known original Power Query query, inspect its applied steps, and check a known visual. |
| Owns the presentation while another team maintains a shared model | Keep the intended shared-model connection. Check the report against that model and identify its maintainer. |
| Needs to download, edit, and republish an existing service item | Include the intended workspace and item, access to the required download mode, and a check that the downloaded artifact supports the maintenance task. Record any portion still awaiting authorized publication. |

A local composite model over a remote Power BI model can add new modeling capabilities. Its existence alone does not establish that the original Power Query transformations are available in the file.

## Validate one representative page before scaling

1. Map the business question, the important measures, visible and hidden filters, and a navigation path that people use. Pick one page that exercises those behaviors.
2. Review a focused prototype with the owner. A screenshot or interactive mockup can settle layout and interaction choices. Reconcile figures in the actual report against the existing model.
3. Compare the same measure at the same grain and data refresh, with the same period, organization, calculation mode and relevant filter scope. Write down actual values. When results diverge, vary one filter at a time and preserve the explanation with the reference scenario.
4. Extend the approved pattern to the remaining pages. Recheck the interactions or results affected by each change. Reuse earlier acceptance evidence when it still applies.

## Close at the scope the owner requested

Record visual acceptance, numerical reconciliation, maintenance verification, and actual publication separately. For replacement, identify the service item before overwriting it. After authorized publication, verify the existing access route and, when requested, the maintenance download. For user adoption, provide a demonstration or usage guide when the audience needs one, and label illustrative data in demonstrations.

## Learning record

Methodology v0.2.0, 2026-11-25. Source: a completed visual redesign with page-by-page acceptance, a filter-scope discrepancy explained against the legacy model, and a packaging change after the owner demonstrated the usual maintenance routine. The local maintenance check was confirmed. This adds a conditional BI guide to the personal methodology. No earlier rule was superseded.
