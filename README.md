# lovelythink Skills

AI 코딩 에이전트 워크플로우에서 쓰는 재사용 가능한 스킬 모음입니다.

## Quickstart

```bash
npx skills@latest add lovelyuk/lovelyskills
```

설치 화면에서 `lovelythink`를 선택하고, 사용할 에이전트를 고르면 됩니다.

특정 에이전트에 바로 설치하려면:

```bash
# Claude Code 전역 설치
npx skills@latest add lovelyuk/lovelyskills --skill lovelythink --agent claude-code --global --yes

# Codex 전역 설치
npx skills@latest add lovelyuk/lovelyskills --skill lovelythink --agent codex --global --yes
```

## Skills

| Skill | 설명 |
| --- | --- |
| [`lovelythink`](./lovelythink/SKILL.md) | 모호한 요청을 소크라테스식 인터뷰로 명확한 요구사항 문서로 정리한다 |

## Why This Exists

AI 코딩 에이전트의 결과물 차이는 모델 성능보다 요구사항을 얼마나 명확히 정의했는지에서 갈립니다.

`lovelythink`는 AI에게 바로 실행을 맡기기 전에, AI가 먼저 사용자를 인터뷰해서 목표·범위·제약·완료 기준을 명확하게 만듭니다.

인터뷰가 끝나면 Claude나 다른 AI에게 바로 넘길 수 있는 **마크다운 요구사항 문서**를 출력합니다.

## Manual Install

### Claude Code

```bash
# 전역 설치
mkdir -p ~/.claude/skills
cp -R lovelythink ~/.claude/skills/lovelythink

# 프로젝트 설치
mkdir -p .claude/skills
cp -R lovelythink .claude/skills/lovelythink
```

### Codex

```bash
# 전역 설치
mkdir -p ~/.agents/skills
cp -R lovelythink ~/.agents/skills/lovelythink

# 프로젝트 설치
mkdir -p .agents/skills
cp -R lovelythink .agents/skills/lovelythink
```

## Repository Structure

```
.
├── .agents/plugins/marketplace.json   # Codex plugin marketplace metadata
├── .claude-plugin/plugin.json         # Claude Code plugin metadata
├── .codex-plugin/plugin.json          # Codex plugin manifest
└── lovelythink/SKILL.md               # Skill source
```

## License

MIT
