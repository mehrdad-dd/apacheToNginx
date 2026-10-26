# Provenance, attribution & license review | سابقه کد و حق نشر

**Review date:** 2026-10-26

## Verified Git history

| Point | Evidence |
|---|---|
| Original public repository | [razamoh/apacheToNginx](https://github.com/razamoh/apacheToNginx) |
| Original author attribution | `README.md` identifies `@razamoh`; `converter.sh` contains "Developed by razamoh" |
| Upstream latest commit reviewed | [8eb802d](https://github.com/razamoh/apacheToNginx/commit/8eb802dcf5a5690cb030aa66456382d15cb5e340) — 2024-08-17 |
| Copy / derivative repository | [mehrdad-dd/apacheToNginx](https://github.com/mehrdad-dd/apacheToNginx) |
| Local 2026 commit | [2908e66](https://github.com/mehrdad-dd/apacheToNginx/commit/2908e66ea4bb22258eb83807f486cdc6882a5956) — removed one blank line from `README.md` |
| Conversion script comparison | Both repositories' `converter.sh` blobs were identical at the time of review (blob SHA `baa396b4abd855740bfe2b2c0057a616ab264a9f`) |
| License file comparison | Both repositories' `LICENSE` blobs were identical at the time of review; they contain the GNU GPL version 3 text |
| Contradiction | Historical English README (including original upstream) claimed MIT while `LICENSE` contains GPLv3 |

**Conclusion:** The available Git records do not establish an independent implementation of `converter.sh` by this repository's maintainer. Maintaining a copy, adapting documentation, reviewing code, or later fixing bugs are valid contributions, but none transfers ownership of the original copyrighted work.

**نتیجه:** در شواهد فعلی، نویسندگی مستقل اسکریپت برای صاحب مخزن حاضر تأیید نمی‌شود. نگه‌داری، مستندسازی و اصلاح‌های آینده مشارکت‌اند؛ انتقال حق نشر کد اصلی نیستند.

## Attribution policy

- Preserve the original `converter.sh` author header and the complete upstream commit history.
- Explain current ownership precisely: *repository maintained by @mehrdad-dd; original script authored by @razamoh*.
- Record new code contributions and their dates in Git; do not retroactively claim authorship.
- Preserve the existing `LICENSE` file as-is until the original author or authorized copyright holder clarifies the historical MIT/GPL discrepancy.
- Do not combine this GPLv3-text project into an MIT-only distribution without establishing the necessary rights.
- If a written clarification or relicensing permission is obtained, link it and record the exact scope before changing license claims.

## Suggested request to the original author

> Hello Raza, thank you for publishing apacheToNginx. I maintain a copy at github.com/mehrdad-dd/apacheToNginx and want to credit your original authorship correctly. Your README says MIT, while the LICENSE file contains GPLv3. Could you confirm which license you intended for the converter script and whether you permit the maintained copy under those terms? I will preserve your attribution and link to the upstream project. Thank you.

This suggested note has **not** been sent; the maintainer may contact the original author through an appropriate public project channel.

## Technical caution

The inherited script currently has a Bash syntax issue and does not implement the documented `--dry-run` argument; it should not be described as production-ready. Code hardening and tests are separate future tasks and should identify all modifications.
