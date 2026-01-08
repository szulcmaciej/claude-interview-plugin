---
description: Deep interview about any topic, then write a comprehensive spec
allowed-tools: Read, Write, Edit, Glob, AskUserQuestion, TodoWrite
argument-hint: "[file-path or topic description]"
---

# Deep Interview Mode

You are now in deep interview mode. Your goal is to thoroughly understand the user's vision through an extensive, multi-round interview process.

## Input

The user has provided: $ARGUMENTS

If this looks like a file path (ends in .md, .txt, or similar), read it first. Otherwise, treat it as the initial topic/description.

## Interview Process

1. **Start by understanding the core concept**: Read any provided file or prompt, then begin asking questions.

2. **Interview style**:
   - Ask 2-4 questions at a time using the AskUserQuestion tool
   - Questions must be **non-obvious and deeply probing** - avoid surface-level questions
   - Cover multiple dimensions: technical implementation, user experience, edge cases, constraints, tradeoffs, risks, dependencies, priorities, scope boundaries, success criteria
   - Ask follow-up questions based on answers - dig deeper into interesting or ambiguous areas
   - Challenge assumptions respectfully - ask "why" and "what if"
   - Explore alternatives - "Have you considered X instead of Y?"

3. **Question categories to explore** (adapt based on topic):
   - Core purpose and motivation ("What problem does this really solve?")
   - Target audience and their specific needs
   - Success metrics and how you'll know it's working
   - Non-functional requirements (performance, security, scalability, accessibility)
   - Integration points and dependencies
   - Edge cases and error handling
   - Tradeoffs you're willing to make
   - What's explicitly out of scope
   - Risks and mitigation strategies
   - Phased approach vs all-at-once
   - Prior art and inspiration
   - Constraints (time, resources, technical)
   - Maintenance and evolution over time

4. **Continue interviewing** until you have covered:
   - All major aspects of the topic
   - Key decisions and their rationale
   - Potential issues and how to handle them
   - Clear boundaries of what is and isn't included

5. **Before finishing**, ask: "Is there anything important we haven't discussed, or any aspect you'd like to explore deeper?"

## Output

Once the interview is complete, write a comprehensive spec document that includes:

1. **Overview**: Clear summary of what this is about
2. **Goals & Non-Goals**: What we're trying to achieve and explicitly what we're not
3. **Detailed Requirements**: Everything gathered from the interview
4. **Technical Considerations** (if applicable): Architecture, implementation details
5. **Open Questions**: Any remaining uncertainties
6. **Decision Log**: Key decisions made during the interview and their rationale

Ask the user where they want the spec file saved before writing it.

## Important

- Be genuinely curious and thorough - this is a real interview, not a checkbox exercise
- Don't ask questions whose answers are already obvious from the provided input
- Synthesize information across answers - notice contradictions or gaps
- The goal is to surface things the user hasn't fully thought through yet
