# 07 Open questions

Decisions the owner has not made yet. When one is answered, update `brand-guidelines.html` first if it affects the guidelines, then the ai-docs, then log it in 06 and remove it here.

## From the guidelines vs later decisions (see 01)

Decided 10 October 2026 and removed from this list: "Built for Progress" (campaign line), the reka.re surface (light-first), the method (SEE → PROVE → BUILD → ADVANCE). See 06.

1. **OVERride and Motion.** Is OVERride (Kinetik's autonomous vehicle and fleet platform) the same as AntaraX Motion, the research platform behind it, or a separate product?
2. **AntaraX colour in REKA materials.** Keep Heuristik blue `#1268F7` for the division and AntaraX blue `#0459F7` for AntaraX surfaces, or converge on one? Same question for PLExyz (purple vs Edge green) and Tinara (maroon vs Tide pink).
3. **Product subdomains.** The dashboard system names plexyz / override / antarax / tinara `.reka.re`, console.reka.re and app.reka.re. Which of these are real or planned, given AntaraX products live on antarax.ai?
4. **Frost & Sullivan.** "Best Crowd Analytics award" (guidelines) or "recognised" (9 October instruction)?
5. **Autoware.** Confirm "member" (the guidelines' hard rule) and remove "regional representative" from the guidelines page.
8. **REKA-hosted AntaraX pages:** decided 10 October for reka.re (AntaraX mark and family colours on REKA's light surface with chamfer). Still open: whether the guidelines should record this as the rule for every REKA-hosted AntaraX page.
9. **Update the guidelines** (`brand-guidelines.html` and its ai-docs) with the October portfolio: AntaraX as the product line, its six families, PLExyz and Tinara under AntaraX, Yara, Janka, Angka and Motion added.

## Carried over

11. **Navigation** for the multi-page reka.re.
12. **Seth on light grounds:** is the small batik cameo in AntaraX illustrations exempt from the dark-only rule?
13. **History facts** marked "to confirm" in 02.
14. **Blog:** confirm reka.re/blog.
15. **Orange inside AntaraX products** (Frame uses `#FB9800`): allowed, or reserved for REKA?
16. **Managed AI pricing:** published starting point, or quoted per engagement?

## From other repositories

17. **Status, container and dark tokens for REKA's look** (asked by RESAM, 13 November 2026, its backlog B-33). RESAM's
    kickoff kit dresses REKA's own documents and client prototypes in REKA's look (`tools/kickoff/DESIGN.md` in RESAM).
    Its 25 brand colours now come from this kit's `tokens/tokens.json` 1.0.0 and are checked against it. These 20 roles,
    each with a light and a dark value, have no token here, so RESAM keeps them by hand. Should this kit own them? If
    yes, add them to the guidelines first, then `tokens/`, and RESAM takes them with its sync script. The diagram colours
    (the kinds of node and the blueprint plate) are not asked for: RESAM's drawing standard owns those.

    | Role | Light (RESAM today) | Dark (RESAM today) |
    |---|---|---|
    | `error` / `error-container` / `on-error-container` | `#B42318` / `#FEECEB` / `#B42318` | `#F7867C` / `#2E1312` / `#F7867C` |
    | `success` / `success-container` / `on-success-container` | `#067647` / `#E7F8EF` / `#067647` | `#5FD49A` / `#10291C` / `#5FD49A` |
    | `warning` / `warning-container` / `on-warning-container` | `#B54708` / `#FEF4E6` / `#93370D` | `#F7B15A` / `#2B1D0A` / `#F7B15A` |
    | `secondary-container` / `on-secondary-container` (the orange tint and its text) | `#FFF1DC` / `#6B3F00` | `#2A1E0B` / `#FFC46B` |
    | `key-container` (the key path's tint) | `#FFF1DC` | `#2A1E0B` |
    | `primary-container` | `#EFEDE8` | (from this kit: `internal.surface-2`) |
    | `surface-container-low` / `-container` / `-high` / `-highest` | `#FBFAF8` / `#F2F0EB` / `#EFEDE8` / `#E4E1D9` | `#131315` / `#1D1D20` / `#232327` / `#2C2C31` |
    | `on-surface-variant` (secondary text) | `#4A4A50` | `#B4B4B0` |
    | `outline` / `outline-variant` | `#8A8A90` / `#DCD9D1` | `#6A6A70` / `#2C2C31` |

    Recommended: yes for the status set and the dark surfaces, since every REKA surface that shows a state needs them;
    take the values above as the starting point, checked for contrast in the guidelines. Note that the orange tint here
    (`#FFF1DC`) is close to, but not, this kit's `--orange-bg` `#FFF2DF`: one of the two should give way.
