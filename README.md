# Text-to-Music
    文本、图片、音乐等都是一种信息传递的载体，其本身都是带有感情色彩。这种不同载体之间所表达的情感是相通。而音乐创作的本身是有难度的，他涉及到旋律、节拍等等。
##  工作内容: 对比几种开源text-to-music的效果
### 开源模型
    1. mustango: 这是一种端到端的文本生成音乐的模型，根据提示语生成对应风格的音乐。该模型是基于diffusion构架
    2. musicLDM
    3. images-to-music
    4. musicGen
### 选择几个不同风格的提示词作为文本
    几种不同风格的提示词
    1. This is a new age piece. There is a flute playing the main melody with a lot of staccato notes. The rhythmic background consists of a medium tempo electronic drum beat with percussive elements all over the spectrum. There is a playful atmosphere to the piece. This piece can be used in the soundtrack of a children's TV show or an advertisement jingle
    2. Cute toy factory theme loop
    3. Slow and emotional melody
    4. Strong rhythm and energy
    5. An 80s driving pop song with heavy drums and synth pads in the background
    6. Liszt is the most important musician in the history of European music and one of the outstanding representatives of the European Romantic School. He has his own unique style in terms of music creation and aesthetic characteristics. His music style is unrestrained, passionate and virtuosic, with rich and active musical ideas. He strives to create sound effects with a full orchestral nature, opening a new page for piano solos.
    7. A tranquil piano melody with gentle strings and woodwinds, complemented by the sound of nature - bird songs and rustling leaves. The tempo is slow and soothing, with occasional crescendos that capture the majesty of the mountains. 

| Model | Generate Music | Effect | time of genMusic | main tech|
| ---- | ---- | ---- | ---- | ---- |
| mustango <br> (text-to-music) | [1. An 80s driving pop song with heavy drums and synth pads in the background...][1] <br> [2. Cute toy factory theme loop][2] <br> [3. Slow and emotional melody][3] <br> [4. Strong rhythm and energy][4] <br> [5. This is a new age piece. There is a flute playing... ][5]| 倾向于生成节奏欢快的乐曲 | 10sec |
| musicLDM <br> (text-to-music) | [1. An 80s driving pop song with heavy drums and synth pads in the background...][6] <br> [2. Cute toy factory theme loop][7] <br> [3. Slow and emotional melody][8] <br> [4. Strong rhythm and energy][9] <br> [5. This is a new age piece. There is a flute playing... ][10] | 能够生成多样化风格的音乐 | 10sec |
| images-to-music | 这一个单独在下一个模块中列出 |
| musicGen <br> (textAndMusic-to-music) | [1. An 80s driving pop song with heavy drums and synth pads in the background...][11] <br> [2. MusicLDM_Strong rhythm and energy][12] <br> [3. mustango_Strong rhythm and energy][13] |  | 15sec |
| musicGen-large | [1. A tranquil piano melody with gentle strings and woodwinds, complemented by the sound of nature - bird songs and rustling leaves. The tempo is slow and soothing, with occasional crescendos that capture the majesty of the mountains][14] <br> [2. Strong rhythm and energy][15] <br> [3. lo-fi music with a soothing melody][16] |  | 29sec |  |

### image-to-music
| images | Generate Music | Effect | time of genMusic | main tech|
| ---- | ---- | ---- | ---- | ---- |
| <img src="https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/ocean%20poet/ocean_poet.jpeg">| [1. MAGNet:A dramatic piano melody with crashing cymbals and ominous strings, building tension as the storm approaches][17] <br> [2. musicGen:A dramatic orchestral piece with ominous strings, crashing percussion, and a solitary woodwind melody, conveying a sense of foreboding and introspection as nature's wrath approaches][18] <br> [3. Riffusion:A haunting melody with ethereal strings and a mournful woodwind, building in intensity as the tempo quickens and thunderous percussion rolls in, evoking the ominous mood of a coming storm at sea][19] <br> [4. audioLDM-2: haunting melody played by a solo violin and cello, accompanied by soft piano chords and distant crashing waves, evokes a sense of introspection and melancholy in this moody scene][20] <br> [5. mustango:A brooding piano melody with ominous strings and gentle percussion, building in intensity as the storm approaches, capturing the raw emotions of introspection and vulnerability][21]|
|<img src="https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/peacful%20nature/peaceful%20nature.jpeg" >| [1. MAGNet:A dramatic piano melody with crashing cymbals and ominous strings, building tension as the storm approaches][17] <br> [2. musicGen:A dramatic orchestral piece with ominous strings, crashing percussion, and a solitary woodwind melody, conveying a sense of foreboding and introspection as nature's wrath approaches][18] <br> [3. Riffusion:A haunting melody with ethereal strings and a mournful woodwind, building in intensity as the tempo quickens and thunderous percussion rolls in, evoking the ominous mood of a coming storm at sea][19] <br> [4. audioLDM-2: haunting melody played by a solo violin and cello, accompanied by soft piano chords and distant crashing waves, evokes a sense of introspection and melancholy in this moody scene][20] <br> [5. mustango:A brooding piano melody with ominous strings and gentle percussion, building in intensity as the storm approaches, capturing the raw emotions of introspection and vulnerability][21]|


[1]: https://github.com/comliwenlong/AI/blob/main/genMusic/mustango_An%2080s%20driving%20pop%20song%20with%20heavy%20drums%20and%20synth%20pads%20in%20the%20background_10sec.wav
[2]: https://github.com/comliwenlong/AI/blob/main/genMusic/mustango_Cute%20toy%20factory%20theme%20loop_10sec.wav
[3]: https://github.com/comliwenlong/AI/blob/main/genMusic/mustango_Slow%20and%20emotional%20melody_10sec.wav
[4]: https://github.com/comliwenlong/AI/blob/main/genMusic/mustango_Strong%20rhythm%20and%20energy_10sec.wav
[5]: https://github.com/comliwenlong/AI/blob/main/genMusic/mustango_This%20is%20a%20new%20age%20piece.%20There%20is%20a%20flute%20playing%20_10sec.wav
[6]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicLDM_An%2080s%20driving%20pop%20song%20with%20heavy%20drums%20and%20synth%20pads%20in%20the%20background_10sec.wav
[7]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicLDM_Cute%20toy%20factory%20theme%20loop_10sec.wav
[8]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicLDM_Slow%20and%20emotional%20melody_10sec.wav
[9]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicLDM_Strong%20rhythm%20and%20energy_10sec.wav
[10]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicLDM_This%20is%20a%20new%20age%20piece.%20There%20is%20a%20flute%20playing%20the%20main%20melody%20with%20a%20lot%20of%20staccato%20notes.%20The%20rhythmic%20background%20consists%20of%20a%20medium%20tempo%20electronic%20drum%20beat%20with%20percussive%20elements%20all%20over%20the%20spectrum.%20_10sec.wav
[11]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicGen_An%2080s%20driving%20pop%20song%20with%20heavy%20drums%20and%20synth%20pads%20in%20the%20background_15sec.mp4
[12]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicGen_MusicLDM_Strong%20rhythm%20and%20energy_15sec.mp4
[13]: https://github.com/comliwenlong/AI/blob/main/genMusic/MusicGen_mustango_Strong%20rhythm%20and%20energy_15sec.mp4
[14]: https://github.com/comliwenlong/AI/blob/main/genMusic/musicGen-large/musicgen_A%20tranquil%20piano%20melody%20with%20gentle%20strings%20and%20woodwinds%2C%20complemented%20by%20the%20sound%20of%20nature%20-%20bird%20songs%20and%20rustling%20leaves.%20The%20tempo%20is%20slow%20and%20soothing%2C%20with%20occasional%20crescendos%20that%20capture%20the%20majesty%20of%20the%20mountains.%20wav
[15]: https://github.com/comliwenlong/AI/blob/main/genMusic/musicGen-large/musicgen_Strong%20rhythm%20and%20energy.wav
[16]: https://github.com/comliwenlong/AI/blob/main/genMusic/musicGen-large/musicgen_lo-fi%20music%20with%20a%20soothing%20melody.wav

[17]: https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/ocean%20poet/MAGNet_%22A%20dramatic%20piano%20melody%20with%20crashing%20cymbals%20and%20ominous%20strings%2C%20building%20tension%20as%20the%20storm%20approaches%22.wav
[18]: https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/ocean%20poet/MusicGen_ocean_poet_%22A%20dramatic%20orchestral%20piece%20with%20ominous%20strings%2C%20crashing%20percussion%2C%20and%20a%20solitary%20woodwind%20melody%2C%20conveying%20a%20sense%20of%20foreboding%20and%20introspection%20as%20nature's%20wrath%20approaches%22.wav
[19]: https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/ocean%20poet/Riffusion_%22A%20haunting%20melody%20with%20ethereal%20strings%20and%20a%20mournful%20woodwind%2C%20building%20in%20intensity%20as%20the%20tempo%20quickens%20and%20thunderous%20percussion%20rolls%20in%2C%20evoking%20the%20ominous%20mood%20of%20a%20coming%20storm%20at%20sea%22.wav
[20]: https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/ocean%20poet/musicLDM_%22A%20haunting%20melody%20played%20by%20a%20solo%20violin%20and%20cello%2C%20accompanied%20by%20soft%20piano%20chords%20and%20distant%20craAudioLDM-2_shing%20waves%2C%20evokes%20a%20sense%20of%20introspection%20and%20melancholy%20in%20this%20moody%20scene.%22.wav
[21]: https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/ocean%20poet/mustango_%22A%20brooding%20piano%20melody%20with%20ominous%20strings%20and%20gentle%20percussion%2C%20building%20in%20intensity%20as%20the%20storm%20approaches%2C%20capturing%20the%20raw%20emotions%20of%20introspection%20and%20vulnerability.%22.wav

[22]:https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/peacful%20nature/MAGNet_%22A%20tranquil%20piano%20melody%20with%20gentle%20strings%20and%20woodwinds%2C%20complemented%20by%20the%20sound%20of%20nature%20-%20bird%20songs%20and%20rustling%20leaves.%20The%20tempo%20is%20slow%20and%20soothing%2C%20with%20occasional%20crescendos%20that%20capture%20the%20majesty%20of%20the%20mountains.%20.wav
[23]:https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/peacful%20nature/MusicGen_%22A%20gentle%20piano%20melody%20with%20soft%20string%20and%20woodwind%20accompaniment%2C%20mimicking%20the%20tranquility%20of%20the%20lake.%20The%20sound%20of%20bird%20calls%20is%20gently%20woven%20into%20the%20background%2C%20adding%20a%20touch%20of%20nature.%20The%20music%20swells%20as%20the%20mountains%20come%20into%20view.wav
[24]:https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/peacful%20nature/Riffusion_%22A%20gentle%20piano%20melody%20with%20soft%20strings%20and%20woodwinds%2C%20accompanied%20by%20the%20soothing%20sound%20of%20a%20waterfall%20and%20bird%20song%2C%20creates%20a%20tranquil%20and%20peaceful%20ambiance%2C%20reminiscent%20of%20a%20serene%20mountain%20lake%20nestled%20in%20a%20lush%20forest%22.wav
[25]:https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/peacful%20nature/AudioLDM-2_%22A%20calming%20piano%20melody%20with%20gentle%20string%20harmonies%2C%20complemented%20by%20the%20tranquil%20sounds%20of%20bird%20chirps%20and%20flowing%20water%2C%20evoking%20a%20peaceful%20and%20serene%20atmosphere%20reminiscent%20of%20a%20tranquil%20mountain%20lake%22.wav
[26]:https://github.com/comliwenlong/AI/blob/main/genMusic/image-to-music/peacful%20nature/mustango_%22A%20gentle%20piano%20melody%20with%20soft%20string%20harmonies%2C%20accompanied%20by%20the%20sound%20of%20bird%20calls%20and%20the%20gentle%20lapping%20of%20waves%2C%20creates%20a%20peaceful%20and%20serene%20atmosphere%20inspired%20by%20a%20tranquil%20lake%20surrounded%20by%20mountains%20and%20trees_10sec.wav






