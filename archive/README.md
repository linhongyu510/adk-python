# Issue 6945 — independent fix (superseded by upstream 8e30a308)

Context cache application could empty `llm_request.contents`, which the
API rejects. This independent fix skips cache application when it would
leave no live contents. Upstream fixed the same bug differently in
8e30a308 (always retain the final content). Archived for reproducibility
before local cleanup; not merged.
