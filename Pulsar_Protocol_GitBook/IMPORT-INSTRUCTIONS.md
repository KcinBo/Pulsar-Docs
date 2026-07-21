# Importing these docs into GitBook

This folder is a complete GitBook repository. Every documentation topic is a separate Markdown file under `docs/`, while `SUMMARY.md` controls the page order and nesting.

## Recommended: Git Sync

1. Extract the ZIP.
2. Upload the **contents of the extracted `Pulsar_Protocol_GitBook` folder** to the root of a GitHub or GitLab repository. Do not upload only one Markdown file.
3. In GitBook, create or open a space and connect that repository through Git Sync.
4. Select the branch containing these files. GitBook should read `.gitbook.yaml`, use `README.md` as the landing page, and build navigation from `SUMMARY.md`.
5. Confirm that the page tree contains the separate Start here, Use the protocol, Treasury and alignment, Understand the system, and Reference groups.

## Images

The image files are included inside `.gitbook/assets/`. Markdown pages link to them with repository-relative paths. Keep this folder in the repository and preserve its name. GitBook will upload and render the assets through Git Sync.

If you copy a page manually into another GitBook space, you must also upload the image it references or replace that image path. The complete ZIP avoids that problem.

## Before publishing

- Replace all contract placeholders only after deployments are verified.
- Confirm token symbols, epoch timing, mint terms, reward sources, and distribution policy against the deployed contracts.
- Add audit links and official social links when available.
- Obtain appropriate legal and regulatory review.

