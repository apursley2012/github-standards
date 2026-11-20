# Shared GitHub standards

Create a public repository named github-standards. Upload the contents of the
github-standards folder, including its hidden .github folder. Create a tag v1.
Copy examples/auto-format.yml into each target repository at
.github/workflows/format.yml. Optionally add examples/format-check.yml at
.github/workflows/format-check.yml and require that check before merging.

Use the Actions tab to run Code formatting manually. Bot pushes require branch
write access. Protected branches may reject pushes. Bot commits normally do
not trigger push workflows; run builds manually or integrate checks into the
same workflow. Review changes on a test branch before enabling automatic writes.

This starter formats HTML, CSS, JS, TS, JSON, YAML and Markdown. Java, XML,
Python and other languages need separate formatters. Recognized boxed headers
are restored exactly; unrecognized protected headers are skipped. Existing
width errors are reported but not repaired. Legal notices, dependency lock
files, binary assets and common generated directories are excluded.

The formatter version is fixed; action commit SHAs must be verified against
official repositories before use. Replace @v1 with the central repository's
verified full commit SHA for stronger supply-chain protection. This starter
does not install security scanners or language-specific formatters.
