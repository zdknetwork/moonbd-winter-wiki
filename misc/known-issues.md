# 🐞 Known Issues

### Accessory Crystal Socketing

#### Karahzad & Preonne Limitations

There is a known UI discrepancy regarding **Karahzad** and **Preonne** accessories. While the socketing interface may display all **Versatile Crystals**, these items are currently restricted.

* **Requirement:** Only **Dawn Crystals** can be successfully socketed into these accessories.
* **The Issue:** The UI does not filtered out incompatible crystals, allowing them to be selected in the menu.
* **Error:** Attempting to socket a non-Dawn crystal will result in an `Item Restricted` error.

***

### Crystal Management

#### Stacked Item Conflict

A technical limitation prevents crystals from being pushed onto items if they are part of a stacked pile in the inventory. If the system detects a quantity greater than one, the socketing action will fail.

**How to Fix:**

1. Open your **Storage** or **Market Warehouse**.
2. Move the entire stack of crystals into the storage.
3. Withdraw exactly **one (1)** crystal into your character's inventory.
4. Proceed with socketing the item.

***

### Technical Support

If you encounter an `Item Restricted` error or socketing failure that is not covered by the scenarios above, please follow these steps:

1. Ensure the crystal matches the item requirements (e.g., **Dawn Crystals** for **Karahzad**).
2. Verify you only have a single unit of the crystal in your bag.
3. If the issue persists, capture a screenshot of the error and open a ticket in the **Discord Ticket System**.
