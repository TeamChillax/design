# Audio System
This document 

## Requirements
1) Selected Audio System must support all required platforms
2) Must support 3d positional sound (Hardware support is desired, Dobly, THX, etc...)
3) Must support playing of some compressed sound format (Ogg, MP3, etc...)
4) Must support mult-channel playback
5) Playback from disk based files (no streaming required)

## Uses
The audio system will be used to play a variety of sounds on the client system during gameplay, including.

1) GUI and HUD notification sounds (2d)
2) Sound effects attached player tanks (3d)
3) Sound effects attached to map locations (3d)
4) Music and voice over tracks as needed (tutorials?)

### Scope Limitations
The audio system will only support in game sounds, it will not be used to record player voices, or provide voice chat.
Voice chat is better supported through third party applications. 

If desirable the audio system can be made to integrate with popular third party voice chat systems if there are desirable features.

## OpenAL
OpenAL appears to support all the desired platforms and features, so is highly likely to be the best choice.
