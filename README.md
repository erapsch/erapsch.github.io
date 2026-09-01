# erapsch.github.io

Source for my academic website, **[erapsch.github.io](https://erapsch.github.io)** — the
personal homepage of Dr. E. Emanuel Rapsch, mathematician working on probability, game, and
decision theory.

It is a static [Jekyll](https://jekyllrb.com/) site served by GitHub Pages, built on the
[Academic Pages](https://github.com/academicpages/academicpages.github.io) template — itself a
fork of the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) theme by Michael
Rose (© 2016, MIT License; see [`LICENSE`](LICENSE)).

## Structure

| Path | Contents |
|------|----------|
| `_config.yml` | Site-wide settings, author profile, social links |
| `_pages/` | Content pages: about, CV, research, teaching, legal notice, privacy policy |
| `_data/navigation.yml` | Top navigation bar |
| `files/` | Downloadable files, served at `/files/…` |
| `images/` | Profile photo and image assets |
| `_sass/`, `assets/` | Styles (Sass) and compiled CSS/JS |

## Running locally

Requires Ruby (with `ruby-dev` and `bundler`), Node.js, and a C toolchain for building
the native gem extensions. On Debian/Ubuntu:

```bash
sudo apt install ruby-dev bundler nodejs build-essential
```

Then install gems into a project-local path (avoids needing root for the system gem
directory) and serve:

```bash
bundle config set --local path vendor/bundle   # one-time; writes .bundle/config
bundle install
bundle exec jekyll serve -l -H localhost
```

Then open <http://localhost:4000>. The local server rebuilds and refreshes on file changes.
(`vendor/` and `.bundle/` are git-ignored. If `bundle install` complains about a lockfile,
delete `Gemfile.lock` and retry.)

## Credits

Built on Academic Pages / Minimal Mistakes, released under the MIT License. Site content ©
E. Emanuel Rapsch.
