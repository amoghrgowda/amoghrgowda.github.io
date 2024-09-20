To use **Jekyll** for your diary/blog and host it on GitHub Pages, follow this (originally meant for Arch but can be easily applied to other distros with few changes):

### 1. **Install Jekyll on Your Local Machine (Optional)**
   If you want to test the site locally before pushing it to GitHub, you can install Jekyll on your system.
   - First, make sure you have Ruby installed. On Arch Linux, you can install Ruby with:
     ```bash
     sudo pacman -S ruby
     ```
   - Next, install Jekyll and Bundler:
     ```bash
     gem install jekyll bundler
     ```
   - Then, create a new Jekyll site:
     ```bash
     jekyll new my-diary
     cd my-diary
     ```
   - Start the local server to see your site:
     ```bash
     bundle exec jekyll serve
     ```
     Now visit `http://localhost:4000` to preview your site.

### 2. **Create a GitHub Repository**
   - Go to GitHub and create a new repository named `<your-username>.github.io`. This will automatically make GitHub host your website at `https://<your-username>.github.io/`.

### 3. **Set Up Your Jekyll Project**
   - After creating the Jekyll site locally, you'll see some key files:
     - `_config.yml`: Configuration for your site.
     - `_posts/`: This is where you add your blog/diary posts in Markdown format.
     - `_layouts/`, `_includes/`, and `_sass/`: These contain the templates and styles used by Jekyll.
   
   You can customize the theme, layout, and add any plugins you want.

### 4. **Write Your Diary Entries**
   Jekyll uses Markdown files for posts. To create a new diary entry:
   - In the `_posts/` directory, create a Markdown file using the naming convention: `YYYY-MM-DD-your-post-title.md`. For example:
     ```
     2024-09-16-my-first-diary-entry.md
     ```
   Inside the Markdown file, use this structure:
   ```markdown
   ---
   layout: post
   title: "My First Diary Entry"
   date: 2024-09-16
   ---
   
   This is my first diary entry where I document what I learned today.
   ```
   The front matter (everything between the `---`) provides metadata like title and date, and the rest is the content of your post.

### 5. **Customize `_config.yml`**
   - Modify `_config.yml` to suit your needs, like adding your site’s title, description, and author name. You can also configure plugins and themes here.

### 6. **Push to GitHub**
   - Add, commit, and push your Jekyll site to the GitHub repository you created earlier.
     ```bash
     git init
     git add .
     git commit -m "Initial commit"
     git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
     git push -u origin main
     ```
   - GitHub Pages will automatically build the Jekyll site and deploy it at `https://<your-username>.github.io/`.

### 7. **Further Customization**
   - You can modify the theme by editing the HTML/CSS files in the `_layouts` or `_sass` directories.
   - You can find various free Jekyll themes online and use them to quickly change the appearance of your blog.
   - Add plugins or features like pagination or category filters to organize your posts better.
