PowerManagement
===============
Plugin for PhoneGap Build

This is adapted from code licensed by Wolfgang Koller. 
https://github.com/phonegap/phonegap-plugins/tree/master/iOS/PowerManagement

The original plugin was not compatible with PhoneGap Build.  We created a plugin.xml for ios.
Android will follow shortly, but we are not deploying there right now and cannot test it.

-- the rest of this file from the original readme at the GIT address above.

The PowerManagement plugin offers access to the devices power-management functionality.
It should be used for applications which keep running for a long time without any user interaction.

For details on power functionality see:

* Android: [PowerManager](http://developer.android.com/reference/android/os/PowerManager.html)
* iOS: [idleTimerDisabled](http://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/Reference/Reference.html#//apple_ref/occ/instp/UIApplication/idleTimerDisabled)
* WindowsPhone: [UserIdleDetectionMode](http://msdn.microsoft.com/en-US/library/windowsphone/develop/microsoft.phone.shell.phoneapplicationservice.useridledetectionmode%28v=vs.105%29.aspx)

Platforms
---------
For all platforms copy the *PowerManagement.js* file to your applications "www" folder and load it using the according HTML code.
`<script type="text/javascript" charset="utf-8" src="lib/cordova/powermanagement.js"></script>`

### Android
Copy the *PowerManagement.java* file to your *src/* directory.

Edit your *AndroidManifest.xml* and add the following permission:
`<uses-permission android:name="android.permission.WAKE_LOCK" />`

In addition you have to edit your *res/xml/plugins.xml* file to let Cordova know about the plugin:
`<plugin name="PowerManagement" value="org.apache.cordova.plugin.PowerManagement"/>`

### iOS
Copy the *PowerManagement.h* and *PowerManagement.m* files to your projects "Plugins" folder.

Add the PowerManagement plugin to the *Cordova.plist* file (to the Plugins list). Both Key and Value are "PowerManagement".

### WindowsPhone
Copy the *PowerManagement.cs* file to your projects "Plugins" folder.

License
=======
Copyright (C) 2011-2013 Wolfgang Koller

This file is part of GOFG Sports Computer - http://www.gofg.at/.

GOFG Sports Computer is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

GOFG Sports Computer is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with GOFG Sports Computer.  If not, see <http://www.gnu.org/licenses/>.

