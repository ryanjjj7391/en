[&#8249; SdkboxAds Doc Home](./)

<h1>SdkboxPlay Integration Guide</h1>
<<[../../shared/-VERSION-/version.md]

##Prerequisites

###Google play
 + Follow this instructions to enable game services for your game and create a linked application. Otherwise, the app won’t be able to make connections to google play. https://developers.google.com/games/services/console/enabling#step_2_add_your_game_to_the_dev_console
 + Use developer console to configure leaderboards and achievements.

###Game Center
 + Enable Game Center on XCode.
 + Use developer console to configure leaderboards and achievements.


##Integration
Open a terminal and use the following command to install the SDKBOX SdkboxPlay plugin. Make sure you setup the SDKBOX installer correctly.
```bash
$ sdkbox import sdkboxplay
```

<!--## Configuration
<<[../../shared/sdkbox_cloud.md]
<<[../../shared/remote_application_config.md]-->

### JSON Configuration
SDKBOX Installer will automatically create a sample configuration `sdkbox_config.json` for you

Here is an example of the SdkboxAds configuration:
```json
    "sdkboxplay" : {
      "leaderboards" : [
        {
          "id" : "CgkI0sux8sMWEAIQAA",
          "name" : "ldb1"
        }
      ],
      "achievements" : [
        {
          "id" : "CgkI0sux8sMWEAIQAg",
          "name" : "ten-games",
          "incremental" : false
        },
        {
          "id" : "CgkI0sux8sMWEAIQAw",
          "name" : "hunter",
          "incremental" : false
        },
        ...
      ],
      "debug" : true,
      "connect_on_start" : false
    }

As it can be seen, leaderboards and achievements have a human readable name, and a machine generated id. This is on purpose so that the same API can be used between platforms. While Google play generated random ids like the ones shown, iOS Game Center will be more human friendly. 
In either case, the developer will reference leaderboards and achievements by a name of his choice, like in the example shown.
    
```

<!--<<[sdkbox-config-encrypt.md]-->

##Usage
<<[usage.md]

<<[api-reference.md]

<<[manual_integration.md]

<<[manual_ios.md]

<<[../../shared/manual_integration_android_and_android_studio.md]

<<[manual_android.md]

<<[extra-step.md]

<<[proguard.md]
