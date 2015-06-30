# SketchPlugin-Remember
A sample plugin that demonstrates how to save variables and access them later.

---

Note: This is only for Sketch Plugin developers and will be of no use to you otherwise as a standalone plugin!

## Setup  

Copy the `pluginDefaults.js` file in your plugin folder.


## Usage

**Import** the `pluginDefaults.js` script using a relative path to the script file:

	@import 'pluginDefaults.js'


Create a `presets` variable to hold default values. These values will be used the first time your plugin is run.

	var presets = {
		myName: "Sketchy Jones",
		myAge: 25
	}


**Initialize defaults** with a unique plugin domain value and the `presets` created above. Do this once at the beginning of your plugin script.

	var userDefaults = initDefaults("com.yoursite.plugin-name", presets)


After initializing defaults, you can **access default values** via the `userDefaults` variable: 

	var myName = userDefaults.myName
	var myAge = userDefaults.myAge


**Set default values** via the `userDefaults` variable, then **commit the changes** to persist values between plugin runs and app launches:

	userDefaults.myName = "Carl Sagan"
 	userDefaults.myAge = 81

 	saveDefaults(userDefaults) // commit changes


You can also **add new variables** to save as defaults that were not included in `presets`:

	userDefaults.myNationality = "American"
	saveDefaults(userDefaults) // commit changes


If you wish to allow your users to **'Restore Original Settings'**, simply overwrite defaults with `presets`:

	saveDefaults(presets)


Please check the example plugin to see all this in action.

---

Ping me [@abynim](http://twitter.com/abynim) if you find this useful or run into issues.

Enjoy!