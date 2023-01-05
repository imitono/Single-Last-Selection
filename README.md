# Single last selection Sublime Text plugin

## The problem

In Sublime Text, you can get out of a multiple selection mode by pressing the Esc key. When you do this, only the **first** selection will remain.

It would be convenient if there was a way to make it so that only the **last selection** will remain instead?

## The solution

This plugin creates a custom command "single_last_selection" that will escape multple selection mode and keep only the **last selection**.

## Create a keybinding

After installing the plugin create a key binding to the command.

In the following example I have changed the binding of the default "single_selection" command to "shift+escape" and binded "single_last_selection" command to "escape", since my preffered behaviour is to keep the last selection.

```
{ "keys": ["shift+escape"], "command": "single_selection", "context":
	[
		{ "key": "num_selections", "operator": "not_equal", "operand": 1 }
	]
},
{ "keys": ["escape"], "command": "single_last_selection", "context":
	[
		{ "key": "num_selections", "operator": "not_equal", "operand": 1 }
	]
},
```

## Credits

Full credits for this plugin go to https://superuser.com/a/1051516
