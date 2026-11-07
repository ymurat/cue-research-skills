# Sources and Licenses

This collection contains nine separate skill adaptations. Each component keeps its own source attribution and license. There is no umbrella license for the collection; a component's license does not automatically apply to other folders.

| Skill or component | Upstream source | License retained here |
|---|---|---|
| `academic-research` | [Academic Research Agent Skill, commit `7be432270686246efd14573426c2ab065e88ccb5`](https://github.com/ngtiendong/Academic-Research-Agent-Skill/tree/7be432270686246efd14573426c2ab065e88ccb5) | MIT, in `skills/academic-research/LICENSE` |
| `book-consistency` | [Novel Hint continuity-check, commit `d4aa27a5e52d2ebc1565b2416627082667639db6`](https://github.com/chianglianglin/novel-hint/tree/d4aa27a5e52d2ebc1565b2416627082667639db6/skills/continuity-check) | MIT, in `skills/book-consistency/LICENSE` |
| `citation-management` | [Scientific Agent Skills citation-management, commit `a92663a0214b3b9fa1ba6b958284ffd919c00a0c`](https://github.com/K-Dense-AI/scientific-agent-skills/tree/a92663a0214b3b9fa1ba6b958284ffd919c00a0c/skills/citation-management) | MIT, in `skills/citation-management/LICENSE.md` |
| `talk-prep` | [Paper-to-Podium, commit `8cb3bf579c2214f215a9336df519e74821a874ac`](https://github.com/mimaowang/paper-to-podium/tree/8cb3bf579c2214f215a9336df519e74821a874ac) | MIT, in `skills/talk-prep/LICENSE-paper-to-podium` |
| `zotero-library-cue` | [Scientific Agent Skills `pyzotero`, commit `a92663a0214b3b9fa1ba6b958284ffd919c00a0c`](https://github.com/K-Dense-AI/scientific-agent-skills/tree/a92663a0214b3b9fa1ba6b958284ffd919c00a0c/skills/pyzotero) | MIT, in `skills/zotero-library-cue/LICENSE` |
| `deepread` | [DeepRead, `research/deepread/SKILL.md`, pinned for comparison at commit `3aa22f1c9f547e37c585f3e13cb33f231a960fef`](https://github.com/alirezarezvani/claude-skills/tree/3aa22f1c9f547e37c585f3e13cb33f231a960fef/research/deepread/SKILL.md) | MIT, in `skills/deepread/LICENSE` |
| `agent-harness-cue` | [ECC `skills/agent-harness-construction/SKILL.md`, commit `b38be6a7f6350964d59328b52f0624e1d1d552d1`](https://github.com/affaan-m/ECC/blob/b38be6a7f6350964d59328b52f0624e1d1d552d1/skills/agent-harness-construction/SKILL.md) | MIT, in `skills/agent-harness-cue/LICENSE` |
| `agent-eval-cue` | [ECC `skills/agent-eval/SKILL.md`, commit `b38be6a7f6350964d59328b52f0624e1d1d552d1`](https://github.com/affaan-m/ECC/blob/b38be6a7f6350964d59328b52f0624e1d1d552d1/skills/agent-eval/SKILL.md) | MIT, in `skills/agent-eval-cue/LICENSE` |
| `empirical-se-standards-cue` | [Murat Yılmaz's `empirical-se-standards` skill](https://github.com/ymurat/academic-agent-skills/tree/main/skills/empirical-se-standards); [ACM SIGSOFT Empirical Standards](https://github.com/acmsigsoft/EmpiricalStandards) checklist | MIT for the skill, in `skills/empirical-se-standards-cue/LICENSE`; the bundled checklist is separately CC0-1.0, with legal text in `skills/empirical-se-standards-cue/references/CC0-1.0.txt` |
| `talk-prep` bundled SimplePlus theme | [SimplePlus Beamer Theme, commit `d4134a7659515d1842e599b33aa84a82e39197d2`](https://github.com/pm25/SimplePlus-BeamerTheme/tree/d4134a7659515d1842e599b33aa84a82e39197d2) | Unlicense, in `skills/talk-prep/assets/simpleplus/LICENSE`; source details in the accompanying `NOTICE.md` |

## Attribution notes

- Keep the applicable copyright and permission notices when copying or redistributing each component.
- Each skill's `ATTRIBUTION.md` identifies its source and adaptation. Upstream authors and projects are not presented as endorsing this collection.
- `agent-harness-cue` and `agent-eval-cue` are independent Cue rewrites of the pinned ECC skill files, not official upstream releases. `agent-eval-cue` adapts ECC's method only; it does not include or require the separate `joaquinhuigomez/agent-eval` CLI or code.
- The Academic Research Agent source recommends citing its repository in academic work. The Scientific Agent Skills source asks users to cite its paper when the skill makes a meaningful contribution to a paper, report, presentation, or code release, and to inform the user. These are source-specific academic-use recommendations or instructions, separate from the MIT redistribution notice.
- The SimplePlus theme's license and `NOTICE.md` apply to its bundled files, not to the other skills.
- The DeepRead commit is a pinned upstream comparison snapshot, not verified provenance for the supplied ZIP: the ZIP metadata does not record which upstream commit the included `SKILL.md` came from. See `skills/deepread/ATTRIBUTION.md`.

Check the relevant `LICENSE`, `ATTRIBUTION.md`, and `NOTICE.md` before reuse. This summary is informational and does not replace the license text.
