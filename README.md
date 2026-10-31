# aoost

Alex's corner of the internet: projects, playlists and a wall to draw on.

## Put it live (free, GitHub Pages)

1. Sign in at github.com and create a new **public** repository.
   - Name it `yourusername.github.io` to get the address `https://yourusername.github.io`.
   - Any other name works too and gives `https://yourusername.github.io/repo-name`.
2. In the new repository, click **uploading an existing file**, drag in everything from this folder (`index.html`, `README.md` and the `art`, `notes`, `covers` folders), and click **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, set *Source* to **Deploy from a branch**, pick `main` and `/ (root)`, and click **Save**.
4. Wait a minute or two, refresh the Pages settings, and the live address appears at the top. Put that link in your Instagram bio.

Later, a custom domain goes in **Settings → Pages → Custom domain**. GitHub Pages stays free.

## Adding your artwork

Upload files into the folders on GitHub (open the folder, then **Add file → Upload files**), then list them at the top of the script in `index.html`, in the block marked `YOUR FILES`.

| What | Folder | Size | List it in |
|---|---|---|---|
| Project artworks | `art/` | 1600 px on the long edge, any shape | `ARTWORK` |
| Sticky note on the projects table | `notes/` | 600 × 600 px, PNG | `SITE_NOTES` |
| Playlist covers | `covers/` | 1080 × 1350 px | `cover` on each playlist in `PLAYLISTS` |

Example:

```js
const ARTWORK = [
  'art/01.jpg',
  'art/02.png',
];
const SITE_NOTES = ['notes/note-1.png'];
const PLAYLISTS = [
  {title:'Rock', id:'2FeVxQ6ZPLOAuoejGJj9Fb', cover:'covers/rock.jpg'},
  ...
];
```

Keep each file under about 500 KB so the page loads fast on mobile data. To preview how new artwork fills the table before uploading, open the live site with `#edit` at the end of the address.

## Font

The page uses Lexend as a stand-in for Facile Sans. Facile Sans is free for personal, non-commercial use. To switch, add the font file to the repository, load it with `@font-face`, and put `"Facile Sans"` first in `--display` and `--body` in the stylesheet.
