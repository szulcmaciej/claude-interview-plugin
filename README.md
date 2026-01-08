# Claude Interview Plugin

A Claude Code plugin that conducts deep, thorough interviews about any topic and generates comprehensive spec documents.

## Installation

### Quick install (local)

```bash
git clone https://github.com/YOUR_USERNAME/claude-interview-plugin.git
claude --plugin-dir ./claude-interview-plugin
```

### From marketplace (once published)

```bash
claude plugin install interview@marketplace-name
```

## Usage

```bash
# With a file
/interview:interview @SPEC.md

# With a topic description
/interview:interview A mobile app for tracking personal habits

# With a detailed prompt
/interview:interview I want to build a CLI tool that manages dotfiles
```

## What it does

1. Reads any provided file or uses your description as the starting point
2. Conducts a deep, multi-round interview (2-4 questions at a time)
3. Asks non-obvious, probing questions across dimensions like:
   - Core purpose and motivation
   - Target audience and success metrics
   - Technical tradeoffs and constraints
   - Edge cases and error handling
   - Scope boundaries and risks
4. Continues until thorough coverage is achieved
5. Asks where to save the output
6. Writes a comprehensive spec document with:
   - Overview
   - Goals & Non-Goals
   - Detailed Requirements
   - Technical Considerations
   - Open Questions
   - Decision Log

## License

MIT
