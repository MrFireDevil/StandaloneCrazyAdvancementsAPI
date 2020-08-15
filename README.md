# CrazyAdvancementsAPI - Standalone Edition
[![](https://jitpack.io/v/jely2002/StandaloneCrazyAdvancementsAPI.svg)](https://jitpack.io/#jely2002/StandaloneCrazyAdvancementsAPI)
[![](https://jitci.com/gh/jely2002/StandaloneCrazyAdvancementsAPI/svg)](https://jitci.com/gh/jely2002/StandaloneCrazyAdvancementsAPI)

This is a fork of the CrazyAdvancementsAPI by ZockerAxel that has been made Maven compatible. This means that the API can now be used with Maven and as a standalone dependency that can be bundled with your plugin. This way there is no need for the server to also have the CrazyAdvancementsAPI plugin.

## Usage
The version of this API that you should use depends on the minecraft version your server/plugin is on. See the chart below.
| Minecraft version | API/dependency version |
| ------------- | ------------- |
| 1.16.2  | 1.13.9  |
| 1.16.1  | 1.13.8  |
| 1.15.x  | 1.13.7  |

**Add the dependency to your pom.xml**
```xml
<dependency>
    <groupId>com.github.jely2002</groupId>
    <artifactId>StandaloneCrazyAdvancementsAPI</artifactId>
    <version>1.13.9</version>
</dependency>
```
**Add the repository to your pom.xml**
```xml
<repository>
     <id>jitpack.io</id>
     <url>https://jitpack.io</url>
</repository>
```

## How to initialize the API
In order to initialize/disable the 'StandaloneCrazyAdvancementsAPI' you need to include the following code in your `onEnable()` and `onDisable()` methods. The rest of the process is almost the same as the original API.

**Example `onEnable()` & `onDisable()` methods:**
```java
private CrazyAdvancements advancementsAPI;

@Override
public void onEnable() {
  this.advancementsAPI = new CrazyAdvancements(this);
}

@Override
public void onDisable() {
  advancementsAPI.disable();
}
```

## How does the API work?
For more info on how you may use this API please take a look at the [original documentation](https://www.spigotmc.org/resources/crazy-advancements-api.51741/). There are also [javadocs](https://crazyadvancements.endercentral.eu/overview-summary.html) available, but please keep in mind the changes this Maven edition brings with.

## Credits
I would like to thank [ZockerAxel](https://github.com/ZockerAxel) for writing [the API](https://github.com/ZockerAxel/CrazyAdvancementsAPI) this Maven edition is based on.
This project has been made according to the GPL-3.0 license bundled with the original code. All changes can be seen through 'commits'.
