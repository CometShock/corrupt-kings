# Initial Spec

Build a "player's future match rewards" token.

For simplicity of the Autonomous Anonymous Lisbon 2024 hackathon, make sure that each player eligible for this "future match rewards" token already owns a minimum of the maximum match rewards (for any single player).

## Flow

1. In order for a player create their token, they deposit the maximum match reward amount into the escrow contract.
2. Player receives 100 player-match "tokens" (MUD table entry). 
3. Player can then propose a swap with another player within the match
4. If other player accepts, check if they have created their own player-match token. (If no, automate steps 1-3 for them.) Then execute the swap.
5. At match conclusion, check match winner data. Allow "token" holders to claim the rewards, proportional to their ownership.

## Data needed from SkyStrife

- Match info
  - Match entity
  - Player entities
  - Match started?
  - Match finished?
  - Match rewards
    - 1st place
    - 2nd place
    - 3rd place
    - ... etc
- Player info
  - Did player already create a match token
  - What match tokens does the player own
  - For the match, how much did the player deposit