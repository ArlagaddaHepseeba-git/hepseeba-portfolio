# hepseeba-portfolio

Personal portfolio for **Arlagadda Hepseeba** — DevOps Engineer.

Live site: **https://arlagaddahepseeba-git.github.io/hepseeba-portfolio/**

## What this is

A single self-contained static page. No build step, no framework, no JavaScript
dependencies. One file: [`index.html`](index.html).

Everything (styles, script, architecture diagram) is inlined, so there is nothing
to install and nothing to compile before publishing.

## Design

- Dark theme, single scrolling column with a fixed sidebar on desktop
- Sidebar collapses to a dropdown bar under 900px
- Terminal hero with a typing animation
- Architecture diagram for the three-tier application is inline SVG, not an image
- Honours `prefers-reduced-motion`, so the typing animation and pulsing status
  dot are disabled for users who ask for reduced motion
- Fonts load from Google Fonts with system-ui fallbacks, so text still renders
  if the font CDN is blocked

## Publish

The site is served from the root of this repository. GitHub Pages must be
enabled:

1. Repository **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / root (`/`)
4. Save — the site publishes at
   `https://arlagaddahepseeba-git.github.io/hepseeba-portfolio/`

`.nojekyll` is present so Pages serves the files as-is instead of running them
through Jekyll.

## Editing the content

All content lives in `index.html`. The sections are:

| Section | `id` | What it covers |
|---|---|---|
| Hero | `#hero` | Name, role, summary, three counts, buttons |
| About | `#about` | Three short paragraphs |
| Skills | `#skills` | Nine-layer stack table |
| Experience | `#experience` | Two internships, newest first |
| Projects | `#projects` | Three project cards with repo links |
| Education | `#education` | Degrees and certifications |
| Contact | `#contact` | Email, phone, LinkedIn, GitHub |

If you add or remove a section, update the navigation in **both** places —
`.rail nav` for desktop and the `<select>` in `.topbar` for mobile. The
scroll-spy script reads section `id` attributes, so it picks up new sections
automatically, but the links have to be added by hand.

## Statistics in the hero

The three numbers in the hero section are counts you can verify by opening the
repositories:

| Number | Source |
|---|---|
| 5 Terraform modules | `terraform/modules/` in `aws-infrastructure-terraform` |
| 5 Kubernetes manifests | `k8s/*.yaml` in `Three-Tier-Web-Application-Deployment` |
| 3 Ansible roles | `roles/` in `ansible-configuration-management` |

If you add or remove a module, manifest, or role, update these to match.

## Projects linked from this site

| Project | Repository |
|---|---|
| Three-Tier Web Application on AWS | [`Three-Tier-Web-Application-Deployment`](https://github.com/ArlagaddaHepseeba-git/Three-Tier-Web-Application-Deployment) |
| AWS Infrastructure with Terraform | [`aws-infrastructure-terraform`](https://github.com/ArlagaddaHepseeba-git/aws-infrastructure-terraform) |
| Configuration Management with Ansible | [`ansible-configuration-management`](https://github.com/ArlagaddaHepseeba-git/ansible-configuration-management) |

## Licence

Personal portfolio. Code samples referenced here belong to their own
repositories and carry their own licences.
