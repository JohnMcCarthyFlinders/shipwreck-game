# Shipwreck Sampling Game

A one-file browser game for the maritime archaeology sampling tutorial (ARCH3208 / ARCH8151). Students play a Southern Seas Heritage Trust archaeologist. They work through all four wrecks (amphora mound, oak hull, iron steamer, drowned landscape), spend a $5,000 budget at each, and get a score and a newspaper headline per site. The four scores add up to a total out of 400, which decides a final career:

| Total | Career |
|---|---|
| 320+ | Famous leading archaeologist |
| 220-319 | Experienced professional |
| 100-219 | Landlubber with more to learn |
| under 100 | Fired from the project |

Each career has a gender-neutral pixel portrait (happy or sad to match) and its own short theme tune. A project is cancelled (0 points) if the budget is exceeded, fieldwork is skipped, or a method can't work at that site. Players can replay for a better result.

Everything is in `index.html` (logo, icons, sounds and scoring are all inside it). There is nothing to install or build.

## Put it on GitHub Pages

1. Sign in to GitHub and create a new **public** repository (for example `shipwreck-game`).
2. Choose **Add file > Upload files** and upload `index.html`. Commit it.
3. Open **Settings > Pages**.
4. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main**, folder **/ (root)**, and save.
5. Wait a minute or two. The game will be at `https://YOUR-USERNAME.github.io/shipwreck-game/`.

## Using it with Canvas

- Add the GitHub Pages address to a Canvas Module as an external URL, or paste it as a link in a Page. Students open it in their browser.
- Embedding it inside a Canvas Page with an iframe may or may not be allowed by your institution's Canvas settings, so test it before class. A plain link is the safe option.
- Uploading `index.html` straight into Canvas Files may download the file instead of running it. Linking out to GitHub Pages avoids that.

## Things to know

- **Sound and music are on by default**, but browsers only allow audio after a click, so it starts when the student presses START. The two buttons at the top right switch effects and lofi music off. Everything is generated in the browser, so there are no audio files.
- **The answers are in the page.** Scores and reasons are stored in the page source, so a curious student can find them with View Source. That suits a tutorial, but not an assessed task.
- **No student data is collected.** The page does not send anything anywhere. Students copy their own Canvas post text.
- **Fonts** load from Google Fonts. If a student is offline, the page falls back to a plain monospaced font and still works.
- **The Flinders logo** is embedded. Check Flinders brand rules before hosting it on a personal GitHub account. A university or school GitHub organisation may be more appropriate.

## Changing prices or scores

Near the top of the `<script>` in `index.html` is a `DATA` block holding the budget, method prices, site descriptions and every score with its reason. Edit the numbers there. If you change a score, check that the best possible plan for each site still fits in the budget (the page works out the best plan itself and shows it to students).
