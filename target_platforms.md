# Target Platforms

This project will be a cross-platform game. Our goal is to support both PC and mobile devices, and to evaluate the possibility of supporting certain television set-top devices like the Apple TV, with consistent gameplay, simulation and behavior among all platforms and devices. During development, we will evaluate the feasibility of the mobile gameplay experience as well as whether PC and mobile users can play together competitively.

## Desktop platforms

We will be targeting the three most popular desktop operating systems for this project: Microsoft Windows, Apple's Mac OS X, and Linux. In considering support for legacy versions of these operating systems, we will balance the desire to support users with devices that are less than cutting-edge with our need to use modern hardware and software features and to create a pleasing experience for the user.

### Windows

Our intention is to support Windows Vista and later. The reason for this is because earlier operating system versions are no longer supported by Microsoft and do not receive security updates.

### Mac OS X

Our intention is to support Mac OS X 10.7 and later. The reasons for choosing this specific version are that there was a major change in the developer tools and application features starting with this version, this version will likely support the graphics library version that we will need and this version is the latest one supported on much of the legacy hardware still in use today.

### Linux

Linux has a tremendous variety of kernel, software and distribution versions that make it complicated to target a specific features or particular specifications. However, our intention is for this project to be available pre-packaged in some form for distributions that support it, as well as to have a method for pushing out updates more quickly than the traditional distribution upgrade process. At the very least, users should be able to build the project from source on distributions that have the necessary library and build tool dependencies.

## Mobile Platforms

We intend to target Apple's iOS and Google's Android operating systems for mobile devices. Minimum device and operating system version requirements will be based on the needs of other dependencies (such as the rendering engine) as well as the eventual processing needs of the game. These will become clearer after some actual development progress is made.

## Television Set-Top Boxes

Recent revisions of the Apple TV have support for games, which can be controlled using the Siri remote, Bluetooth controller or possibly a USB keyboard. While this would be a rather niche market, it is possible that this platform can be gained with little or no code beyond what we will need for iOS support. If this turns out to be the case, then supporting this platform could be worthwhile as this type of game might be relatively unique among what is available for this device which could help expand our user base.
