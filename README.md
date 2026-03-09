# riftbound-auditor
A simple game state reconstruction tool for Riftbound Judges and players. It allows for verifying mathematical consistency, tracking rune deck flow, and solving turn count.
It tracks rune flow from the deck to the board, accounting for turn-channeled, “ramped”, and recycled runes.

CORE MODES
  - SOLVER MODE
  Used to calculate a missing parameter.

  Set one value to SOLVING and the others to FIX.
  
  Automatically accounts for starting runes (2 if Going First, 3 if Going Second).
  
  Calculates passive draw (2 runes per turn).
  
  Solves for Board, Turn, Ramp, or Recycles based on the current state.


  - AUDIT MODE
  Used for manual verification (e.g., during a Judge investigation).

  All fields are unlocked.
  
  The tool flags a DISCREPANCY if the entered board state does not match.
  
  the theoretical calculation.
  
  Flags a BOARD ERROR if entries exceed the physical limit of 12 runes.
  

- - - 
MONITORING STATS
- RUNES IN DECK: Real-time count of remaining resources.
- SUPPLY DEMAND (Control Stat): Total runes requested from the deck since
  the start. This value helps track total resource consumption.
- DECK DEPLETED: This flag is triggered only when the "Runes in Deck" count reaches zero,
  indicating that no further runes can be channeled regardless of the total Supply Demand.
- NET RECYCLES: Total runes recycled minus any Tokens/Effects discounts.


TECHNICAL INFO

- FORMAT: Single-file HTML (index.html).

- DEPENDENCIES: Uses Tailwind CSS via CDN. Requires an internet connection to load styles, but logic is handled locally via Vanilla JavaScript.

- PRIVACY: No data is stored or transmitted. All calculations happen locally in the browser. Use "Reset Session Data" to clear the current state.


Developed for the Riftbound Community <3
