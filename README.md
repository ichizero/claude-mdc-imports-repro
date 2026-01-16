# claude-md-imports-repro

A repository to reproduce an issue where `@` file imports in CLAUDE.md are not working properly.

## Structure

```
.
├── CLAUDE.md                    # Config file with @import
└── docs/
    └── sample-instructions.md   # Sample file to be imported
```

## How to Reproduce

1. Start Claude Code in this repository
2. Run `/context` command to check if `@docs/sample-instructions.md` is imported in the memory files

## Result

### v2.1.1

```bash
     Memory files · /memory
     └ ~/.claude/CLAUDE.md: 45 tokens
     └ CLAUDE.md: 69 tokens
     └ docs/sample-instructions.md: 48 tokens
     └ .cursor/rules/sample-cursor-instructions.mdc: 50 tokens
```

### v2.1.2

```bash
     Memory files · /memory
     └ ~/.claude/CLAUDE.md: 45 tokens
     └ CLAUDE.md: 69 tokens
     └ docs/sample-instructions.md: 48 tokens
```

### v2.1.9

```bash
                                                                                            Memory files · /memory
                                                                                            └ ~/.claude/CLAUDE.md: 45 tokens
                                                                                            └ CLAUDE.md: 69 tokens
                                                                                            └ docs/sample-instructions.md: 48 tokens
```
