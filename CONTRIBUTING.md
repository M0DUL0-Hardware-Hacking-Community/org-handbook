# Contributing to M0DUL0

Thank you for helping build a serious, hands-on hardware security community in Malaysia.

## Contribution Scope

Contributions should support:

- Hardware security education and methodology
- Reproducible PoCs, research writeups, and hardware modification projects
- Curated learning resources: materials, datasheets, research papers, and tool references
- Community safety and documentation quality

## Before You Submit

1. Read [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
2. Read [DISCLAIMER.md](DISCLAIMER.md).
3. Ensure your content is lawful, educational, and based on devices you own or are authorised to test.
4. Redact personal data, credentials, and device identifiers from all artefacts.

## What You Can Contribute

- Writeups and white papers from personal research, hardware modification projects, or CTF hardware challenges.
- Tool references and datasheet links with notes on ethical and lawful usage.
- Improvements to existing documentation and onboarding guides.
- PoC demonstrations with responsible disclosure completed where a vendor product is involved.
- Hardware modification documentation, including build notes and project writeups.
- Resource recommendations: datasheets, research papers, conference talks, learning materials.

## Submission Standards

All submissions should include:

- **Purpose**: what this contribution teaches or solves.
- **Context**: who it helps (newcomers, intermediate practitioners, researchers).
- **Verification**: how findings were tested and reproduced.
- **Risk Check**: potential misuse considerations and any mitigations applied.

### Example 1 (Writeup)

```text
Purpose: Document a UART root shell extraction on a consumer router for educational use.
Context: Helps newcomers understand UART identification, baud rate detection, and console interaction.
Verification: Tested on a personally owned device. Steps reproduced independently.
Risk Check: Device model and firmware version disclosed. No credentials or personal data included. Vendor no longer supports this firmware version.
```

### Example 2 (Resource Addition)

```text
Purpose: Add a reference to a datasheet collection for common JTAG-accessible microcontrollers.
Context: Reduces time newcomers spend hunting datasheets when starting board-level research.
Verification: Links checked against official manufacturer sources. No paywalled or pirated material.
Risk Check: Educational reference only. No exploitation guidance included.
```

## Writeup Structure

When contributing a writeup or research note, structure it so it works for newcomers and veterans alike:

- **Theory**: background and conceptual explanation.
- **Cheat Sheet**: quick-reference summary of commands or key facts.
- **Usage**: practical steps, examples, or walkthrough.
- **Resources**: references, tools, and further reading.

Write clearly first, technically second. If you're building on someone else's research, credit them in the Resources section. Only use your own screenshots and diagrams.

## Submitting Changes

1. Fork this repository.
2. Make your changes in a branch on your fork.
3. Open a Pull Request against `main` when ready.
4. A maintainer will review and merge. Expect some back-and-forth on larger writeups.

## Prohibited Contributions

Do not submit content that:

- Demonstrates attacks on devices you don't own or aren't authorised to test.
- Includes firmware dumps, credentials, or personal data from a third party's device.
- Enables attacks on unpatched, deployed production devices before responsible disclosure is complete.
- Reproduces copyrighted vendor documentation or datasheets in full without permission.

For urgent safety matters, contact a Volunteer or Core Founding Team member directly rather than opening a public issue.

## Review and Moderation

Maintainers may edit, request changes, or decline submissions to protect legal compliance, community safety, and educational quality.

Repeated violations may trigger moderation actions under the graduated warning model defined in [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
