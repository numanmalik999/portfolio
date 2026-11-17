# How to update the portfolio

- Live site: https://portfolio-wine-theta-91.vercel.app
- GitHub repo: https://github.com/numanmalik999/portfolio
- Vercel project: "portfolio" — every push to `main` redeploys automatically.

The whole site is one file: `index.html`. All projects live in a list called
`PROJECTS` near the bottom of that file (search for `const PROJECTS`).

---

## Add a project

Copy any existing block, paste it inside the `PROJECTS` list, and change the values:

```js
{name:"My New App", icon:"🚀", cat:"tools",
 desc:"One or two sentences about what it does and who it's for.",
 tags:["React","Supabase"],
 live:"https://my-new-app.vercel.app",
 repo:"my-new-app"},
```

| Field | Required | What it means |
|---|---|---|
| `name` | yes | Title shown on the card |
| `icon` | yes | Any emoji |
| `cat` | yes | Category: `health`, `erp`, `ai`, `loyalty`, `tools` or `web` |
| `desc` | yes | Short description |
| `tags` | yes | Tech used, e.g. `["Next.js","TypeScript"]` |
| `live` | no | Live link (your Vercel URL or custom domain) |
| `repo` | no | GitHub repo name — **only for public repos**, private ones would show a 404 to visitors |
| `repoLabel` | no | Text on the GitHub button (default `Code`, e.g. `Downloads`) |
| `featured` | no | `featured:true` also shows it in the big "Featured work" section |
| `points` | only if featured | 2–3 highlight bullets: `points:["...","...","..."]` |

Don't forget the comma `,` after the closing `}`.

## Remove a project

Delete its whole `{ ... },` block.

## Edit a project

Change any field in its block (e.g. update the `live` link if you add a custom domain).

## Add a new category

Add a line to `CATS` (just above `PROJECTS`):

```js
edu:{label:"Education", c:"#4dabf7"},
```

`c` is the category colour. Then use `cat:"edu"` on projects.

## Other things you might change

- **Intro text / headline**: in the `<header class="hero">` section.
- **Contact email & LinkedIn**: in the `<section id="contact">` section.
- **Toolkit / skills**: in the `<section id="skills">` section.

Counts, filters and the footer year update by themselves.

---

## Preview locally

From this folder run:

```bash
python -m http.server 5180
```

then open http://localhost:5180

## Publish changes

If this folder is connected to a GitHub repo that's linked to Vercel:

```bash
git add .
git commit -m "Update projects"
git push
```

Vercel redeploys automatically within a minute.

## Easiest way

Open this folder in Claude and say, for example:
"Add my new project X, it's on Vercel" or "Remove Car Wash Loyalty".
Claude can look up the repo and its Vercel link and update the card for you.

## Where the links come from

- Live links: Vercel team "Muhammad nouman's projects" → each project's Domains.
- Repos: https://github.com/numanmalik999?tab=repositories
