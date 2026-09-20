# BËTR maintained OpenViking distribution

This fork carries the reviewed Claude Code final-answer capture correction from upstream PR [5209](https://github.com/volcengine/OpenViking/pull/5209). Plugin source is pinned to commit `118529344f21e8281114dbaad62b347b302c9f3a`, based on upstream `a55afb001bca201f09830b90dc2f64eed20cb799`. The root marketplace points to that exact fork commit using the standard Claude Code git-subdir source. It retains the upstream plugin name and version; identify this distribution by repository and commit, not version alone.

Install through Claude Code's native plugin marketplace using a commit-pinned URL to this catalog. Preserve the existing OpenViking client configuration and credentials. Replace the existing marketplace registration rather than loading two copies of the same plugin. No shell wrapper, new memory store, custom indexer, or server replacement is required.

The source correction reads the final answer supplied by Claude Code's Stop event when the transcript has not flushed it yet, preserving native session capture and duplicate suppression. Proof authored the automated regression coverage and an independent auditor reviewed the recorded before/after behavior. Twelve hook checks passed; real installed capture and fresh-session recall must still be qualified after installation.

The initial fork main was one upstream commit behind the plugin's already-selected baseline. The merged upstream Git-watch authentication correction is source history only for this plugin release; no OpenViking server deployment is part of this change. Do not infer server or repository-watch qualification from plugin installation.

Keep local changes bounded and separately review upstream updates. When an official release contains the equivalent correction and passes the same live capture/recall qualification, return the marketplace to the official distribution and retire this local delta. Application source and business context continue to use the same shared OpenViking service.
