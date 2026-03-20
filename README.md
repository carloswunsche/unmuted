# Carlos Wunsche — Unmuted Artist Page

This is your Unmuted artist page. It's a small folder of text files that describe your music — your name, bio, albums, and track list. The actual audio files live here too. When a listener adds you on Unmuted, the app reads these files directly and streams your music.

**No coding required.** Everything is done through GitHub's website.

\---

## Your share link

Once this repo is live on GitHub Pages, your Unmuted link will be:

```
https://YOUR\_GITHUB\_USERNAME.github.io/music/artist.json
```

And your listener deep link (what you put in your Instagram bio) will be:

```
https://unmuted.app/add#https://YOUR\_GITHUB\_USERNAME.github.io/music/artist.json
```

Replace `YOUR\_GITHUB\_USERNAME` with your actual GitHub username.

\---

## Folder structure

```
music/
│
├── artist.json        ← Your profile (name, bio, social links)
├── avatar.jpg         ← Your profile photo
│
└── singles/
    ├── singles.json   ← Your singles tracklist
    ├── cover.jpg      ← Cover art for your singles
    ├── 01-your-first-song.mp3
    └── 02-another-song.mp3
```

\---

## Step 1 — Set up GitHub Pages

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click the **+** button in the top right → **New repository**
3. Name it exactly: `music`
4. Make sure it's set to **Public**
5. Click **Create repository**
6. Upload all these files by dragging them into the GitHub page
7. Go to **Settings** → **Pages** → under "Branch" select `main` → click **Save**
8. Wait 2–3 minutes. Your page is live! ✅

\---

## Step 2 — Fill in your details

### Update your profile (`artist.json`)

Open `artist.json` and replace the placeholder values:

* `YOUR\_INSTAGRAM\_HANDLE` → e.g. `carloswunsche`
* `YOUR\_YOUTUBE\_HANDLE` → e.g. `carloswunsche`
* `YOUR\_SOUNDCLOUD\_HANDLE` → e.g. `carloswunsche`

To edit on GitHub: click the file → click the pencil icon ✏️ → edit → click **Commit changes**.

### Add your profile photo

* Rename your photo to `avatar.jpg`
* Upload it to the root folder (same level as `artist.json`)
* It should be square, at least 400×400px

\---

## Step 3 — Add your singles

### Upload your audio files

1. Go into the `singles/` folder on GitHub
2. Click **Add file** → **Upload files**
3. Drag your MP3 files in
4. Name them cleanly, no spaces — e.g. `01-midnight-drive.mp3`
5. Click **Commit changes**

> \*\*MP3 is recommended.\*\* WAV files work but are very large and will load slowly for listeners. If you have WAV files, convert them to MP3 first (320kbps is great quality).

### Update the tracklist (`singles/singles.json`)

Open `singles/singles.json` and update it for each song you uploaded:

```json
{
  "title": "Singles",
  "year": 2025,
  "cover": "cover.jpg",
  "tracks": \[
    {
      "title": "Midnight Drive",
      "src": "01-midnight-drive.mp3",
      "duration": 214
    },
    {
      "title": "Glass Room",
      "src": "02-glass-room.mp3",
      "duration": 187
    }
  ]
}
```

* `title` — the song name as listeners will see it
* `src` — the exact filename of your MP3 (must match perfectly, case sensitive)
* `duration` — length of the song in seconds (3:34 = 214 seconds)

### Add cover art

* Rename your cover image to `cover.jpg`
* Upload it to the `singles/` folder
* Square image, at least 500×500px recommended

\---

## Step 4 — Get your share link

Once everything is uploaded and GitHub Pages is enabled, your link is:

```
https://YOUR\_GITHUB\_USERNAME.github.io/carlos-wunsche/artist.json
```

Test it by opening that URL in your browser. You should see your `artist.json` file as text.

Then put this in your Instagram bio, tweet it, or share it anywhere:

```
https://unmuted.app/add#https://YOUR\_GITHUB\_USERNAME.github.io/carlos-wunsche/artist.json
```

\---

## Adding a new single later

1. Upload the new MP3 to the `singles/` folder
2. Open `singles/singles.json` and add a new entry to the `tracks` list
3. Commit — listeners will see it automatically next time they open the app ✅

\---

## Adding a full album later

1. Create a new folder, e.g. `my-first-album/`
2. Add a `album.json` inside it (same format as `singles.json`)
3. Upload your MP3s and cover art into that folder
4. Open `artist.json` and add the new album path to the `albums` list:

```json
"albums": \[
  "singles/singles.json",
  "my-first-album/album.json"
]
```

\---

## Updating anything

Changed your bio? New photo? Fixed a typo in a song title? Just edit the file on GitHub and commit. Changes go live within a few minutes. Listeners get the update automatically — no action needed on their end.

\---

## Need help?

Something not working? The most common issues are:

* **Song won't play** — check that the filename in `singles.json` matches the uploaded file exactly, including uppercase/lowercase
* **Page not found** — GitHub Pages might still be building, wait 5 minutes and try again
* **Link not working in Unmuted** — make sure GitHub Pages is enabled in your repo settings

\---

*Built with* [*Unmuted*](https://unmuted.app) *— free, open, artist-owned music.*

