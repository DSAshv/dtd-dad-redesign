DTD-DAD Week 5 assignment

What I changed and why

Your original bug — the back gesture silently discarding form data — is a constraint failure: the app let a destructive action happen with zero friction. The redesign fixes that plus the two other heuristics you named:

Constraint: Back now checks if there's unsaved input. If so, it blocks the navigation and forces a choice ("Keep editing" / "Discard and go back") instead of silently leaving. Search stays disabled until input actually matches the expected format for the selected type, so you can't submit garbage.
Discoverability: Each search-type card now shows a clear selected/unselected state (was previously always purple regardless of selection) and a helper line explains exactly what format to enter for that method. A persistent "Hide keyboard" bar appears the moment you tap the input, so you never need the risky back-gesture just to dismiss the keyboard.
Feedback: Real-time inline validation ("Looks good" / format hint) as you type, a loading state on Search, and toast confirmations for every state-changing action (keyboard closed, entry discarded, search complete) — so nothing happens invisibly.
