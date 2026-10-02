# Crowd Control Pack — Borderlands 3

## Pack metadata
- **Game display name:** Borderlands 3
- **Crowd Control game ID:** `Borderlands3`
- **Connector type:** `SimpleTCPServerConnector`


This repository supplies the PC Crowd Control pack descriptor for **Borderlands
3**. It contains effect metadata and the connector selection; the game-side
implementation is maintained separately:
<https://github.com/PyrexBLJ/CrowdControl-BL3>.

## Requirements

- Borderlands 3 for PC.
- The matching game-side mod from the linked project.
- A Crowd Control client using the Borderlands 3 PC pack.

## Installation and setup

Install the game-side mod using the instructions in its repository, then start
Borderlands 3 and select/start this pack in Crowd Control. This repository does
not bundle the mod or duplicate its loader and game-version instructions.

## Connection behavior

The descriptor uses a `SimpleTCPServerConnector` and legacy Crowd Control
messages. It does not override the connector host or port locally; those
connection details must remain aligned with the separately maintained mod
rather than being guessed or copied from another pack.

## Troubleshooting

- **No connection:** verify that the separately maintained mod is installed and
  that its version supports the effect codes exposed by this descriptor.
- **An effect is unavailable or behaves differently:** check the mod project’s
  documentation and game-state requirements. The descriptor lists effects but
  contains no game-side readiness logic.
- **Endpoint mismatch:** use the endpoint configured by the game-side mod; this
  repository defines no explicit endpoint to edit.

## Repository layout

- `Borderlands3.cs` defines the pack.