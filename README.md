# Growcastle Save Editor / CastleForge

> *"Somebody else will do it at some point, so I may as well do it now."*

**A message to the Dev:** If you want me to cancel working on this project, I am willing to do that, and also help improve security on your game. Just contact the public email on my GitHub profile, and preferably, use your raongames.com email. Until then, here we are.

> [!NOTE]  
> **Release Status:** I am going to release this in a few days. This will either be the climax of GrowCastle or the most anti-climactic thing to exist. Pray it works. (Heavily WIP).

---

## 🛠️ Features

Edit your Growcastle save file to your heart's content. Currently supported edits include:
* **Currencies:** Gold and Gems.
* **Treasures:** Contracts, dark crystals, and stones.
* **Items:** Modify item ranks (B, A, S, etc.), item types (hammer, sword, etc.), and their specific buffs.
* **Misc Values:** Auto-battle, macro detector (placed in the treasure tab, because I said so).
* **The Proto Editor:** You can edit literally *any* value, as long as you know how it works!

### 🚧 Work In Progress (WIP)
* Map editing
* Skill tree editing
* Making this work seamlessly on non-rooted devices

---

## ❓ Q&A

**Why does this project exist?**
> Because the developer just doesn't care about the game! Neither should you.

**Why is it so unfinished?**
> I took an insult personally on the internet and released this early.

**Can I get the Growcastle decompilation pls pls?**
> I know some of you are skids, but I literally posted a guide below. Do it yourself.

**Did you SkidGPT this?**
> Of course, the entire Python file was originally made using Claude!  
> ...Not anymore, actually. I removed all the documentation because it made the file nearly double in length.

**Why do you type like that?**
> get out of my repo

---

## ⚙️ Prerequisites

### Setting up the Editor
* **Python:** Preferably `3.12.4` (the version used to build this).
* **IDE:** VSCode is highly recommended to make your life easier for this tutorial.

### Getting Your Game Save (Rooted)
* A rooted Android device (probably works on a jailbroken Apple device, but you'll have to find the file paths yourself).
* **ZArchiver** with access to: `/data/data/com.raongames.growcastle/data.dat`
* *Emulator Note:* On an emulator, use your shared folder. By default, for LDPlayer9, the Windows and Android folders are located at:
    * Windows: `C:\Users\%USERNAME%\Documents\XuanZhi9\Pictures`
    * Android: `/mnt/shared/pictures`

### Getting Your Game Save (Unrooted)
* Work in progress (pog).

### Decompiling the Game
If you're going to dig into the code, you'll need these tools:
* [IL2CPPDumper GUI](https://github.com/Perfare/Il2CppDumper) (The *normal* IL2CPPDumper will NOT work).
* **Ghidra** or **IDA**. (I am providing guides for Ghidra. If you use IDA, you're on your own).
* Any emulator (like LDPlayer9) OR a rooted Android device (unless your device is buns af).
* **ZArchiver** installed on the emulator/device.

---

## 📖 Decompilation Tutorial

I am not going to distribute a Growcastle decompilation, but I can legally give out the steps. *All steps up to 18 are working as of APK version 1.50.14.*

1. **Get the APKs:** Download Growcastle. Alternatively, download the [APKs here](https://mega.nz/file/cKdQmCpR#YMJKJv20M7lRfpwKAgNyyu9uoV8SALVztLfs4DRYjEs) and unzip them (passwords in credits), then skip to Step 7.
2. Open **ZArchiver** on your device/emulator.
3. Grab the `base.APK` and `split_config.arm64_v8a.APK` files from `/data/app/com.raongames.growcastle-xxxx`. *(Note: the `-xxxx` is a random base64 string and will differ).*
4. Close ZArchiver on your emulator, and drag the APKs onto your PC.
5. Rename the `.APK` file extensions to `.ZIP`.
6. Extract the newly renamed ZIP files.
7. Open the extracted `base` folder.
8. Navigate to: `assets/bin/Data/Managed/Metadata`.
9. Steal the `global-metadata.dat` file, put it into a new folder on your PC, and name that folder whatever you want.
10. Now go back to the `split_config.arm64_v8a` folder you unzipped earlier.
11. Navigate to: `lib/arm64-v8a`.
12. Steal `libil2cpp.so` and put it in the same folder as your `global-metadata.dat`.
13. Open **IL2CPPDumper GUI**, and load both the `.dat` and `.so` files.
14. Now you get banned for spamming 'ez' because it's actually tough, but it worked fr fr.
15. If you're stuck here, you'll need to find another tutorial. Ghidra is honestly complex, and I can't help you past this point.
16. **[Recommended Ghidra Tutorial](https://gist.github.com/BadMagic100/47096cbcf64ec0509cf75d48cfbdaea5)**

---

## 🤝 Contributing

Chances are, I will rarely check this account. Please report issues, or better yet, make a fix yourself and submit a pull request!

## 🏆 Credits

* **BedroomBest5286** (Reddit): Their username is the password for the 7zipped APKs. I bet he will enjoy this!
* **Myself:** Thanks, me.
* **You:** In your skid-worthy glory (or lack thereof).
* **The GrowCastle Developer:** Last, but still noteworthy. Just stop ignoring the community.

## 📄 License

### MIT License
More free and editable software!
