# lovelyskills

AI 코딩 에이전트 워크플로우에서 쓰는 재사용 가능한 스킬 모음입니다.

## Quickstart

```bash
npx skills@latest add lovelyuk/lovelyskills
```

설치 화면에서 원하는 스킬을 선택하고, 사용할 에이전트를 고르면 됩니다.

특정 스킬을 바로 설치하려면:

```bash
# Claude Code 전역 설치 예시
npx skills@latest add lovelyuk/lovelyskills --skill lovelythink --agent claude-code --global --yes
npx skills@latest add lovelyuk/lovelyskills --skill grill-me --agent claude-code --global --yes
```

## Skills

| Skill | 설명 |
| --- | --- |
| [`lovelythink`](./skills/lovelythink/SKILL.md) | 모호한 요청을 소크라테스식 인터뷰로 명확한 요구사항 문서로 정리한다 |
| [`grill-me`](./skills/grill-me/SKILL.md) | 플랜이나 설계를 끊임없는 질문으로 검증해 공유된 이해에 도달한다 |

## Repository Structure

```
.
├── skills/
│   ├── lovelythink/
│   │   └── SKILL.md
│   └── grill-me/
│       └── SKILL.md
├── plugin.json
└── README.md
```

## License

MIT
