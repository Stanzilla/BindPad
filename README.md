# BindPad

by Tageshi

## WHAT IS "BindPad"

BindPad is an addon to make key bindings for spells, items, and macros.
You no longer need actionbar slots just to make key bindings for your macros etc.

The BindPad addon provides many icon slots in its frame. You can drag and drop
anything into one of these slots, and click the slot to set key bindings.

## HOW TO USE "BindPad"

1. Type /bindpad or /bp to display the BindPad frame.
(Also you can find a `Toggle BindPad` key binding command in the standard
key bindings frame of the Blizzard UI.)

2. Open your spellbook frame (`P`), your bag (`B`), or the macro panel (`/macro`).
(Also you can use three mini-icons on the BindPad frame to open these windows.)

3. Drag an spell icon, item icon, or macro icon using `Left Mouse Button` and
drop it onto the BindPad window.
(You may need to press `Shift Key + Left Mouse Button` to drag if your action bars are locked.)

4. Now you see the icon placed on BindPad frame. Click it,
and a dialog window that asks you to `Press a key to bind` will appear.

5. Tap a key to bind to the spell and click the `Close` button.

6. When you want to remove icons from BindPad frame, simply drag away the icon
and press right click to delete it.

Note that key bindings itself will not be unbinded when you delete the icon.
To unbind it, click the icon and click the `Unbind` button on the dialog window.
Also you can simply override key bindings with different ones.

## HOW TO USE TABS

----

### SLOT TABS

----

There are four tabs called slot tabs at the top of the BindPad frame:

* `General` slots are common icons used for every character and every spec.

* `Character Specific` slots are for icons specific to the current character
and current spec.

* [2] and [3] (aka. 2nd and 3rd character specific slots) will act
in the same way as `Character Specific` slots.

Note that you can only use the `Character Specific` tab after clicking
the `Character Specific Key Bindings` checkbox.

----

### PROFILE TABS

----

There are another three tabs on the side of BindPad frame.

Different Profiles can hold different contents in `Character Specific` slots.
You can click a profile tab to switch your current profile, and your choice of
profile is saved for each talent spec and automatically reverted to former
profile when you change talent specs. If you choose the same profile for both
talent specs this automatic change will not happen.

Note that `General` slots are not effected by a profile change, as all
contents of the `General` tab are common to all characters AND all specs.
If you change your profile while the `General` tab is shown,
BindPad will automatically show the `Character Specific` slots tab of
the specified profile.

----

### CAN I SWITCH PROFILE IN COMBAT? ON STANCE CHANGE

----
No, you cannot.

If you need different skills bound for different stances/forms,
simply use the stance condition to decide on what skill to use.

Example: `/cast [stance:1/2] Berserker Stance; [stance:3] Intercept`

Where `[stance:1/2]` is conditioning the macro for you to be in `Battle Stance`
or `Defensive Stance` and `[stance:3]` is conditioning you to be in `Berserker Stance`.
This works for all classes with stances (Including Rogues for `Stealth` (`[stance:1]`)
and `Shadow Dance` (`[stance:2]`) or none of the previous `[stance:0]`).

Druid example: /cast [stance:1] Bash; [nostance:1] Healing Touch

[nostance] = Caster, [stance:1] = Bear, [stance:2] = Aquatic, [stance:3] = Cat,
[stance:4] = Travel, [stance:5] = Tree/Moonkin if available else Flight,
[stance:6] = Flight if Tree/Moonkin is not available.

----

### "You want to convert this icon into a BINDPAD MACRO?"... What

----

"BindPad Macro" is a new feature from BindPad version 1.8.0 ;
which allow you to make almost unlimited number of virtual macro icons.

Older versions of BindPad just let you save your limited action bar slots.
This new BindPad will let you save your limited macro slots on the standard
"Create Macro" panel.

Usage:

- Click the small red "+" icon to create an empty BindPad Macro.
- Right-click an existing spell/item/macro icon on BindPad to convert it into a BindPad Macro.
- Right-click the "BindPad Macro" to edit macro-text.
- ...and you can use left-click to set keybindings as usual.

Note that BindPad Macro will only exist within the BindPad frame;
You can drag-and-drop them within BindPad, but you cannot drop them outside.

----

### DETAILS AND MORE INFORMATION

----

BindPad addon utilizes basic functions from the WoW API.

You can use these functions (and many others) in any addons or macros.

```lua
GetBindingKey("command")
SetBinding("KEY", "command")
SetBindingSpell("KEY", "Spell Name")
SetBindingItem("KEY", "itemname")
SetBindingMacro("KEY", "macroname"|macroid)
```

Just don't forget to save changes by calling
`SaveBindings(GetCurrentBindingSet())`.

There are some other similar addons by other authors.
Try them and choose what you like.

* [SpellBinder](https://www.wowinterface.com/downloads/info5614-SpellBinder.html)

* [mBindings](https://www.wowinterface.com/downloads/info11614-2.html)

* [ncBindings](https://www.wowinterface.com/downloads/fileinfo.php?id=15270)

* [ProKeybinds](https://www.wowinterface.com/downloads/fileinfo.php?id=18841)

Also you can visit [Wowpedia](https://wow.gamepedia.com/Making_a_macro) for more information about keybindings and macros.
