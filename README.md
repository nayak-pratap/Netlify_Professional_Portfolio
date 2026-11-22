# Netlify Professional Portfolio

Source for **[pratapnayak.netlify.app](https://pratapnayak.netlify.app/)** — the portfolio
site of Pratap Nayak, Manufacturing Engineering & Technology Leader.

Plain static HTML. No build step, no framework, no dependencies.

## Files

| File | What it is |
| --- | --- |
| `index.html` | Home page: intro, initiatives, career timeline, leadership approach, working library, credentials, contact. Navigates by anchor. |
| `tools.html` | The working library — every tool and framework, each linking out to its own repository on GitHub Pages. Served at `/tools`. |
| `GitHub.jpg` | Portrait used on the home page. |
| `_redirects` | Netlify routing: the clean `/tools` URL, plus forwarding for pages that have moved. |
| `netlify.toml` | Publish directory only. There is no build command. |

## How it deploys

Netlify builds from this repository. A push to `main` is a production deploy —
there is no confirmation step, so a push is a publish.

Build command: none. Publish directory: repository root.

## Where the tools live

The site itself is two pages. Every tool is its own repository, served from GitHub Pages:

- [The Manager's Toolkit](https://nayak-pratap.github.io/MBA_Managers_Toolkit/) — 18 frameworks and 33 interactive calculators
- [Cost per Part Business Case](https://nayak-pratap.github.io/MBA-Business-Case-Cost-per-Part/)
- [Quality Tools for Manufacturing](https://nayak-pratap.github.io/ENG_MFG_Quality_Tools/index.html)
- [Engineering AI Value Case](https://nayak-pratap.github.io/MBA-Engineering-AI-Value-Case/)
- [Facility Location (MILP)](https://nayak-pratap.github.io/MBA-SCM-Facility-Location-MILP/)
- [Interview Panel Score Audit](https://nayak-pratap.github.io/MBA-Interview-Panel-Score-Audit/)

## Redirects

Pages that used to be hosted here now live in those repositories. `_redirects`
forwards the old URLs so existing links and bookmarks keep working instead of
returning 404. The toolkit rule maps one-to-one, because the file names are
identical on both sides:

```
/tools/managers-toolkit/machining-tools.html
  -> https://nayak-pratap.github.io/MBA_Managers_Toolkit/machining-tools.html
```

The remaining retired paths point at the tools listing until each has a
confirmed new home.
