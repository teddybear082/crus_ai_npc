# crus-ai-npc
 A free artificial intelligence NPC mod for Cruelty Squad powered by whisper.cpp , convai.com and gpt4all


**Unzip this release into a folder called "crus_ai_npc" in your mods directory: https://github.com/teddybear082/crus_ai_npc/releases/download/crus-ai-npc/crus_ai_npc.zip** It is **essential** that the folder be called exactly **crus_ai_npc** because the path to certain files in the folder is hard coded in the mod's files.  If you do not name the folder that likely the mod will not work.  There should be exactly one folder inside of your mods folder called "crus_ai_npc" and in that should be the mod.zip, mod.json and other files from this release.  There should not be two crus_ai_npc folders.


**You already need to have crus modloader or crus-vr-modloader installed to install this mod.**

***Either:***

(1) create an account at convai.com and create the character you want to talk to, and copy your api key and character id from convai into the config file (ai_npc.cfg) in the designated fields and make sure ai_brain_choice="convai" OR

(2) (EXPERIMENTAL) download this large language model and put it into the mod folder: https://gpt4all.io/models/ggml-gpt4all-j-v1.3-groovy.bin to use local AI generated responses. You can modify "prompt_template.txt" to create a different character. You can change the model settings in gpt4all.json (see readme). Make sure ai_brain_choice="gpt4all" in the ai_npc.cfg.

***If you want to use voice responses, you can either:***

(1) use convai and in the ai_npc.cfg file put true instead of false for use_convai_voice (if you are using convai.com for the AI brain) OR

(2) install the separate crus-text-to-speech mod found here: https://crus.cc/mod/crus-text-to-speech/

Make sure you have a microphone connected!!

## In Game Use

Once you have installed the mod, go to Pharma and walk to the left corner of the building outside.  To start chatting with Gorbino, interact with him.  He will tell you he is listening.  Say whatever you want into your mic, then interact with him again.  He will repeat what you said so you know if your microphone input was picked up correctly.  He will then respond.

You do need to speak English to use this mod.


## Advanced Options

**Convai.com**

Convai.com is a website to create AI NPCs.  There is a very generous free tier, so while you have to create an account you don't need a credit card or anything.  When creating an account on convai.com, you can also upload background information to your character.  I have created a folder in this release called "crus-text-info."  You can use those files if you want to load the knowledge you want to your character.  I got all of the information from https://crueltysquad.fandom.com/wiki/Cruelty_Squad_Wiki

Once you create your character, grab your API key and character code from the website and put them into the convai_api_key= and convai_character_id= fields of the ai_npc.cfg.  It's possible but untested that using your own API key but the character id I have already provided in the ai_npc.cfg will link you directly to the character I have created on convai, but I'm not sure. You could try this first and see if it works. If not, create your own character to your liking!

When you create your character you can also choose the voice you want your character to have. If you want your character to use that voice, put **true** instead of **false** in the ai_npc.cfg in the line for use_convai_voice.

When using the convai.com option make sure the line in ai_npc.cfg says **ai_brain_choice="convai"**.

**GPT4All**

This is a free, purely local, option for AI generated responses.  It also uses the CPU and ram on your computer instead of going out to the internet for information.  As a result, it is a bit slower, more experiemental and unpredictable and not quite as easy to fine tune as convai.com characters. Some older computers could have issues running it and the game at the same time. Sometimes the NPC does not respond. 

**To use the gpt4all option**, you will need to download the large language model you want to use.  Note that each one has different strengths and weaknesses and different models may require different prompt template formats (found in the prompt_template.txt file).  You can learn more about gpt4all here: https://gpt4all.io/index.html?s=09  The model I recommend starting with as it is quickest and a good balance of speed and responses (when it works) is https://gpt4all.io/models/ggml-gpt4all-j-v1.3-groovy.bin  Download that and put it into the crus-ai-npc mod folder.  

**If you want to use a different model**, you can find compatible models and model descriptions on that same gpt4all.io website under "model explorer" section.  If you want to try another model, download it, put it into the crus-ai-npc folder, and change the gpt4all_llm_model= line in the ai_npc.cfg file to the name of the new model you downloaded.  For example, if you downloaded the **"snoozy"** model, you would change that line to **gpt4all_llm_model="ggml-gpt4all-l13b-snoozy.bin"**.

**To change your character's personality** when using GPT4All, you can change the text in **prompt_template.txt**.  Note that different models need different prompt styles. You need to research the best style for yourself / trial and error.

**To change other gpt4all options**, you can edit the **gpt4all.json**.  More information about those options are on gpt4all's website and kuvaus's LlamaGPTJ-chat github.  Look at the "Detailed Command List" on this page for more: https://github.com/kuvaus/LlamaGPTJ-chat. They are also common GPT type options so google is your friend.

When using the GPT4All option, make sure the line in ai_npc.cfg says **ai_brain_choice="gpt4all"**.

## Credits

This mod uses:

Whisper.cpp : https://github.com/ggerganov/whisper.cpp  

GPT4All: https://gpt4all.io/index.html?s=09

LlamaGPTJ-chat: https://github.com/kuvaus/LlamaGPTJ-chat

Convai: https://www.convai.com/  (their support to me as someone creating free stuff with a not officially supported engine, Godot, has been truly remarkable!)

Thank you so much to all of the above for creating such technology!!  '

All licenses for the above are as reflected on their websites/github; nothing contained here is intended to modify their licenses.
