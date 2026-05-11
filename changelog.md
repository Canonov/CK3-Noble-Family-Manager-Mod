# Changelog

## v1.5.1 - 2026/05/11
### Changed
- Non-Admin Rulers are now able to use the **Elevate a Noble Family** decision, it will be cheaper due to no admin house needing to be made.

### Fixed
- **Elevate a Noble Family** refunds should be more accurate and the new house head should get the costs now.


## v1.5.0 - 2026/05/10
### Added
- Added **Cadet Branch Control** system:
  - New game rules to configure minimum title rank, prestige level, and child count requirements for cadet branch formation
  - New decision to toggle cadet branch restrictions for your dynasty (ban/unban)
  - New interactions to forbid or restore cadet branch rights for specific houses
  - Based on my old mod "Ban Cadet Branch Tools & Rebalance"

- Added **Grant Cadet Branch** interaction where a liege, dynasty head, or house head can establish a cadet branch for a dynasty member (Available to non-Admin type governments, admin type governments now have a discount for Grant Noble Family Status for same dynasty members)
- Added **Debug Toggle Decision**, available in debug mode only, removes costs and restrictions from NFM decisions for the current character
- House aspirations will sometimes be assigned on creation based on house type, with support for Celestial and Japanese government types, base admin powerful family types to come.

### Changed
- NFM decisions now appear under their own group
- Grant Noble Family Status interaction now requires actor to be liege or above of recipient (no longer restricted to courtiers only)
- Grant Noble Family Status now offers a 50% prestige and influence discount when granting to a same-dynasty member
- Grant Noble Family Status base influence cost reduced from 150 to 125
- Elevate Lowborn cost reduced from 100 to 50 prestige; interaction now requires actor to be liege or above rather than checking courtier status
- All major costs now zero when debug toggle is enabled

### Fixed
- Grant Noble Family Status no longer targets ruling house heads or player heirs to a house head
- Updated descriptor to support CK3 1.19 'Scribe'


## v1.4.1 - 2026/02/24

### Changed
- Change required tier to duchy for county-level family governments
- Rebalance costs
- Move common triggers to can_use_nfm_interactions custom trigger

### Fixed
- Fix minor else using limit


## v1.4.0 - 2026/01/21

### Added
- Added "Poached Family Head" modifier to house head recruited via "Invite Foreign House Head" interaction
- Added house relation checks to "Invite Foreign House Head" interaction
- Added house relation changes for interactions and the decision

### Changed
- Inviting a house head now copies their existing family's title history.
- Buffed "Recently Founded House" fertility bonus from 20% to 30%
- Changed government checks to use direct influence/has noble family checks rather than just a general administrative type check

### Fixed
- Fixed availability conditions for all interactions and decisions (You won't be unable for seemingly no reason to do the interaction if they/you are travelling)


## v1.3.0 - 2026/01/17

### Added
- Added "Recently Founded House" modifier - newly created noble houses now receive a modifier for 10 years boosting fertility at the cost of stress gain and fellow vassal opinion
- Added game concepts explaining House Types with tooltips for each house type
- Added custom localization for displaying House Type names and descriptions

### Changed
- House type modifiers are now displayed in the event description alongside a hint of the house type, rather than the option text
- Reorganized localization files (moved toast localization to events file)
- Changed foreign house type modifier from raw opninion boosts to ignore_negative_culture_opinion.


## v1.2.0 - 2026/01/14

### Added
- Added Diplomatic House Type
- Added House Modifiers, each house type has a house wide modifier applied to it on creation.
- This ranges from the Steward's Governor XP gain, domain tax mult, and build cost, to the Martial House's levy size, prowess, and control bonuses, each house modifier will also have at least 2 main skill points.


## v1.1.0 - 2026/01/13

### Added
- New "Invite Foreign House Head" interaction to recruit heads of existing noble families from other realms
- New icon for "Dissolve Dying House" interaction
- New icon for "Invite Foreign House Head" interaction

### Fixed
- Removed unused localization keys


## v1.0.2 - 2026/01/10

### Added or Changed
- Use new vanilla method of creating a dynasty when elevating lowborns
- Add a toast notification to the elevate lowborn decision
- Fix Minor "trigger_else_if with no trigger_else" error


## v1.0.1 - 2026/01/09

### Added or Changed
- Quick Fixes for most glaring issues with AGOT compatibility 
- Set versioning to 1.18.* instead of 1.18.2