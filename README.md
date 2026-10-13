# Citizens of AI starter

A free Astro blog starter for the Citizens of AI workshop, based on [Blogsmith Free by Cosmic Themes](https://github.com/Cosmic-Themes/blogsmithfree).

Start with a working website. Use AI to understand it, customize a small part, save your changes, and deploy your own copy.

[Create your own copy](https://github.com/R3defined/citizens-of-ai-starter/generate) · [Workshop instructions](WORKSHOP.md) · [Original theme documentation](UPSTREAM.md)

## Before the workshop

Bring a laptop and access to your email and verification device. Sign into GitHub, Vercel, and the AI editor demonstrated by the instructor. Different AI tools have different repository access and editing capabilities. A chat assistant alone does not automatically edit or publish your repository.

## Make your own project

1. Click **Use this template**, then **Create a new repository**.
2. Select your own GitHub account as the owner.
3. Give your project a name, such as `my-learning-journal`.
4. Choose the visibility intentionally. Public means anyone can see the source. Never include passwords, API keys, private information, or client content.
5. Leave **Include all branches** unchecked and create the repository.
6. Open your new repository in the selected AI editor. Work in your copy, not this shared starter.

## Run the site

Use Node.js 22 LTS and npm for the workshop. Local verification was performed with Node.js 26.4.0 and npm 11.17.0; Node.js 22 is the recommended participant baseline, not an independently tested environment.

From your project folder:

```sh
npm ci
npm run dev
```

Open the local URL printed by Astro, normally `http://localhost:4321`.

To check the production build:

```sh
npm run build
npm run preview
```

The production files are written to `dist`. This workshop copy includes `package-lock.json` so npm installs have a recorded dependency resolution. The upstream pnpm lockfile is preserved for provenance; use npm consistently during the workshop.

## Your first changes

| What you want to change | Where to start |
| --- | --- |
| Homepage headline and introduction | `src/components/Hero/Hero.astro` |
| Site name, browser title, description | `src/config/siteData.json.ts` |
| About page | `src/data/otherPages/about.md` |
| Sample articles | `src/data/blog/` |
| Navigation links | `src/config/navData.json.ts` |
| Theme colors | `src/styles/tailwind-theme.css` |

Keep the sample article frontmatter and image references valid. The theme includes upstream demonstration content, author profiles, branding, and a sample privacy policy. Those are examples, not claims about your own site. Review them before sharing your finished website beyond the exercise.

## Deploy your copy to Vercel

1. Sign into Vercel and add a new Project.
2. Connect GitHub and grant access to your workshop repository rather than every repository, where the authorization flow permits that choice.
3. Import your own repository.
4. Confirm the framework is **Astro**, the build command is `npm run build`, and the output directory is `dist`.
5. Use `npm ci` as the install command and Node.js 22.x in the project settings. The site does not require environment variables for this exercise.
6. Review the sample content, then deploy only if you intend to make the site accessible at its deployment URL.
7. Open the URL and test the homepage, an article, navigation, and a narrow phone layout.

After your first deployment, update the `site` URL in `astro.config.mjs` and the sitemap URL in `public/robots.txt` to your own production domain, then commit the change. They initially retain the original theme's demo domain.

A private repository does not automatically make the deployed website private. Deployment access depends on the Vercel project's settings. Inspect those settings rather than assuming a URL is protected.

Vercel deployment instructions are provided here, but this repository has not yet been deployed to Vercel by the instructor. A local build is not proof of a successful hosted deployment.

## Workshop scope

Customize the introduction and one article, save a meaningful commit, deploy, and verify the result. Accounts inside the website, payments, databases, API integrations, and custom domains are outside this first exercise.

Finish by saving your GitHub repository URL and your deployed website URL.

## Security and limitations

This is an educational starter, not a security hardened production application. The initial dependency audit reported known advisories. Read [SECURITY.md](SECURITY.md) before extending the project. Do not expose the development server publicly or use sensitive data. Dependency remediation and hosted deployment verification remain separate work.

## Attribution and license

The underlying theme was created by **Cosmic Themes**, not Citizens of AI. The original source is [Cosmic-Themes/blogsmithfree](https://github.com/Cosmic-Themes/blogsmithfree), imported from commit `3d0849221b0a6f098b59b169a738745d2a6447a5`.

The original [GPL-3.0 license](LICENSE), theme attribution, and source notices are retained. Workshop documentation and the npm lockfile were added for this shared starter. Preserve the license and applicable notices when distributing copies or modifications, and comply with GPL source distribution requirements.

The original README is available in [UPSTREAM.md](UPSTREAM.md). This repository does not grant rights to Cosmic Themes' separate paid products or to third party content beyond the rights actually provided by their owners.
