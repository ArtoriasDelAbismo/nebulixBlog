# Nebulix | Astro + Static CMS

[![License: CC BY-ND 4.0](https://img.shields.io/badge/License-CC_BY--ND_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nd/4.0/)




A Universe of Possibilities: Blogs, Portfolios, Webshop, Restaurant Menus, and Beyond.



![Nebulix](https://nebulix.unfolding.io/screenshot.png)

## Notice

__This theme is still in development, till we reach v1.0.0 it can be that upgrading will cause errors.__


## Constellations of Features:

-   📰 Chart Your Path with a Blog
-   🖼 Showcase Your Stellar Portfolio
-   🍝 Illuminate Culinary Voyages with a Restaurant Menu
-   🛒 Launch Your Webshop Powered by Snipcart
-   🔍 SEO Constellations: Canonical URLs and OpenGraph radiance
-   🧭 Navigational Maps: Sitemap Support
-   📑Language of the Stars: Markdown & MDX Support
-   📝 Static CMS Ready for Galactic Exploration
-   🕵 Unveil Hidden Constellations with Full Text Search using Pagefind

## ♻️ Page Speed and Emissions
Experience the green and swift capabilities of Nebulix. With an impressively low emission of 0.08g CO2 per page visit and consistently achieving a lighthouse score between 99 and 100, Nebulix ensures both speed and environmental consciousness for your website.

## 🚀 Getting Started

### 1. Setting up the .env file

rename the `env.txt` to `.env` and fill in your details

```ENV
BLOG_SLUG=blog
PORTFOLIO_SLUG=work
SHOP_SLUG=shop
MENU_SLUG=menu
WEBSITE_LANGUAGE=en
CURRENCY=USD
UNITS=metric
SNIPCART_KEY=<your-snipcart-public-key>
NODE_VERSION=18
```

### 2. Configure your Static CMS Backend

Navigate to `src/pages/admin.astro` and provide your Git repository details. You can find a list of all supported Git backends at:
<https://www.staticcms.org/docs/backends-overview>


**_Gitlab Example:_**

```javascript

const config = {
	locale: lang,
	site_url: url,
	logo_url: 'https://nebulix.unfolding.io/nebulix-logo.svg',
	local_backend: true,
	backend: {
		name: 'gitlab',
		repo: '/<your-gitlab-repo>',
		auth_type: 'pkce', // Required for pkce
		app_id: 'xxxx', // Application ID from your GitLab settings
		commit_messages: {
			create: 'Create {{collection}} "{{slug}}"',
			update: 'Update {{collection}} "{{slug}}"',
			delete: 'Delete {{collection}} "{{slug}}"',
			uploadMedia: 'Upload "{{path}}"',
			deleteMedia: 'Delete "{{path}}"'
		}
	},
	search: 'true',
    ....
}

```

### 3. Add your site to the astro config

```javascript

export default defineConfig({
	site: 'https://your-website.com',
    ....

```

### 4. Install dependencies

```bash
$ npm install
```

### 🛠️ 5. Start Development server

```bash
$ npm r
```

If you wish to engage the local backend:

```bash
$ npm run cms-proxy-server
```

Now you can open Static CMS on http://localhost:4321/admin/


## ❌ Removing Collections
If your cosmic journey excludes a blog, portfolio, shop, or restaurant menu, simply remove the corresponding documents from the `src/content`. Additionally, erase the page templates from `src/pages` .


## 🛸 Commands

All commands are run from the root of the project, from a terminal:

| Command                    | Action                                           |
| :------------------------- | :----------------------------------------------- |
| `npm install`              | Installs dependencies                            |
| `npm run dev`              | Starts local dev server at `localhost:3000`      |
| `npm run cms-proxy-server` | Starts Static CMS proxy server for local-backend |
| `npm run build`            | Build your production site to `./dist/`          |
| `npm run preview`          | Preview your build locally, before deploying     |
| `npm run astro ...`        | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help`  | Get help using the Astro CLI                     |

## 📁 Documentation
Learn how to harness the power of Static CMS and craft a distinctive website that stands out from the crowd.

[Documentation](https://nebulix.unfolding.io/blog/tag/docs)

## 🌐 Demo

Witness the extraordinary speed of Nebulix in action.

[Demo](https://nebulix.unfolding.io)

## 👀 Want to learn more about Astro?

Check out [Astro documentation](https://docs.astro.build) or jump into Astro's [Discord server](https://astro.build/chat).

## 📚 Tech Stack

Astro, MDX, Vue, TailwindCSS, Pagefind, Snipcart

## 🛟 Support

If you encounter any issues or bugs, we encourage you to open an issue in the repository. To help us quickly address the problem, please provide detailed information about the bug and steps to reproduce it.

For those seeking priority assistance, we offer premium support services. Feel free to reach out to us by email at [hello@unfolding.io.](mailto:hello@unfolding.io.) We're here to help!


## 🚕 Roadmap

As we journey towards v1.0, our path includes enriching the page builder with a diverse array of new blocks, upgrading dependencies to ensure optimal performance, and introducing exciting features. We're eager to hear from you! If you have any feature requests, please feel free to reach out and let us know.
