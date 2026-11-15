# Design decisions

## Product scope

A small listening room, not a streaming-service clone. The catalog is intentionally three real tracks. No fake social proof, recommendation intelligence, popularity metrics, billing, or account system.

## Information architecture

Discover → mood/search → track playback → queue → saved collection. The global audio element is independent from the view. The primary session action replaces the queue unless the listener has locked it.

## State contract

- Arrive paused; explicit user intent starts audio.
- End of queue stops unless repeat-all is active.
- Repeat-one applies to natural completion; manual next still advances.
- Shuffle preserves the current track and randomizes the remainder.
- Queue membership is unique; adding a duplicate gives feedback.
- The current track cannot be removed. Reorder does not restart playback.
- Queue lock blocks mutation, not playback or navigation. It is not a security boundary.
- Named sessions persist original track IDs. Local files are deliberately excluded.
- Local audio is session-only and never uploaded.
- Saved preferences are local to this browser, not synchronized.

## Visual system

Paper #f5f3ec, ink #22241f, muted #686b63, cobalt #254be8. Dark mode uses #1b1e1c, #eeeee4 and #a5b4ff. DM Sans supports interface text; DM Serif Display adds an editorial voice. Album artwork retains its colors in either theme.

## Responsive choices

Desktop: a left rail, editorial hero, three-column record shelf and full player. Tablet: compact top navigation. Mobile: a stacked hero, compact track rows, essential mini-player and expanded Now Playing controls. The layout prioritizes reading and control size over matching a desktop composition at every width.

## Accessible interaction intent

Native buttons, anchors, range inputs and dialogs; visible focus; a skip link; named controls; status announcements; keyboard playback shortcuts that avoid form controls; reduced motion. Explicit queue arrows avoid a drag-only interaction. These choices are implementation evidence, not a conformance claim.

## Figma handoff

https://www.figma.com/design/w4ichthh1SMuQNj2Mk40c5

Pages: Design system, Experience, Mobile prototype. Variables mirror the code's semantic color roles. Prototype connections demonstrate arrival, playback, pause, saved state, queue and next-track/dark state. The live app remains the behavioral reference. The Figma prototype does not play the audio.
