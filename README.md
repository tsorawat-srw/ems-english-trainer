# EMS English Trainer

Static GitHub Pages website with ABCD/SAMPLE flashcards, multiple-choice quiz, and a local Question Builder.

## Publish on GitHub Pages
1. Create a **public** GitHub repository named `ems-english-trainer`.
2. Upload **index.html**, **style.css**, **script.js**, **questions.json** to the repository root (README optional).
3. Go to **Settings → Pages → Build and deployment**. Select **Deploy from a branch**, branch **main**, folder **/(root)**, then **Save**.
4. Wait for deployment. Open `https://YOUR-USERNAME.github.io/ems-english-trainer/`.

## Add questions
- On the live site open **Question Builder**, fill the fields and click **Save question on this device**.
- Click **Export all questions (.json)**. This exports all current questions (starter and custom).
- On GitHub, open **questions.json**, choose **Edit**, replace its contents with the exported JSON, then **Commit changes**. Alternatively upload the exported file to replace `questions.json`.
- After GitHub Pages redeploys, **new visitors** will see the new questions.
- **Important:** existing browsers with a locally saved question set continue to use that local set. To get published changes on those devices, import the new `questions.json` using Question Builder. A future version can add a reset/sync button.

## Local preview
Because `questions.json` is loaded via fetch, don't double-click `index.html` using a `file://` URL. Run a local server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Limitations
- GitHub Pages is static; local saves do not automatically update GitHub or other users.
- Quiz scores and question changes are not synchronized between devices.
- Question Builder is not access controlled; anyone can modify their own browser's local copy, but cannot modify the GitHub repository without GitHub permissions.
- Educational language tool; not a clinical decision support system.
