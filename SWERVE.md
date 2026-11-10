# swerve

A big, dynamic, long-term feature-development project for Evan, Codex and Claude Code, forked directly from nightscout/Trio main. All work stays in EvanWamstad-Org/swerve; never modify EvanWamstad-Org/Trio.

- Display name: swerve. URL scheme: Swerve.
- Bundle ID: org.nightscout.TEAMID.swerve, with separate watch and LiveActivity extensions.
- App Group: group.org.nightscout.TEAMID.swerve.swerve-app-group.
- Signing storage: private EvanWamstad-Org/Swerve-Match-Secrets, seeded with existing encrypted distribution certificate files read from Match-Secrets. Original profiles and store are not changed.
- No schedules, upstream auto-sync or push-triggered builds. Run workflows manually.
- Certificate revocation is disabled in this fork.

## First TestFlight build

Follow https://triodocs.org/install/build/browser/browser-build-overview/ with the separate Swerve names above:
1. Run `2. Add Swerve identifiers` (includes validation and signing-store setup).
2. In Apple Developer create the separate Swerve App Group and assign it to Swerve, Swerve Watch App and Swerve Watch Complication. Enable Time Sensitive Notifications for the Swerve main identifier.
3. Create a NEW Swerve app in App Store Connect, choosing the Swerve bundle ID. Add an internal testing group and yourself as tester.
4. Run `4. Build Swerve and upload to TestFlight`. Install only after explicitly choosing to test this separate app.

Do not connect the experimental app to the pump controlled by the existing Trio installation. A successful build does not validate clinical behavior. xDrip and other integrations that assume standard Trio identifiers need separate compatibility work.

Upstream workflows are preserved as non-executable reference files in DeveloperDocs/Swerve/upstream-workflows. Upstream license and attribution remain in place. No dosing logic was changed for the initial setup.

## Project memory

The repo stays separate from the everyday Trio repository/app. Future features have not been chosen yet. Shared agent instructions live in AGENTS.md and CLAUDE.md; maintain them together. The Obsidian project home holds longer-term user decisions and session handoffs.
