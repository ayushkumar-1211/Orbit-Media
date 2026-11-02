# Deploy Orbit to Vercel

## Option A: GitHub + Vercel (no coding tools needed)
1. Create a free GitHub account and a new repository (e.g. `orbit-site`).
2. On the repository page click "uploading an existing file", drag in EVERYTHING inside this folder
   (index.html, vercel.json, the assets folder), then "Commit changes".
3. Go to vercel.com/new, sign in with GitHub, import the repository.
4. Framework preset: "Other". Leave build settings empty. Click Deploy.

## Option B: Vercel CLI
    npm i -g vercel
    cd orbit-site
    vercel          # first deploy (preview)
    vercel --prod   # production

## Custom domain from GoDaddy
1. Vercel project > Settings > Domains > Add > enter yourdomain.com (also add www when asked).
2. GoDaddy > My Products > your domain > DNS:
   - Delete any existing A record for "@" (often "Parked") and any AAAA record for "@".
   - A     @    -> the value shown on your Vercel domain card (usually 76.76.21.21)
   - CNAME www  -> the value shown on your Vercel domain card (e.g. xxxx.vercel-dns-017.com)
3. Wait for Vercel to show "Valid Configuration". HTTPS is added automatically.
