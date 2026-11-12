VOCA 0.0.3 - installable web app (PWA)

1. Put this folder on any static host over https (GitHub Pages, Netlify, Cloudflare Pages), or serve it on localhost.
   (Installing and offline use need https or localhost. Double-clicking index.html works too, but cannot install.)
2. Open the address in Chrome on your phone, menu > Install app / Add to Home screen.
3. Updating: change VERSION in index.html, and bump C = "voca-0.0.3" in sw.js so phones fetch the new files.

Local models (Settings > AI):
- Base URL: http://localhost:11434/v1 (Ollama) or http://localhost:1234/v1 (LM Studio). API key can stay empty.
- Ollama must allow this page's origin: set OLLAMA_ORIGINS=* before starting it. LM Studio: switch on "Enable CORS".
- An https page can reach http://localhost, but browsers block plain-http network addresses (like http://192.168.x.x)
  from an https page. Host Voca on http in that case, or put the model behind https.
