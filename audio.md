# Audio System

## Requirements
1. Selected audio system must support all required platforms
2. Must support 3D positional sound (Hardware support is desired, Dolby, THX, etc...)
3. Must support playing of some compressed sound format (Vorbis, MP3, etc...)
4. Must support multi-channel playback
5. Playback from disk based files (no streaming required)

## Uses
The audio system will be used to play a variety of sounds on the client system during gameplay, including:

1. GUI and HUD notification sounds (2D)
2. Sound effects attached player tanks (3D)
3. Sound effects attached to map locations (3D)
4. Music and voice over tracks as needed (tutorials?)

### Scope Limitations
The audio system will focus on in-game sounds.  Voice chat is beyond the scope of the game and is better handled by third-party applications.  We may, however, offer integrations with one or more third-party voice chat applications, such as offering player position information to Mumble for positional audio.

## OpenAL
OpenAL appears to support all the desired platforms and features, so is highly likely to be the best choice.  On Windows, Linux, and OS X, OpenAL Soft can be used.  iOS includes a proprietary OpenAL, and Android may also be supported by OpenAL Soft. 
