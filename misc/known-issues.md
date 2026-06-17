# 🐞 Known Issues

#### Pets & Collision

* Certain pets such as Dragons, Bears, and Eggs may cause collision or movement issues in some situations.
* If a character becomes stuck, switching to a different pet serves as a workaround while a fix is developed.

#### Hunting Matchlock Issues

* Hunting Matchlocks may currently display retry or usage errors.
* As a temporary workaround, players can now exchange Matchlocks into the Ranger-exclusive [**Huntress Bow**](https://moonbd.online/codex/item//1007558).
* Added exchange support through the Velia **\<New Class Weapons & Matchlock Exchange>** [**Minotavros**](https://moonbd.online/codex/npc/901009).
* The Huntress Bow is intended as a temporary replacement hunting weapon until Matchlock functionality is fully restored.
* Once the issue is resolved, Huntress Bows will be converted back into Matchlocks automatically.

#### Maegu Skill Issues

* Maegu Fox summons may not properly appear during certain skills.
* Some Maegu skills may occasionally fail to register the first hit correctly.
* Investigation and combat testing are ongoing for these issues.

#### Buff Display Issues

* Drakania, Woosa, and Maegu E-Buff icons may not appear in the buff bar even though the buff effects are functioning normally.

#### Accessory Crystal Socketing

**Kharazad & Preonne Limitations**

* There is currently a known UI discrepancy involving Kharazad and Preonne accessories.
* The socketing interface may incorrectly display all Versatile Crystals as available options.
* At this time, these accessories only support Dawn Crystals.

**Current Requirement**

* Only Dawn Crystals can be successfully socketed into Kharazad and Preonne accessories.

**Known UI Issue**

* The interface does not properly filter incompatible crystals from the socketing menu.

**Result**

* Attempting to socket unsupported crystals will trigger an `Item Restricted` error.

#### Crystal Management

**Stacked Item Conflict**

* There is currently a technical limitation involving stacked crystals in inventory.
* If a crystal exists in a stack with a quantity greater than one, socketing may fail.

**Resolution**

* The character opens Storage or Market Warehouse.
* The full crystal stack is moved into storage.
* Exactly one crystal is withdrawn into the inventory.
* The socketing process is attempted again.

#### Technical Support

If `Item Restricted` errors or socketing failures persist:

* The crystal must match the accessory requirements.
* Only a single crystal must exist in the inventory.
* If the issue persists:
  * A screenshot of the error is captured.
  * A ticket is opened through the [**official Discord**](https://discord.gg/3xK6p7rhD4) ticket system for support.
