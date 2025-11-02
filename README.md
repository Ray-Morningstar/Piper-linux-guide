# Piper-linux-guide
Guide to install and run piper on linux 

It is my first time making a github repository/documentation/guide soo dont expect it to look prety.

I eventually will finish making a video to show visually all the steps to take etc, however it is very time consuming and i am out of practice with my video editor even if i still have the muscle memory,soo i will add it later to the repository

The comand list to run and download list on cronological order for those who just want to control c control v without a 10 minet yap, do not close terminal or move position unless specified, it may only work on linux mint, reading or watching 
the yapping is recomended but not obligatory>

Run !uname -m!

>Install piper with same infra-structure/numbers and letters and the end<                          >https://github.com/rhasspy/piper/releases/tag/2023.11.14-2<

Chose a voice and download its onnx and onnx.json files from this or other place                   >https://huggingface.co/rhasspy/piper-voices/tree/main<

Download this python script for control piper settings                                             >https://codeberg.org/Hoomelab/Piper_TTS_Banco_de_Voz/src/branch/main/main.py<

Go to root then make folder !piper-tts! 

Put all inside and decompress piper.tar, then delete it

Make folder !piper-voices! and put inside onnx and onnx.json of voice

Check python version bigger or equal to 3.9, if not download or compile from source code

Go to !piper-tts! folder, open in terminal

Check dependency !python3,12-venv! present, if not run !apt install python3,12-venv! or manually download it

Run !python3 -m venv venv!

Run !source venv/bin/activate!

Run !pip install pydub! or manually download

Run !sudo apt install ffmpeg! or manually download

Check if alsa-utils present, if not run !sudo apt install alsa-utils! or manually download

Open visual studio code or any text coding aplication, then edit python script

Row 25 atach path to !piper-voices!, row 51 atach path to piper binary inside piper folder !piper/piper!

Row 53 to 56 voice settings, modify when set up completed to your taste

Save modifications and go back to terminal

Run !nano texto.txt!

Write a 20 word sentence for test, control+X, and save(changes with pc language, you can read under) (this is test input for piper, only modify test inside do not delete)

Run !python main,py!

Piper outputs number of voices and name, chose wich tiping number on theyr left then enter

Lower your volume or you will probably go deaf

Now will processes and output audio file, you WILL hear it.

Decide if save or not audio file on a folder automatically made inside !piper-tts!



For closing>

A> run !deactivate! 

B> close terminal and kill all programs running



Comand list For start up (like after turning pc on)

Open terminal on root
Run !cd piper-tts!
Run !source venv/bin/activate!
Run !python main.py!

As mentioned before, row 53 to 56 of !main.py! pythin script are settings for your selected voice, print one audio for test, then change values slowly and save, repeat making piper process the same text for tuning talking speed or others.  

Thats prety much it, now the 20 minet yaping.



I will cover. stuff necesary to use, how to set up, basic use knowledge.

I do this becouse the only guide i found of this was on spanish and i am not mexican, this is mostly a translated version, sources at the end

First we need to know wich version of piper download depending of your linux version.

Soo terminal, and type !uname -m!

Myne is, x86_64, soo i would go to piper official github page, and download that one. !https://github.com/rhasspy/piper/releases/tag/2023.11.14-2!

Now we want to get the voice that reads the text, there are diferent places to get them from, but you have to make sure that they are free to use for everyone, i got one from here. !https://huggingface.co/rhasspy/piper-voices/tree/main!

I got the one i use from here and there is a lot to chose from, soo dont rush it and try to find the one you prefer.

When you do, you have to download this 2 files inside of the voice folder, !onnx.! and !onnx.json! both are necesary.

Now we download this python file, it is like the settings piper uses, i decided to keep the one from the mexican tutorial since it is easier to find where the important stuff is. 

Now you can either put everything where you want on your pc or doit exactly as writen, i recomend to copy it by the letter first, so you can test if it works, and later modify everything if you want.

Go to your home directory and make a folder called !piper-tts!.

Now go inside and put everything into it, once that is done, decompress the !piper.tar! and then delete it. now make another folder without changing place. called. !piper-voices! and put the 2 files of the voice you chose inside.

Now that we have everything on place, we need to check our pc python version, go to your terminal and type !python3 --version! mine is 3,12,3. piper only works if it is the 3,9 or superior.

If it isnt the same or over 3,9. if avaliable download it from terminal, if not you will need to compile from the source code (watever that means).

After cheking that, go to the !piper-tts! folder, right click and open in terminal, or access it using the cd command and name of folder from your home directory, example> !cd piper-tts!.

Check if you have the dependency !python3,12-venv! if not or you dont know how to check, you can try install it with !apt install python3,12-venv!.

After that write !python3 -m venv venv! this lets us use piper without conecting outside of the pc, after it is done you need to open it from terminal with this command, from that exact place !source venv/bin/activate! if you did it propelly
at the left of the next terminal text you get, you should see, !venv! on the left side of it.

From there and only there, we need to download the necesary librarys, try use !pip install pydub! this manages the audios, now we download the dependency it needs,
try use !sudo apt install ffmpeg! if it dosent work you may need to download it from somewhere else.

And finally the last one, we download aplay. for play the audios on linux, try use !sudo apt install alsa-utils! it may be already downloaded depending on your linux version/distribution.

Those are all the install and place steps, the last one is configurate the piper settings file, soo it knows where everything is, i recomend you use >visual studio code<. or another text coding aplication of your chosing.

You want to connect where the voices folder is and where the piper binary is, open the main.py script and>

Go to row 25 and write the path to !piper-voices!

<img width="570" height="32" alt="image" src="https://github.com/user-attachments/assets/e77a7ad6-4612-4f00-8913-cd09a77a80db" />

Now go to row 51 and atach the path to piper binary inside !piper! folder, how it should look> !piper/piper!

<img width="536" height="42" alt="image" src="https://github.com/user-attachments/assets/8407b09f-5718-4de8-b284-3ac97142833f" />

Now we make a text file from the terminal using !nano texto.txt! write something small inside, and then save with !control+x! and save the changes. this file is where u write all u want piper to say, save it each time before operating piper
and do not delete it.

After doing all this configuration, write !python main.py! this will start piper,
if everything was done properly, it will let you chose the voice to use, for this type the number it has on its left, and press enter, be carefull becouse it will automatically start process and then say what u typed on the text file
and it is at full system volume by default.

After piper is done procesing and saying each verse, it will ask if you want or no to save the audio, they will be saved on a audio folder piper makes automatically, it will ask you and you will have to chose like the number before and press 
enter.

When its done with all the verses u wrote, piper will turn off automatically, for turning off the offline conexion of piper either type !deactivate! or just close the terminal killing all runing programs inside it.

Now if you want to turn piper from 0 like if your pc turned on, just go to your home/root on terminal, and type the next commands in order> !cd piper-tts!, !source venv/bin/activate!, !python main.py!.

For modify your voice settings like voice speed, separation, or others, go to the pythin scrypt and modify slowly the values from row 53 to 56, you will probably need to test it more than once.

I recomend you write down the necesary commands for start up from 0, in case you may forget them, on a text file somewhere easy to find.

The script can be modified for change places of folders, name of files to run etc, but it is a optional step, i actually have it like this and it dosent make problems, soo it depends if you want to move it to somewhere harder to access, change
name of things like the python script or similar.

This is the end of the guide for download and operate piper from linux, if you are from windows, just follow a-lillian documentation page, since it is already on english, they also have avaliable a custom version of a program >Curses< 
that can be used like a UI for piper, while also generating subtitles for streaming or recording purposes, and also giving the option to record your own audio, and automatically get it writen into text, and then said by piper.
!https://github.com/a-lilian/STTTS-tutorial/blob/main/How%20to%20talk%20like%20a_lilian.md!

Sources or mentioned>

piper repository> !https://github.com/rhasspy/piper/releases!

voice repository i used/linked> !https://huggingface.co/rhasspy/piper-voices/tree/main!

hoomelab documentation on spanish !https://codeberg.org/Hoomelab/Piper_TTS_Banco_de_Voz< diferent website!

a-lillian windows documentation !https://github.com/a-lilian/STTTS-tutorial/blob/main/How%20to%20talk%20like%20a_lilian.md!
