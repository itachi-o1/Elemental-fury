
Elemental Fury — GitHub + Netlify + Render deployment package
============================================================

Contents:
- Client in /src and /public (Vite + React)
- Server stubs in /server (Socket.IO)
- GitHub Actions workflow to build the client

Quick start — local play
1. npm install
2. npm run dev
3. Open the Vite URL (usually http://localhost:5173)

Deploy client to Netlify (static hosting)
1. Create a GitHub repo and push this project.
2. In Netlify: "Add new site" → Import from GitHub → select repo.
3. Build command: npm run build
   Publish directory: dist
4. Add Netlify env var: REACT_APP_SOCKET_SERVER = https://<your-server-url>
5. Deploy site — you'll get a netlify.app URL.

Deploy server to Render (free)
1. Sign into Render and create a new Web Service from GitHub.
2. Use the /server folder as the service root and start command: node server_ggpo_full.js
3. After deploy, note the public URL and set it as REACT_APP_SOCKET_SERVER in Netlify envs.
4. Open the Netlify site and switch game mode to Online to connect to your server.

Notes:
- Server stubs are for demo/testing only.
- Replace placeholder sprites in /public/assets/sprites with your art for better visuals.

If you'd like, I can (with your permission):
- Create the GitHub repository for you and push this package.
- Trigger the Netlify and Render deployments (you will need to authorize/link accounts).
