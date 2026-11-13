# Repository Guidelines

## Project Structure

This repository indexes public reverse engineering work for the first-generation Sony ZV-E10 (ILCE-ZV-E10). `README.md` is the English index, `README.zh-CN.md` is the Chinese index, and `CONTRIBUTING.md` describes how to suggest or review entries. The repository links to external projects; it does not distribute their code or firmware.

## Adding and Updating Entries

Organize entries under camera firmware and software reverse engineering or software compatibility patches. Include the project link, its concrete work, relevant firmware or software versions, and known limitations. Check the project's source or documentation for a direct connection to the original ZV-E10 and evidence of substantial original work; for forks, identify what was added. Exclude empty projects, pseudo-open-source projects and forks without meaningful changes.

Record available license information and known attribution concerns without assuming that public source grants redistribution rights. Distinguish author-reported results from independently verified findings, and simulator results from hardware tests. Do not claim a project is verified without evidence.

## Documentation and Verification

Keep the English and Chinese indexes consistent when adding, changing or removing entries. Preserve language-switch links, risk notices and applicable version restrictions. Use concise Markdown and keep table rows contiguous: blank lines inside a table break its rendering. Preview both files and check changed links. Run `git diff --check` to catch whitespace errors; there is no build system or automated test suite.

## Commits and Pull Requests

Use short, imperative commit subjects, such as `Add firmware research project`. Keep changes focused. Pull requests should explain the change, link relevant issues or upstream evidence, and state what was checked. Include screenshots only when useful for a rendering change.

## Security and Configuration

Do not commit camera firmware, device backups, keys, credentials or machine-specific configuration. Preserve the README warnings about device damage, warranty and compliance risks.
