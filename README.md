# 👁️ AI Eyes: Hear what you can't see

An accessibility project that explains images, charts, memes and web pages **out loud** for people who are blind or have low vision. It works as a website and as a Chrome extension.

**Live demo:** https://priyaexe18.github.io/ai-eyes-website/

## The problem
Screen readers read text well, but they cannot describe images, graphs, memes or complex layouts. Many images on the web have no description at all, so blind and low-vision users miss important information.

## The solution
Choose an image (or take a photo) and AI Eyes describes it in clear spoken words, in Hindi or English.

## Features
- **Describe any image:** charts, graphs, memes, infographics, diagrams and screenshots
- **Take photo:** on a phone it opens the camera and describes the photo straight away
- **Ready-made samples:** try a bar chart, a meme and a news page without any setup
- **High contrast and large text:** one button makes the site black and yellow with bigger text
- **Speech speed:** slow, normal or fast
- **Hindi and English voice**
- **Keyboard and screen reader friendly:** labels, focus outlines and live status messages
- **Chrome extension:** right-click an image, press Alt+Shift+E to explain the screen, Alt+Shift+S to stop

## How it works
1. The browser sends the image to a small **Cloudflare Worker**.
2. The Worker adds the secret API key and asks **Gemini Vision** to describe the image.
3. The description comes back and the browser reads it aloud with **text-to-speech**.

The API key is stored only on the server, never in this repository. Visitors do not need their own key.

## Tech stack
JavaScript, HTML and CSS, Chrome Extension (Manifest V3), Cloudflare Workers, Gemini Vision API, Web Speech API, GitHub Pages

## Files
| File | What it is |
|---|---|
| `index.html` | The website, including the live demo |
| `ai-eyes-extension.zip` | The Chrome extension |

## Install the Chrome extension
1. Download and unzip `ai-eyes-extension.zip`.
2. Open `chrome://extensions` and turn on **Developer mode**.
3. Click **Load unpacked** and choose the unzipped folder.
4. Paste a free Gemini API key (from aistudio.google.com/apikey) on the settings page and save.

## Privacy
Images are sent only to generate a description and are not stored by this project.

## Future scope
- Describe every image on a page at once
- More Indian languages
- Offline mode
- Firefox and mobile app support
