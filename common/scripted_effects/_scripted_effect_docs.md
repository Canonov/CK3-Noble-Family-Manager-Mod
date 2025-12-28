################################################################################
# DOCUMENTATION TEMPLATE FOR SCRIPTED EFFECTS
################################################################################
# Use this template at the top of each scripted effect file or before each effect
#
# Format:
# ## Effect Name
# Description of what the effect does
# 
# @scope: [character/title/province/faith/culture/etc] - Required scope type
# @param PARAM_NAME [type] - Description (default: value) {optional}
# @input scope:name [type] - Required scope passed in
# @output scope:name [type] - Scope created/modified by effect
# @var variable_name [type] - Variable used/created
# @example: Brief usage example
################################################################################


################################################################################
# Noble Family Management - Family Creation Effects
# nfm_scripted_effects/01_family_creation.txt
################################################################################

## nfm_effect_create_house_steward
# Creates a complete stewardship-focused noble family with parents, house head,
# heir, and siblings. Family size varies based on the family_size scope value.
#
# @scope: character - Must be called from the liege/employer who will hire the family
# @input scope:family_size [value] - Controls family composition (small/medium/large)
# @output scope:new_house_head [character] - The generated family head
# @output scope:new_heir [character] - The generated adult heir (16-18 years old)
# @output scope:head_father [character] - Father of house head (if family_size > small)
# @output scope:head_mother [character] - Mother of house head (if family_size > small)
# @var nfm_familysize_small [value] - Threshold for small family generation
# @var nfm_familysize_headchildcount [value] - Number of additional children to generate
# @var nfm_familysize_siblingsforcount [value] - Number of siblings to generate
# @example:
#   scope:family_size = nfm_familysize_medium
#   root = { nfm_effect_create_house_steward = yes }


################################################################################
# ADDITIONAL EXAMPLES
################################################################################

## nfm_elevate_character_to_noble
# Elevates a character to noble status, grants them prestige and a noble house
#
# @scope: character - The character being elevated (recipient)
# @param PRESTIGE_GAIN [integer] - Amount of prestige to grant (default: 500)
# @param CREATE_CADET [yes/no] - Whether to create cadet branch if dynasty exists (default: no) {optional}
# @input scope:grantor [character] - The ruler granting nobility (required)
# @output scope:new_title [title] - The noble house title created
# @var elevated_to_nobility [flag] - Sets character flag for tracking
# @example:
#   scope:recipient = {
#     nfm_elevate_character_to_noble = {
#       PRESTIGE_GAIN = 1000
#       CREATE_CADET = yes
#     }
#   }

nfm_elevate_character_to_noble = {
    # Implementation here...
}


## nfm_apply_house_opinion
# Applies opinion modifiers to all members of a noble house
#
# @scope: character - Any character (typically the grantor/liege)
# @param TARGET_HOUSE [house] - The house scope to apply opinions to (required)
# @param OPINION_TYPE [string] - Localization key for opinion modifier (required)
# @param OPINION_VALUE [integer] - Opinion value to apply (default: 0)
# @param DURATION [integer] - Duration in days (default: permanent) {optional}
# @example:
#   root = {
#     nfm_apply_house_opinion = {
#       TARGET_HOUSE = scope:recipient.house
#       OPINION_TYPE = nfm_op_elevated
#       OPINION_VALUE = 30
#       DURATION = 3650
#     }
#   }

nfm_apply_house_opinion = {
    # Implementation here...
}


################################################################################
# DOCUMENTATION TAG REFERENCE
################################################################################
#
# @scope: [type] - What scope type this effect must be called from
#   Types: character, title, landed_title, province, faith, culture, house, 
#          dynasty, artifact, secret, struggle, any
#
# @param PARAM_NAME [type] - Parameter that can be passed in
#   Types: integer, value, yes/no, string, scope, flag, list
#   Add (default: X) if there's a default value
#   Add {optional} if the parameter is not required
#
# @input scope:name [type] - Scope that must exist before calling
#   Mark as (required) or {optional}
#
# @output scope:name [type] - Scope created or modified by the effect
#   Include what it represents
#
# @var variable_name [type] - Variables used or created
#   Types: flag, value, boolean, scope_value
#
# @example: - Usage example with typical parameters
#   Should be a complete, copy-paste-able example
#
# @note: - Special considerations or warnings
#   Use sparingly for important gotchas
#
# @see: - Reference to related effects
#   effect_name - Brief description
#
################################################################################


################################################################################
# QUICK REFERENCE CARD
################################################################################
# Place at the top of each scripted effects file:

# FILE: nfm_scripted_effects/01_family_creation.txt
# PURPOSE: Character generation for noble families
# EFFECTS:
#   - nfm_effect_create_house_steward
#   - nfm_script_create_family_martial
#   - nfm_script_create_family_learning
#   - nfm_script_create_family_intrigue
#   - nfm_script_create_family_foreign
# COMMON INPUTS:
#   - scope:family_size [value] - Controls generation size
# COMMON OUTPUTS:
#   - scope:new_house_head [character] - Always created
#   - scope:new_heir [character] - Always created
################################################################################