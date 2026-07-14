# Yura — Codex Animated Pet

<p align="center">
  <img src="screenshots/yura-idle.png" alt="Yura idle pose" width="160">
</p>

Yura is a mysterious moonlit chibi girl with violet-gray eyes, a long blue-black braid tied with plum ribbons, and a deep indigo kimono. Her ivory collar, moon-gold obi, crescent and cloud motifs, white tabi, and dark geta keep the traditional silhouette readable at pet size. She is packaged as a Codex sprite v2 pet with nine standard animation states and sixteen clockwise look directions.

유라는 보랏빛 회색 눈과 자두색 리본으로 묶은 긴 청흑색 땋은 머리, 짙은 남색 기모노가 특징인 달빛 아래의 신비로운 치비 캐릭터입니다. 아이보리색 깃과 달빛 금색 오비, 초승달·구름 문양, 흰 버선과 짙은 게타를 사용해 작은 펫 크기에서도 전통적인 실루엣이 잘 보입니다. Codex sprite v2 규격의 아홉 가지 기본 애니메이션과 열여섯 방향 시선을 지원합니다.

## Highlights

- Codex sprite contract: v2
- Atlas: `1536 × 2288` WebP with transparency
- Cell size: `192 × 208`
- Layout: 8 columns × 11 rows
- Standard states: idle, drag right, drag left, wave, jump, failed, waiting, working, review
- Look loop: 16 directions in 22.5-degree steps
- Public QA: atlas validation, three-reviewer blind direction validation, and independent final visual QA

## Animation previews

| Idle | Drag right | Drag left |
| --- | --- | --- |
| ![Idle](previews/idle.gif) | ![Drag right](previews/running-right.gif) | ![Drag left](previews/running-left.gif) |

| Wave | Jump | Failed |
| --- | --- | --- |
| ![Wave](previews/waving.gif) | ![Jump](previews/jumping.gif) | ![Failed](previews/failed.gif) |

| Waiting for input | Working | Review |
| --- | --- | --- |
| ![Waiting](previews/waiting.gif) | ![Working](previews/running.gif) | ![Review](previews/review.gif) |

## Full sprite and look-direction previews

<details>
<summary>Open the complete 8 × 11 animation sheet</summary>

![Yura animation sheet](screenshots/animation-sheet.png)

</details>

<details>
<summary>Open the neutral + 16-direction QA sheet</summary>

![Yura look directions](screenshots/look-directions.png)

</details>

## Install

From the repository root on macOS or Linux:

```bash
mkdir -p "$HOME/.codex/pets/yura"
cp "Yura/pet.json" "$HOME/.codex/pets/yura/pet.json"
cp "Yura/spritesheet.webp" "$HOME/.codex/pets/yura/spritesheet.webp"
```

Restart or refresh the Codex desktop app if Yura does not appear immediately.

To uninstall:

```bash
rm -rf "$HOME/.codex/pets/yura"
```

## Required package files

Only these files are required by Codex:

```text
Yura/
├── pet.json
└── spritesheet.webp
```

The `previews`, `screenshots`, and `qa` folders are documentation and verification artifacts for repository visitors.

## Verification

The published package passed the following checks:

- `spriteVersionNumber: 2`
- WebP RGBA, `1536 × 2288`
- 8 columns × 11 rows
- Transparent RGB residue: 0 pixels
- Atlas errors and warnings: none
- All blind direction pairs passed with no warning or unconfirmed result
- All sixteen labeled look directions passed independent final visual review
- Continuity metric warnings were accepted after the ordered loop showed no visible snap, clipping, scale pop, identity break, or braid detachment
- Published package and key screenshot checksums are listed in [`SHA256SUMS`](SHA256SUMS)

See [`qa/validation.json`](qa/validation.json), [`qa/direction-blind-validation.json`](qa/direction-blind-validation.json), and [`qa/final-visual-qa.json`](qa/final-visual-qa.json) for the public QA summaries.

## License

The package uses two licenses:

- `pet.json`, this README, `SHA256SUMS`, and files in `qa/` are available under the [MIT License](../LICENSES/MIT.txt).
- `spritesheet.webp`, images in `screenshots/`, and animations in `previews/` are available under [CC BY 4.0](../LICENSES/CC-BY-4.0.md).

When sharing or adapting Yura's visual assets, use this attribution where practical:

> Yura Codex Pet by Ryu JaeHyun, licensed under CC BY 4.0.

See the repository's [license overview](../LICENSE.md) for details.
