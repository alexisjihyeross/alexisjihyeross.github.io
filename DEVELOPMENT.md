# Local Development

## Prerequisites

This site uses Jekyll with the `github-pages` gem, which requires **Ruby 3.1** (not newer) due to compatibility issues with the Liquid templating engine.

## Setup (macOS)

### 1. Install Homebrew (if not installed)
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Install Ruby 3.1
```bash
brew install ruby@3.1
```

### 3. Add Ruby 3.1 to your PATH
Add this to your `~/.zshrc`:
```bash
export PATH="/opt/homebrew/opt/ruby@3.1/bin:$PATH"
```

Then reload:
```bash
source ~/.zshrc
```

### 4. Verify Ruby version
```bash
ruby --version
# Should show ruby 3.1.x
```

### 5. Install dependencies
```bash
bundle install
```

## Running the site locally

```bash
bundle exec jekyll serve
```

Then visit: **http://localhost:4000**

## Troubleshooting

### Wrong Ruby version being used
If you see errors about `tainted?` method or incompatible gem versions, you're likely using Ruby 3.2+. Make sure Ruby 3.1 is in your PATH:
```bash
export PATH="/opt/homebrew/opt/ruby@3.1/bin:$PATH"
ruby --version  # Should be 3.1.x
```

### Gemfile.lock issues
If switching Ruby versions, delete and regenerate:
```bash
rm Gemfile.lock
bundle install
```

## Deployment

The site auto-deploys to GitHub Pages when you push to the main branch:
```bash
git add -A
git commit -m "Your message"
git push
```

Site will be live at: **https://alexisjihyeross.github.io**

