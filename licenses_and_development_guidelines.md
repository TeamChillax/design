This page lays out some details for how we intend for this project to operate with respect to development and licensing of our source code.

# License and Ownership

This product will be open-source software. It is important to us that it remains free and accessible to everyone, and that nobody can take someone else's work intended for public benefit and restrict people's freedom to use, modify and extend it. On the other hand, we understand that there are many widely-used proprietary devices which are unfriendly to certain open-source licenses, so for modules that will need to run on such devices, we need a license that still preserves people's freedoms but does not conflict with those specific platforms' end user license agreements.

This project may include not only source code created by project members, but also source code submitted by members of the community. We must therefore also consider copyright enforcement issues, as well as a potential future need to re-license our source code for reasons that might arise.

## Copyright Assignment

While this is a complex issue which might still need more discussion, our current intent is to form a legal partnership between the project's core maintainers which will hold copyright over the project's source code. This arrangement, where individual maintainers may come and go while still maintaining the integrity and presence of the body, is thought to be superior to having any single person holding the copyright for all of our source code. Submissions of source code from both project members and community members will only be accepted once the author agrees to assign copyright of their work to the partnership of maintainers. This method provides for the future option of re-licensing source code after a decision of the partners, rather than having to track down every individual contributor and asking them to re-license their work under the desired license.

## Game Client and User Tools Code License

Our current intent is to use the [Mozilla Public License (MPL)](https://www.mozilla.org/en-US/MPL/) Version 2.0 for all modules that may be included in binaries intended to run on users' devices. We chose this license because it has strong protections for source code, including derivative works. We also chose this license over the [GNU General Public License (GPL)](https://www.gnu.org/licenses/gpl.html) and the [GNU Lesser Public License (LGPL)](https://www.gnu.org/licenses/lgpl.html) because it is compatible with the distribution of binaries on Apple's macOS, iOS and tvOS app stores.

## Network Services and Web Code License

Our current intent is to use the [GNU Affero Public License (AGPL)](https://www.gnu.org/licenses/agpl-3.0.en.html) for all modules intended to provide a network service or web interface (excluding modules that are also used by the game client or user tools, which were discussed above). We chose this license because we intend for all server-side code, some of which may be written in an interpreted or markup language (which may never be compiled into binary form), to have the same protections as our other source code, including the mandatory availability of source code for download and inspection. We are currently evaluating the option of adding a clause to this license to make it compatible with the [OpenSSL License](https://www.openssl.org/source/license.html) in case we choose to use that library for encrypted communication.

## Assets License

We define *assets* to include all media, artwork and data included with and used by the game client or user tools that would not generally be compiled into a binary for execution. Some examples of assets we might use include textures, logos, icons, and world maps, including intermediate forms such as vector artwork files. Our current intent is to use one of several available [Creative Commons](https://creativecommons.org) licenses, such as [CC0](https://creativecommons.org/share-your-work/public-domain/cc0/), [CC BY](https://creativecommons.org/licenses/by/4.0/) or [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/). The merits of each license will continue to be evaluated and we will choose a specific one at a later time.
