# MOB PLACEMENT EDITOR:

This tool can be used to edit mobPlacementParam and subEventPlacementParam. Both can be extracted from advCommonParam.xfbin (rpg/WIN64) with Sutando's Xfbin Parser. These files determine how NPCs will behave in adventure mode. You can change their placement, scripting, and a lot more. SubEvent contains mobs related to main events of the story, MobPlacement contains secondary mobs.

## Fields:

**Stage Name:**
Field which defines the stage where the mobs on this section will appear.

**Sub Event:**
Unclear, probably used for mobs that appear when you've progressed enough in adventure mode.
Only available for subEventPlacementParam.

**Sequence:**
Unclear. Related to the field above.
Only available for subEventPlacementParam.

**Action:**
Type of mob (is it interactable by pressing B? is it a trigger?)

**Model:**
Viewmodel of mob. Defined in mobLooksParam.bin and mobLooksListParam.bin (rpg/WIN64/advCommonParam.xfbin)

**Animation:**
Animation of mob.

**Script:**
List of scripts that will be executed when the mob is interacted with (rpg/script/rpg_script.xfbin)
These scripts can be modified with my LUA editor. You can add more scripts or modify existing ones.

**Unique ID:**
Unknown use, but it has to be unique

**Position:**
World position of the mob

**Direction:**
Look direction of the mob

**Collision Radius:**
Self explainatory

**Event Collision Type:**
See below for information.

**Event Collision Position:**
Position of the event collision

**Event Collision Radius:**
Radius of the event collision

**Drop Item ID:**
Usually used for boxes and gimmicks that can be broken. Defined in dropItemInfo.bin (rpg/WIN64/advCommonParam.xfbin)
Only available for mobPlacementParam.

**Icon:**
The icon that will appear on top of this mob. See below for more information.

## Types of Data:

**ACTION TYPES:**
- 0: NONE (No interaction)
- 1: ACTION (Interactable by pressing B)
- 2: TRIGGER (Automatic interaction when the player triggers with the mob's collision)
- 3: AREAIN (Unclear, probably similar to TRIGGER)
- 4: AREAIN_TRIGGER (Unclear, probably similar to TRIGGER)
- 5: SETUP (Unclear, perhaps it is executed automatically without interacting or triggering. Needs testing)

**EVENT COLLISION TYPES:**

- 0: NONE
- 1: NORMAL
- 2: LOCK
- 3: OFFSET
- 4: OFFSET_DIR
- 5: PLANE

**ICON IDS:**

- 0: NONE
- 1: TALK
- 2: MAIN
- 3: HOKAGE
- 4: SUB_EVENT
- 5: FRIEND_EVENT
- 6: SHOP
- 7: MOVE_STAGE
- 8: SAVE
- 16: SUDDEN
- 17: HOT_NET
