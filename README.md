# SketchPlugin-Remember
A sample plugin that demonstrates how to save variables and access them later.

---

Note: This is only for Sketch Plugin Developers and will be of no use to you otherwise as a standalone plugin!

## Setup  
1. Copy the `lib` folder in your plugin folder  
2. In your `.sketchplugin` file, import `config.js` by adding `#import 'lib/config.js'` at the top  
3. Open the `config.js` file and set a unique value for the var `kPluginDomain`  
4. In the same file, add variables you want the plugin to remember and set initial values for them by editing the `userDefaults` variable.

## Usage
1. Once you've setup the `config.js` file as mentioned above, you can access values of default variables by using `getDefault('variableName')`.  
2. You can programmatically set the values of default variables using `setDefault('variableName', newValue)`.  

Enjoy!