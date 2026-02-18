---
title: "Web Interface Redesign"
date: 2026-02-17T21:00:00+03:00
series: "What's new"
translationKey: "redesign-and-cool-features"
titleEmoji: ":tada:"
---
We've rolled out a fresh redesign of the web interface.

Many components were reworked to make the experience cleaner, more consistent, and more responsive — especially on mobile devices. The goal wasn't just to refresh the visuals, but to remove friction from everyday interactions and make the interface feel more predictable and alive.

Alongside the visual update, this release introduces several important functional improvements.

## Toast notifications

Actions like copying a link, adding items to the library, or deleting content now trigger small confirmation popups.

Previously, many of these interactions had no visible feedback, leaving users unsure whether the action actually worked. Now you immediately see a success, error, or informational message that appears briefly and disappears on its own.

## Status icons in the progress log

The processing log now uses visual indicators instead of text labels:
- ✓ completed steps
- ✕ errors
- ⚠ warnings

This makes it much easier to scan the log and understand what's happening, particularly on smaller screens.

## Smoother video playback start

In earlier versions, video playback could stutter during the first moments while the transcoder was warming up.

The system now pre-buffers up to five minutes of HLS segments as soon as transcoding begins. This allows playback to start smoothly from the very first second, without the initial buffering hiccups.

## Automatic restart of failed jobs

Previously, if a background job — such as downloading or transcoding — failed, it remained in an error state until manually restarted.

Now, when the same resource is requested again, failed jobs automatically restart. This removes the need for manual intervention and prevents stale failures from blocking the workflow.

---

This redesign is part of a broader effort to make Webtor more responsive, reliable, and easier to use in day-to-day scenarios.
More improvements to both UX and infrastructure are already in progress.
