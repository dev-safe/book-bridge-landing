# BookBridge landing page

Marketing site for [BookBridge](https://play.google.com/store/apps/details?id=cm.devsafe.bookbridge), live at <https://bookbridge.devsafe.cm>.

Built with SvelteKit and deployed on Vercel through `@sveltejs/adapter-vercel`. Every push to `main` deploys to production, and each pull request gets its own preview deployment.

## Develop

```bash
npm install
npm run dev
```

The server routes need three variables, which are already set in Vercel: `SUPABASE_URL` and `SUPABASE_ANON_KEY` for the listing share pages (`/l/[id]`), and `RUST_CORE_URL` for `/upgrade`. For local development, put them in `.env`; it is gitignored.

`static/.well-known/assetlinks.json` backs Android App Links for the app. It must keep both SHA-256 fingerprints, the Play app signing key and the upload key.
