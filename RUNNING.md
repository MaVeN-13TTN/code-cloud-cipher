# Running the Site Locally

This document provides instructions for running the Code, Cloud and Cipher blog locally on your machine.

## Prerequisites

1. Ruby (version 3.2.3 or higher)
2. RubyGems
3. Bundler
4. Git

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/MaVeN-13TTN/code-cloud-cipher.git
   cd code-cloud-cipher
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

## Running the Site

1. Start the Jekyll server:
   ```bash
   bundle exec jekyll serve --livereload
   ```
   This will:
   - Build your site
   - Start a local server
   - Watch for changes
   - Enable live reload (automatically refresh your browser when files are modified)

2. Access the site:
   - Open your browser and go to: http://127.0.0.1:4000/code-cloud-cipher/
   - The site should be available with full functionality

## Verifying Your Setup

1. Check Prerequisites:
   ```bash
   # Verify Ruby version
   ruby -v  # Should show 3.2.3 or higher

   # Verify Bundler installation
   bundle -v

   # Verify Jekyll installation
   bundle exec jekyll -v
   ```

2. Verify Site Structure:
   - Ensure these key files/directories exist:
     ```bash
     ls -la
     # Should show:
     # - _config.yml
     # - Gemfile
     # - _posts/
     # - _tabs/
     # - assets/
     ```

3. Verify Site Functionality:
   - [ ] Homepage loads at http://127.0.0.1:4000/code-cloud-cipher/
   - [ ] Navigation menu is visible
   - [ ] About page loads correctly
   - [ ] Blog posts are visible and properly formatted
   - [ ] Images load correctly (especially avatar and icons)
   - [ ] Site search works
   - [ ] Categories and Tags pages work

4. Verify Development Features:
   ```bash
   # Test live reload
   touch _posts/$(date +%Y-%m-%d)-test.md
   # The server should detect the new file
   
   # Test build process
   bundle exec jekyll build
   # Should complete without errors
   ```

5. Common Success Indicators:
   - Server starts without errors
   - No missing dependency warnings
   - No layout warnings in the console
   - Live reload connects successfully
   - Site loads with proper styling

## Common Issues and Solutions

1. **Port Already in Use**
   If you see an error about the port being in use, you can either:
   - Kill the existing Jekyll process:
     ```bash
     pkill -f jekyll
     ```
   - Or use a different port:
     ```bash
     bundle exec jekyll serve --livereload --port 4001
     ```

2. **Bundler Version Conflicts**
   If you encounter gem version conflicts, try:
   ```bash
   bundle clean --force
   bundle install
   ```

## Development Tips

1. The `--livereload` flag automatically refreshes your browser when files are modified
2. Use `bundle exec jekyll serve --drafts` to preview posts in the `_drafts` folder
3. The site configuration is in `_config.yml`
4. Posts are stored in the `_posts` directory

## File Structure

- `_posts/` - Blog posts
- `_tabs/` - Navigation pages (About, Categories, etc.)
- `assets/` - Images, CSS, and other static files
- `_config.yml` - Site configuration
- `Gemfile` - Ruby dependencies

## Additional Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Chirpy Theme Documentation](https://chirpy.cotes.page/)
