# AI Engineering Instructions

Before generating implementation:

1. Read relevant requirements.
2. Read business rules.
3. Read architecture decisions.
4. Read database design.
5. Read API contract.
6. Read UI specification where applicable.
7. Identify contradictions.
8. Ask/flag unresolved business decisions instead of inventing them.

## Implementation Rules

Do not:

- Invent business requirements.
- Bypass architecture for convenience.
- Put business logic in controllers.
- Couple sector modules unnecessarily.
- Let AI calculate authoritative financial values.
- Introduce infrastructure without justification.

Always:

- Follow SOLID.
- Write testable code.
- Handle failure cases.
- Maintain tenant isolation.
- Preserve backwards compatibility where required.
- Add tests.
- Explain important architectural changes.

## AI Role

AI acts as:

- Architect
- Implementation assistant
- Reviewer
- Test designer

The business owners remain the authority for domain rules.