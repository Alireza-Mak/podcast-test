# 🎙️ podcast-test

A learning project exploring **GitHub Actions**, built as part of my journey through the **[Career Essentials in GitHub Professional Certificate](https://www.linkedin.com/learning/paths/career-essentials-in-github-professional-certificate)**.

---

## 👋 About This Project

[#-about-this-project](#-about-this-project)

This repo is where I'm practicing real-world GitHub Actions workflows — starting small with a Python script that generates a podcast RSS feed, with the eventual goal of automating the whole thing with CI/CD.

**Status:** 🚧 Work in progress — still learning and building.

---

## 🚀 What It Does

[#-what-it-does](#-what-it-does)

**`feed.py` (Python)**

1. Reads episode data from **`feed.yaml`** — each entry describes a podcast item (e.g. title and other metadata).
2. Builds an XML structure that follows the **Apple Podcasts RSS feed** spec:
   - Creates the root `<rss>` element with the correct version and iTunes namespace/content attributes.
   - Adds a `<channel>` sub-element with feed-level info: title, subtitle, description, iTunes language, link, and category.
   - Loops through the items in `feed.yaml` and creates an `<item>` element for each one.
3. Outputs the final result as **`podcast.xml`** — a valid podcast RSS feed.

**`feed.yaml`**

Holds the source data feed.py reads from — the feed's metadata plus a list of episode items.

---

## 📁 Project Structure

[#-project-structure](#-project-structure)

```
podcast-test/
│
├── feed.py          # Reads feed.yaml and generates podcast.xml
├── feed.yaml         # Podcast feed & episode data (input)
├── podcast.xml        # Generated Apple Podcasts-compliant RSS feed (output)
└── README.md
```

---

## ⚙️ GitHub Actions

[#-github-actions](#-github-actions)

Automating `feed.py` with a GitHub Actions workflow (e.g. regenerating `podcast.xml` on a schedule or on push) is the next step — still figuring out the right trigger and setup as part of this learning process.

---

## ▶️ How to Run

[#-how-to-run](#-how-to-run)

1. Clone the repo
2. Update `feed.yaml` with your podcast/episode info
3. Run the script:
   ```bash
   python feed.py
   ```
4. Find your generated feed at `podcast.xml`

---

## 🛠 Skills Practiced

[#-skills-practiced](#-skills-practiced)

- Python (XML generation, file parsing)
- Working with YAML data
- RSS / Apple Podcasts feed spec
- GitHub Actions (in progress)

---

## 👨‍💻 About Me

[#-about-me](#-about-me)

I'm **Alireza Mak**, a full-stack developer with 5 years of experience, passionate about game development and creative coding. This project is part of my broader push to round out my CI/CD and automation skills alongside that.

🌐 Portfolio: [alirezamak.com](https://alirezamak.com)

---

## 🔗 Links

[#-links](#-links)

[![Portfolio](https://img.shields.io/badge/My_Portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://alirezamak.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alireza-mak/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:info@alirezamak.com)

---

## 📜 License

[#-license](#-license)

This project is open-source and available under the [MIT License](LICENSE).



## Useful Links
- [RSS Feed Sample](https://help.apple.com/itc/podcasts_connect/en.lproj/itcbaf351599.html)
- [Helpfull documentation](https://raybo.org/slides_practicalactions/#/)
- [Github Actions](https://docs.github.com/en/actions)