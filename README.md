# Apache → Nginx Configuration Converter

**Repository status: upstream-derived, maintained copy — not an original implementation by this repository owner.**

[فارسی](README_FA.md) · [Origin & attribution](PROVENANCE.md) · [License file](LICENSE)

> [!IMPORTANT]
> **Original author:** [Raza Rafaideen (@razamoh)](https://github.com/razamoh), author of the [upstream project](https://github.com/razamoh/apacheToNginx).  
> **This repository's maintainer:** [@mehrdad-dd](https://github.com/mehrdad-dd) — maintains this copy and its documentation. **Repository ownership is not a transfer of copyright.**

## What is this?

A Bash script originally written to assist with converting Apache virtual-host configuration into Nginx configuration. This repository preserves its upstream authorship and history. No independent authorship of `converter.sh` is claimed here.

| Item | Status |
|---|---|
| Original source | [razamoh/apacheToNginx](https://github.com/razamoh/apacheToNginx) |
| Original code author | Raza Rafaideen / `@razamoh` |
| Current repository maintainer | `@mehrdad-dd` |
| Code provenance | `converter.sh` matched the upstream file at the recorded October 2026 review |
| Changes in this repository | The October 14, 2026 commit edited README whitespace only; later documentation changes are tracked in Git |
| License | The included [LICENSE](LICENSE) contains **GNU GPL version 3**; the old README (including upstream) incorrectly said MIT. See below. |

## Safety and current limitations

> [!CAUTION]
> **Do not use this converter on a production server in its current state.** The current script has an unterminated shell quote near `DEFAULT_SSL_KEY_PATH`, its advertised `--dry-run` option is not actually parsed, and its file-handling logic can move/replace Nginx configurations. It has not been validated for safe execution here.

You can inspect the file without executing its conversion logic:

```bash
git clone https://github.com/mehrdad-dd/apacheToNginx.git
cd apacheToNginx
bash -n converter.sh
```

`bash -n` currently reports a syntax problem; the script requires a separate code audit, reliable non-destructive dry-run implementation, and tests before use.

## License clarification

The repository and upstream both contain a `LICENSE` file with the **GNU General Public License, version 3 (GPLv3)** text, while the historical README claimed **MIT**. These statements conflict.

**We have removed the unsupported MIT claim from this README and preserved the GPLv3 license text unchanged.** Until the original rights holder clarifies the discrepancy, do **not** describe this script as MIT-licensed, replace its license, or claim its original code as your own. If you plan to redistribute or relicense it, confirm the appropriate permissions and obligations first.

The included GPLv3 text, if applicable, allows modification and redistribution subject to its obligations, including preserving copyright/license notices and marking changes. This README is not legal advice.

## Credits and contributions

- **Original implementation and upstream history:** [Raza Rafaideen (@razamoh)](https://github.com/razamoh/apacheToNginx).
- **Maintenance and later documentation in this copy:** [@mehrdad-dd](https://github.com/mehrdad-dd).
- **Detailed provenance and outstanding license questions:** [PROVENANCE.md](PROVENANCE.md).

Contributions are welcome once submitted with clear attribution, a summary of the changes, and confirmation that the contributor has rights to provide the material. No one should remove historical credit when preparing a derivative.
