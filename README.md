# soojaechun-skills

어느 프로젝트에서나 쓰는 Claude Code 스킬 모음입니다.

| 명령 | 하는 일 |
| --- | --- |
| `/sjc-skills:3w <지시>` | 이 서비스를 쓰는 소비자 기준으로 누가·무엇을·왜를 먼저 보여 주고 지시를 이행합니다 |
| `/sjc-skills:tetris <대상>` | 이미 있는 것 중 정리·정렬·재배치가 필요한 곳을 찾아 보고합니다. 파일은 바꾸지 않습니다 |

두 명령 모두 직접 칠 때만 동작합니다. 에이전트가 스스로 부르지 않습니다.

## 설치

Claude Code 2.1.292 이상에서 터미널에 한 줄을 입력합니다.

```bash
claude plugin install sjc-skills --marketplace soojaechun/soojaechun-skills
```

터미널, 데스크톱 앱, VS Code 중 어디서 설치해도 세 곳 모두에서 보입니다. 설치한 뒤 새 세션을 열면 `/sjc-skills:`로 시작하는 명령이 나옵니다.

## 업데이트

```bash
claude plugin update sjc-skills@soojaechun-skills
```

터미널 세션의 `/plugin` → **Marketplaces** → `soojaechun-skills` → **Enable auto-update**를 한 번 켜 두면 세션을 시작할 때 알아서 받습니다.

## 플러그인 없이 쓰기

`plugins/sjc-skills/skills/` 안의 `3w`, `tetris` 폴더를 `~/.claude/skills/`에 복사하면 `/3w`, `/tetris`로 씁니다. 이 방법은 업데이트할 때 다시 복사해야 합니다.

## 참고

- tetris가 실행 중에 파일을 바꾸지 못하게 막는 설정(`disallowed-tools`)은 Claude Code에서만 동작합니다.
- 스킬 원문은 `plugins/sjc-skills/skills/<이름>/SKILL.md`에 있습니다.
