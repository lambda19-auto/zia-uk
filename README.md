# Run Locally

**Prerequisites**: Node.js

1. Install dependencies: `npm ci`.
2. Create your local environment file from the template:

   ```bash
   cp .env.example .env
   ```

3. Set the destination website in `.env`:

   ```dotenv
   VITE_SERVICE_URL=https://travelai.top/
   ```

   Use a full `https://` or `http://` URL. All three service buttons use this
   address. If the variable is missing or empty, they use `https://travelai.top/`.

4. Start the app: `npm run dev`.

Restart the development server after changing `.env`.

## Production build

Create and configure `.env` as described above, then run `npm run build`.
Deploy the generated `dist/` directory. To change the destination on a deployed
site, update `.env`, run `npm run build` again, and deploy the new `dist/`.
You can check the build locally with `npm run preview`.

`.env` is excluded from Git; `.env.example` is the committed template.
Variables prefixed with `VITE_` are included in the browser bundle and must not
contain secrets.
