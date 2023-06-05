# GAMEBOY-FLASHCART-MBC5-DUAL-FLASH-4-8MB
The first working 8MB Gameboy flash cart as far as I know. You can also use this to to make a 4MB cart out of cheaper 2MB chips.

I'm not going to explain the basics for this flash cart, just how this works and the benefits of it. If you are looking at this as your first flash cart, then I'd recommend you look at one of my other projects first and make 20 of them. Then come back. This is one of the most difficult flash carts to build.

I don’t remember if this uses any of HDR footprints, so just in case go check out their own builds on github.

You have all seen how much 4MB flash chips are vs the 2MB flash chips. You can buy 2 2MB chips for less than 1 4MB chip. So why can’t you use them together to make 4MB? Well you can now with a little bit of basic logic. Even with the logic chip it is still cheaper than 1 4MB chip, but the more of these you make, the cheaper each cart works out. The cost is directly between making a 2MB cart and a regular 4MB cart. There is zero downsides or quirks to this, it just works. You will have to use its own FlashGBX profile as it doesn’t auto detect, but that’s it. Maybe Lesserkuma will include even it in a newer version to make it even more seamless.

Now 8MB you’re wondering. Well one single official game was released to use all that space (most of it anyway). If you really wish to play Desnha De Go 2, then this is for you. A train simulator fully in Japanese. This obviously requires 2 expensive 4MB flash chips. I guess you really got to want it. On a more serious note, the more accessible an 8MB cartridge is, the more likely people will develop games or ROM hacks for that size of cartridge. For usefulness today though, there are already people making video cartridges/ROMs for the GBC. So doubling the useable space is a huge benefit to those carts.

When building your cartridge you just have to put a solder bridge over the desired 4 or 8MB selection.

Also with many 2MB MBC5 games, they don’t require any additional logic to use FRAM. For whatever reason all 4MB ROMs tested required some logic to refresh the precharge on the FRAM.

Parts List

| Part | Quantity |
|------|----------|
| MBC5 | 1 |
| FM18W08 | 1 |
| 74LVC1G139 | 1 |
| 74LVC1G332GW125 | 1 |
| 29F016 or 29F032 | 2 |
| C 100nF | 5 |
| R 10K | 2 |
