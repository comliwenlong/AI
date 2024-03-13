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
| mustango <br> (text-to-music) | [1. An 80s driving pop song with heavy drums and synth pads in the background...][1] <br> [2. Cute toy factory theme loop][2] <br> [3. Slow and emotional melody][3] <br> [4. Strong rhythm and energy][4] <br> [5. This is a new age piece. There is a flute playing... ][5]| 情感色彩变化丰富 | 10sec |
| musicLDM <br> (text-to-music) | [1. An 80s driving pop song with heavy drums and synth pads in the background...][6] <br> [2. Cute toy factory theme loop][7] <br> [3. Slow and emotional melody][8] <br> [4. Strong rhythm and energy][9] <br> [5. This is a new age piece. There is a flute playing... ][10] | | 10sec |
| images-to-music | | ---- |---- | |
| musicGen <br> (textAndMusic-to-music) | [1. An 80s driving pop song with heavy drums and synth pads in the background...][11] <br> [2. MusicLDM_Strong rhythm and energy][12] <br> [3. mustango_Strong rhythm and energy][13] | | 15sec |
| musicGen-large | |  |  |  |







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
