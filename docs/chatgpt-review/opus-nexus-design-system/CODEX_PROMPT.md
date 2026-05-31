# ChatGPT Review Prompt - Opus Nexus Design System

Use this as Codex instruction when implementing the reviewed design system.

## Context

Opus Nexus is a premium personal assistant / personal command center.

Visual direction:
- Dark UI
- Roman inscriptions, sharp geometric, authoritative
- Gold is a restrained brand authority accent, not a full-app theme

Functional colors:
- Blue: health / protein / water / feedback
- Green: training / movement / fiber / sync / success
- Purple: sleep / recovery / Vita support
- Orange: energy / warning / attention
- Red: critical alert / deficit
- Gray: inactive / missing data

## Files

Copy reviewed files from this folder into the app when ready:

```txt
design-tokens/opus-nexus.tokens.json
src/design-system/opusNexusTokens.ts
src/design-system/OpusNexusIcons.tsx
src/design-system/OpusNexusIconSystem.tsx
```

## Implementation requirements

1. Use `opusNexusTokens.ts` as the app token source.
2. Use custom SVG icons from `OpusNexusIcons.tsx`:
   - `OpusNexusMark` for brand mark
   - `HealthHeart` for health primary
   - `VitaGuardianShield` for Vita
   - `FiberLeaf` for fiber
   - `SunriseIcon` for Today
3. Navigation and Utility tiles must use radius 8-10px, not big pills.
4. Active navigation may use gold; inactive states use readable gray.
5. Do not apply gold to every metric icon. Keep gold around 10-15 percent visual weight.
6. Add a temporary preview route/page using `OpusNexusIconSystem.tsx` for visual QA.
7. Preserve existing functionality; this is design-system integration only.

## Acceptance criteria

- Design tokens exist in JSON and TypeScript.
- Custom icons compile without external SVG files.
- Preview page renders the icon system.
- Bottom nav uses Today, Vita, Calendar, Approval icons consistently.
- Health uses Heart; Fiber uses Fiber Leaf; Vita uses Guardian Shield.
- No emoji icons are used.
