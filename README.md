# Week 5 assignment DTD-DAD: What I Changed and Why

When I used the original app, I accidentally lost the data I had entered because I used the phone's back gesture to close the keyboard. Instead of hiding the keyboard, the app immediately went back to the previous screen without any warning. I redesigned the screen to fix this issue and improve the overall user experience.

## Constraint

I changed the back action so that if I have unsaved input, the app first asks whether I want to **Keep Editing** or **Discard and Go Back** instead of leaving the page immediately. This prevents accidental data loss. I also disabled the **Search** button until the entered value matches the expected format for the selected search method, preventing invalid searches.

## Discoverability

I made the selected search method much more obvious by giving it a clear selected state while keeping the others unselected. I also added helper text below the input field to show the expected format (for example, an EPIC number). Since I originally used the back gesture just to hide the keyboard, I added a persistent **Hide Keyboard** button whenever the keyboard is open so that the correct action is easy to find.

## Feedback

I added real-time validation while typing so the app immediately tells me whether my input is valid or if it needs correction. When I tap **Search**, the app now shows a loading indicator instead of appearing unresponsive. I also added toast messages to confirm actions such as closing the keyboard, discarding unsaved changes, and completing the search, so I always know what the app is doing.
