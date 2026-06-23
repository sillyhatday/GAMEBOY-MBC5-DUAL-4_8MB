# GAMEBOY-MBC5-DUAL-4/8MB

## 🟦 Introduction

A working 8MB Gameboy flash cart. It uses 2 flash chips to double the ROM storage space. It can be configured for 2x2MB or 2x4MB for 4MB or 8MB respectively.

If you are looking at this as your first flash cart, then I'd recommend you look at one of my other projects first, then make 20 of them. This is one of the more difficult flash carts to build.

You have all seen how much 4MB flash chips are vs the 2MB flash chips. You can buy two 2MB chips for less than one 4MB chip. So why can’t you use them together to make 4MB? Well you can now with a little bit of basic logic. Even with the logic chip it is still cheaper than one 4MB chip, but the more of these you make, the cheaper each cart works out.

The cost per cart is directly between making an ordinary 2MB cart and a 4MB cart. There is zero downsides or quirks to this, it just works. You will have to use its own FlashGBX profile as it doesn’t auto detect, but that’s it. ~~Maybe Lesserkuma will include even it in a newer version to make it even more seamless.~~ 

>[!NOTE]
>UPDATE! As of V3.30 it is included!

![LK V3 30](https://github.com/sillyhatday/GAMEBOY-MBC5-DUAL-4_8MB/assets/65309612/78d43b0f-2e17-4e5c-9316-7730b43ccd07)

Only one game was ever released to use all 8MB. I imagine the cart cost and coding time to track so many ROM banks wasn't worth it to everyone. So if you really wish to play Desnha De Go 2, then this is for you. A Japanese train simulator. This obviously requires 2 expensive 4MB flash chips. I guess you really got to want it. On a more serious note, the more accessible an 8MB cartridge is, the more likely people will develop games or ROM hacks for that size of cartridge. I think the main use for this right now is the video ROMs out there.

>[!TIP]
>When building your cartridge you just have to put a solder bridge over the desired 4 or 8MB jumper. Also many <2MB MBC5 games, they don’t require the additional glue logic for FRAM. For whatever reason, all 4MB ROMs tested require some extra glue logic.

## Game compatibility
Simply put this cart has the best compatibility of all my cartridges. If you want a cartridge that has the least compromises, this is the one.

Nearly all Gameboy colour games used this memory mapper. It can address 32KB to 8MB of game storage and 8KB to 128KB of game save storage. This one can use all 8MB of game storage and only 32KB of save storage. Most 8KB save files should work fine on the 32KB chip and I think only LSDJ uses 128KB of save storage.

Games that use real time clock functions do not work on this cartridge due to it not having the clock functionality. Most later Pokemon games will not work properly on this. They require a MBC3 cartridge.

>[!WARNING]
>Once more, if you don't know how to solder this sort of thing then you should come back to this later. Don't be mad at me, I don't want you to waste your money.

![Racomendd](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB/assets/65309612/815020d6-9d19-4641-8ca3-6ea37c257a56)

## 🟦 Parts List

>[!IMPORTANT]
>When ordering cartridge PCBs, make sure to choose 0.8mm thickness and gold plating. <br>
>Order FRAM from Aliexpress & eBay at your own risk, they are known to be ***extremely*** unreliable. <br>

| Part | Quantity |
|------|----------|
| MBC5 | 1 |
| FM18W08 | 1 |
| 74LVC1G139 | 1 |
| 74LVC1G332GW125 | 1 |
| 29F016* | 2 |
| Capacitor 100nF | 5 |
| Resistor 10K | 2 |

*You can use a varity of flash chips for this. AM29F016B, MBM29F016, AM29F032, MBM29F033C for example, so long as they have the same pin out.

>[!NOTE]
>Flash the cartridge with the "Sillyhatday MBC5-DUAL-FLASH-4/8MB" profile in FlashGBX. The regular 4MB profiles will not work.

### Final version in 2x2MB config
<img width="640" height="427" alt="final2x22" src="https://github.com/user-attachments/assets/ea8f6eaf-1742-40cd-8502-5db75928554a" />
<img width="640" height="427" alt="final2x21" src="https://github.com/user-attachments/assets/5db8c64a-6b7f-4c34-8ea7-d89cdab79881" />

### 2x2MB mode prototype
<img width="450" height="800" alt="proto2x2" src="https://github.com/user-attachments/assets/7935de40-722d-4cbf-b1ee-229fb119b3e5" />

### 2x4MB mode prototype
<img width="450" height="600" alt="proto2x4" src="https://github.com/user-attachments/assets/ca661a82-b87c-4b82-9c67-6056b9dce162" />

## 💙 Thanks
Thanks to Jamo for helping test this prototype, Lesserkuma who helped setup FlashGBX and Modded Gameboy Gameboy Club for even giving me the idea in the first place.

## 🩷 Links

🖇️ Bytendo Mods GitHub: https://github.com/bytendomods <br>
🛒 Natalie Shop: https://nataliethenerd.com/ <br>
🤓 Natalie GitHub: https://github.com/natalie-lang/natalie <br>
📱 MGGC Discord: https://discord.gg/moddedgameboyclub

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License. You are able to copy and redistribute the material in any medium or format, as well as remix, transform, or build upon the material for any purpose (even commercial) - but you must give appropriate credit, provide a link to the license, and indicate if any changes were made.
