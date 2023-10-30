#  Directus Agency OS

This is a ddev wrapper for a directus instance with nuxt frontend. [Agency OS Template](https://github.com/directus-community/agency-os)

1. Start project with `ddev start`
2. Create API token for directus Admin User
3. Clone Agency OS repo into `frontend` folder
   ```
   git clone https://github.com/directus-community/agency-os frontend
   ```
4. Set token and urls in `frontend/.env` file (the url are set globally in container already)
   ```
   # DIRECTUS_URL="http://directus.agency-os.ddev.site"
   DIRECTUS_SERVER_TOKEN="<TOKEN>"
   # SITE_URL="https://agency-os.ddev.site"
   ```
5. SSH into web container: `ddev ssh`
6. Init Agency OS data: `ddev exec npx directus-template-cli@latest apply`
7. Install Frontend dependencies: `ddev exec pnpm i`
8. Start Nuxt Frontend: `ddev exec pnpm dev`

Directus User:
* User: `admin@example.com`
* Pass: `d1r3ctu5`
