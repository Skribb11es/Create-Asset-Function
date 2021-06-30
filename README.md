# Create-Asset-Function
A simple Lua function designed to allow developers to directly download needed assets such as images to a users computer, with more functionality such as the ability to change file names and their extensions.

# Initilization
```lua
local createAsset = loadstring(game:HttpGet("https://raw.githubusercontent.com/Skribb11es/Create-Asset-Function/main/createAsset.lua", true))()
```

# Usage

## Just URL

In the case you only supply a URL, the function will default to the file name and extension within the URL.
```lua
local createAsset = loadstring(game:HttpGet("https://raw.githubusercontent.com/Skribb11es/Create-Asset-Function/main/createAsset.lua", true))()
createAsset("https://blog.roblox.com/wp-content/uploads/2017/01/Roblox_Logo_Square_Image.jpg")
```
Resulting in the function returning "assetCache/Roblox_Logo_Square_Image.jpg" with this usage.

## URL and File Name

If you are to supply a file name with the URL, the function will use the supplied name but will default the extension to the extension supplied within the URL.
```lua
local createAsset = loadstring(game:HttpGet("https://raw.githubusercontent.com/Skribb11es/Create-Asset-Function/main/createAsset.lua", true))()
createAsset("https://blog.roblox.com/wp-content/uploads/2017/01/Roblox_Logo_Square_Image.jpg", "example")
```
Resulting in the function returning "assetCache/example.jpg" with this usage.

## URL and Extension

If you are to supply an extension with the URL, the function will use the supplied extension but will default the name to the name supplied within the URL. Do note that if you are going to supply an extension but not a file name, it is manditory that you add a blank string where the name would otherwise be located. The easiest way to do this is demonstrated below.
```lua
local createAsset = loadstring(game:HttpGet("https://raw.githubusercontent.com/Skribb11es/Create-Asset-Function/main/createAsset.lua", true))()
createAsset("https://blog.roblox.com/wp-content/uploads/2017/01/Roblox_Logo_Square_Image.jpg", "", ".png")
```
Resulting in the function returning "assetCache/Roblox_Logo_Square_Image.png" with this usage.

## URL, File Name, and Extension

If you supply the function with a URL, file name, and extension, the function will rename the output and change the file name to the desired output.
```lua
local createAsset = loadstring(game:HttpGet("https://raw.githubusercontent.com/Skribb11es/Create-Asset-Function/main/createAsset.lua", true))()
createAsset("https://blog.roblox.com/wp-content/uploads/2017/01/Roblox_Logo_Square_Image.jpg", "example", ".png")
```
Resulting in the following output of "assetCache/example.png" with this usage.
