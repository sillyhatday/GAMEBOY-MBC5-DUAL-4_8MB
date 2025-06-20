# GAMEBOY-MBC5-DUAL-4/8MB
A working 8MB Gameboy flash cart. You can also use this to to make a 4MB cart out of cheaper 2MB chips.

I'm not going to explain the basics for this flash cart, just how this works and the benefits of it. If you are looking at this as your first flash cart, then I'd recommend you look at one of my other projects first and make 20 of them. Then come back. This is one of the most difficult flash carts to build.

I don’t remember if this uses any of HDR footprints, so just in case go check out their own builds on github.

You have all seen how much 4MB flash chips are vs the 2MB flash chips. You can buy 2 2MB chips for less than 1 4MB chip. So why can’t you use them together to make 4MB? Well you can now with a little bit of basic logic. Even with the logic chip it is still cheaper than 1 4MB chip, but the more of these you make, the cheaper each cart works out. The cost is directly between making a 2MB cart and a regular 4MB cart. There is zero downsides or quirks to this, it just works. You will have to use its own FlashGBX profile as it doesn’t auto detect, but that’s it. ~~Maybe Lesserkuma will include even it in a newer version to make it even more seamless.~~ UPDATE! As of V3.30 it is included!

![LK V3 30](https://github.com/sillyhatday/GAMEBOY-MBC5-DUAL-4_8MB/assets/65309612/78d43b0f-2e17-4e5c-9316-7730b43ccd07)

Now 8MB you’re wondering. Well one single official game was released to use all that space (most of it anyway). If you really wish to play Desnha De Go 2, then this is for you. A train simulator fully in Japanese. This obviously requires 2 expensive 4MB flash chips. I guess you really got to want it. On a more serious note, the more accessible an 8MB cartridge is, the more likely people will develop games or ROM hacks for that size of cartridge. For usefulness today though, there are already people making video cartridges/ROMs for the GBC. So doubling the useable space is a huge benefit to those carts.

When building your cartridge you just have to put a solder bridge over the desired 4 or 8MB selection. There is also a version without JLC serial number markings if you wish to pay the extra to have the serial number removed, else you can specify a location and have the serial number hidden under the FRAM.

Also with many 2MB MBC5 games, they don’t require any additional logic to use FRAM. For whatever reason all 4MB ROMs tested required some logic to refresh the precharge on the FRAM.

## Game compatibility
Simply put this cart has the most compatibility of all the cartridges. If you want a cartridge that has the least compromises, then either configuration of this cartridge will do that.

Nearly all Gameboy colour games used this memory mapper. It can address 32KB to 8MB of game storage and 8KB to 128KB of game save storage. This one using all 8MB of game storage and 32KB of save storage, as 95% of the games using this mapper are within that size range. Most 8KB save files should work fine on the 32KB chip also.

It is not suggested to make the 8MB configuration due to the cost vs gain. Only one official game (and unofficial as far as I know) use 8MB. For most people I suggest making the 4MB version as this should work with every MBC5 game except one.

Games that use real time clock functions do not work correctly on this cartridge due to it not having the clock functionality. Most Pokemon games will not work properly on this. They require a MBC3 cartridge.


## BUILD GUIDE

Once more, if you don't know how to solder this sort of thing then you should come back to this later.

![Racomendd](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/815020d6-9d19-4641-8ca3-6ea37c257a56)

Firstly, decide what size cart you want to build and solder the jumper on the cart for the respective size. Then, I would recommend soldering the MBC and demultiplexer chips followed by the LOWER BANK flash chip. UB and LB next to the flash chips stand for UPPER BANK and LOWER BANK.

At this point, flash the cart under "FlashGBX 29F016/32" or "Sillyhatday MBC5-DUAL-FLASH-4/8MB" profile using a 2MB or 4MB ROM, whichever is half the size of the cart you're building. Any bad connections made will be easier to solve now.

Once this is proven working, I'd suggest to solder the UPPER BANK chip. Then, using the profile included in FlashGBX "Sillyhatday MBC5-DUAL-FLASH-4/8MB", flash a 4MB or 8MB ROM. Once that is proven to work 100%, solder on the FRAM and OR gate.

Finally prove that your game saves properly or better, use the RAM stress test under FlashGBX, and you are good to go!

Remember to support Lesser Kuma for their continued hard work in supporting this great hardware with regular updates and bug fixes. Their Kofi is linked at the bottom.

## Parts List

| Part | Quantity |
|------|----------|
| MBC5 | 1 |
| FM18W08 | 1 |
| 74LVC1G139 | 1 |
| 74LVC1G332GW125 | 1 |
| 29F016 or 29F032 | 2 |
| Capacitor 100nF | 5 |
| Resistor 10K | 2 |

You can use a varity of flash chips for this. AM29F016B, MBM29F016, AM29F032, MBM29F033C for example, so long as they have the same pin out.
### Final version in 2x2MB config
![IMG_5658](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/72163434-7865-4c13-bdaa-4ec5b58a38fa)
![IMG_5652](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/7c0b5e94-a9e7-4a41-8f7e-5831737e5a58)

### 2x2MB mode prototype
![SHD Proto](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/5d0126c4-fa22-4488-836b-ad33e03c95ef)

### 2x4MB mode prototype
![JM Prototype](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/d2490f02-4f30-4c4f-aaee-5c836a3d6c7b)

### 3D render of the attached gerbers
![image](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/58a8015d-0c31-4e0b-aa61-b199808d9987)
![image2](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/e59a21e6-7a26-43a1-b3d7-ffb42e88c59d)

Thanks to Jamo for helping test this prototype, Lesserkuma who helped setup FlashGBX and Modded Gameboy Gameboy Club for even giving me the idea in the first place.

### Check them all out below!

https://ko-fi.com/jamo_mods

https://ko-fi.com/lesserkuma

https://ko-fi.com/nataliethenerd

https://ko-fi.com/sillyhatday

https://github.com/lesserkuma

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License. You are able to copy and redistribute the material in any medium or format, as well as remix, transform, or build upon the material for any purpose (even commercial) - but you must give appropriate credit, provide a link to the license, and indicate if any changes were made.

https://discord.gg/moddedgameboyclub
