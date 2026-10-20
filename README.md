# Mimir

A coding skill that agrees on the result before building the smallest complete
solution. Replies use concise, complete sentences informed by ASD-STE100.

## How it works

1. **Understand.** Inspect the code, check assumptions, and ask one question at
   a time about decisions that affect the result.
2. **Agree.** Define the scope and acceptance checks. Wait for approval before
   changing code.
3. **Build.** Reuse existing code, keep changes focused, and complete all affected
   parts.
4. **Verify.** Check the agreed result and report any material limits.

Clear writing applies throughout. Mimir uses short sentences and consistent
terms. It does not claim formal ASD-STE100 compliance.

## Install in Codex

On another laptop, clone this repository into your personal skills folder:

```sh
mkdir -p ~/.agents/skills
git clone https://github.com/kyrylolvov/mimir.git ~/.agents/skills/mimir
```

This command is for a new installation. If the destination already contains a
manually installed skill, move that folder elsewhere before cloning.

If the skill does not appear, restart Codex.

## Use

In Codex, include `$mimir` in your prompt:

```text
$mimir Help me fix the login error.
```

Mimir stays active for that conversation. Say `stop mimir` or `normal mode` to
stop. Each new coding task needs its own scope agreement; an approved task does
not need repeated approval.

## Update

For an installation cloned from this repository:

```sh
git -C ~/.agents/skills/mimir pull --ff-only
```

## Files

```text
mimir/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── README.md
```

`SKILL.md` contains the complete workflow. `agents/openai.yaml` sets the display
name to **Mimir** in supported interfaces. The invocation name remains `$mimir`.
No other skills are required.

## Sources

Mimir combines ideas from these sources into one workflow:

- [Grilling](https://github.com/mattpocock/skills/blob/main/skills/productivity/grilling/SKILL.md): clarify decisions and challenge assumptions.
- [Ponytail](https://github.com/DietrichGebert/ponytail/blob/main/skills/ponytail/SKILL.md): make the smallest complete change.
- [Karpathy guidelines](https://github.com/multica-ai/andrej-karpathy-skills/blob/main/CLAUDE.md): state assumptions, limit edits, and verify success.
- [ASD-STE100](https://www.asd-ste100.org/about.html): principles for clear technical English.
