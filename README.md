# CS 3803 Team 12 Project Website

This repository hosts our report website for the **MARTA App Redesign** project

## Website Pages

- `Home` ([index.md](index.md)): project title, authors, banner image, and summary.
- `Data` ([data.md](data.md)): methods, participants, tasks, and key findings template.
- `Recommendations` ([recommendations.md](recommendations.md)): redesign recommendations, roadmap, and success metrics.

## Run Locally (macOS)

From the repo root, run:

```bash
script/bootstrap
script/server
```

Then open: `http://127.0.0.1:4000`

### If `script/bootstrap` fails

This is usually a Ruby/Bundler environment issue on macOS.

1. Check Ruby is available:
   ```bash
   ruby -v
   ```
2. Install Bundler to your user gems (avoids permission issues):
   ```bash
   gem install --user-install bundler
   ```
3. Make sure your shell can find user gems:
   ```bash
   export PATH="$HOME/.gem/ruby/$(ruby -e 'print RbConfig::CONFIG["ruby_version"]')/bin:$PATH"
   ```
4. Retry:
   ```bash
   bundle install
   bundle exec jekyll serve
   ```

## Editing Content

- Update project metadata in [_config.yml](_config.yml).
- Replace author placeholders in [index.md](index.md).
- Fill in data/findings in [data.md](data.md).
- Fill in final recommendations in [recommendations.md](recommendations.md).

## Build Check

To verify the site builds:

```bash
script/cibuild
```

## Deployment

This project is structured for GitHub Pages with Jekyll.
Push changes to your repo branch, then publish via GitHub Pages settings (or your class deployment workflow).
