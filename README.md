### Liberty Prime

I saw that Think Geek was taking pre-orders for a  [Liberty Prime](https://www.thinkgeek.com/product/ktgl/) statue and I kind of had to have one. I was a bit sad to see that it doesn't come equipped with audio to broadcast the amazing on-liners that make Liberty Prime the star of Fallout 3 (and 4, potentially). At the urging of my friend I made an arduino routine to play Liberty Prime quotes. Here are a few of my favorites:

- "Patriotism Subroutine, engaged"
- "Democracy is non-negotiable"
- "Obstructions: sand, gravel, and communism"
- "Death is a preferrable alternative to communism"

There is a [youtube channel](https://www.youtube.com/watch?v=GzXAbm55DOE) with a lot of them. I pulled the audio out using this [site](https://www.onlinevideoconverter.com/mp3-converter) and then split the nin minute long file into 58 smalled clips using [Audacity](https://www.audacityteam.org/) and `Analyze` > `Silence finder`. Then `Export` > `Export multiple`.

I followed this [tutorial](https://circuitdigest.com/microcontroller-projects/arduino-audio-music-player) for setting up the arduino.


Must convert the file names to format 8.3, with the structure `NAME001.EXT` where `NAME001` is an 8 character string and `.EXT` is a 3 character extension. The file names start with the structure `Liberty_Prime-01.wav`, which is too long. Renames with this command: `rename 's/.+/our $i; sprintf("LP%d.wav", 1+$i++)/e' *`
