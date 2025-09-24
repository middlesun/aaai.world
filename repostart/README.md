# RepoStart - Open Source Repository Discovery

RepoStart is a modern web application that helps developers and entrepreneurs discover the best open source repositories on GitHub. Built with vanilla HTML, CSS, and JavaScript, it provides powerful filtering, sorting, and search capabilities without requiring any backend infrastructure.

## Features

- **🔍 Advanced Search**: Search repositories by name, description, tags, and topics
- **🏷️ Smart Filtering**: Filter by categories, programming languages, and licenses
- **📊 Multiple Sorting**: Sort by stars, forks, recent updates, or launch date
- **❤️ Favorites**: Save your favorite repositories locally
- **🚀 One-Click Deploy**: Direct deployment links to Vercel and Netlify
- **📱 Responsive Design**: Works perfectly on desktop and mobile devices
- **⚡ Fast Performance**: Static site with JSON data for lightning-fast loading

## Quick Start

1. **Clone or download** this repository
2. **Open `index.html`** in your web browser
3. **Start exploring** repositories using the search and filter controls

## Data Management

### Adding New Repositories

Edit the `data/repos.json` file to add new repositories. Each repository should follow this structure:

```json
{
  "id": "unique-repo-id",
  "name": "Repository Name",
  "description": "Brief description of the repository",
  "github_url": "https://github.com/owner/repo",
  "live_demo": "https://demo-url.com",
  "stars": 1234,
  "forks": 567,
  "updated_at": "2025-01-15T10:30:00Z",
  "launched_at": "2023-06-01",
  "categories": ["E-commerce", "CMS"],
  "languages": ["JavaScript", "TypeScript"],
  "license": "MIT",
  "project_type": ["Web App", "Mobile"],
  "tags": ["react", "nodejs", "database"],
  "deploy_targets": ["vercel", "netlify"],
  "topics": ["trending", "featured"],
  "repo_owner": "owner",
  "repo_name": "repo"
}
```

### Field Descriptions

- **id**: Unique identifier (used for favorites)
- **name**: Display name of the repository
- **description**: Brief description (appears in search)
- **github_url**: Link to the GitHub repository
- **live_demo**: Live demo URL (optional)
- **stars**: Number of GitHub stars
- **forks**: Number of GitHub forks
- **updated_at**: Last update date (ISO format)
- **launched_at**: Launch date (YYYY-MM-DD format)
- **categories**: Array of categories (E-commerce, CMS, Social Network, etc.)
- **languages**: Array of programming languages
- **license**: License type (MIT, Apache-2.0, GPL-3.0, etc.)
- **project_type**: Array of project types (Web App, Mobile, Desktop)
- **tags**: Array of searchable tags
- **deploy_targets**: Array of supported deployment platforms
- **topics**: Array of display topics (trending, popular, featured, new)
- **repo_owner**: GitHub repository owner
- **repo_name**: GitHub repository name

## Deployment

### Static Hosting (Recommended)

Deploy to any static hosting service:

- **Vercel**: Connect your GitHub repo and deploy automatically
- **Netlify**: Drag and drop the folder or connect via Git
- **Cloudflare Pages**: Connect repository for automatic deployments
- **GitHub Pages**: Enable in repository settings

### Local Development

1. Serve the files using a local server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

2. Open `http://localhost:8000` in your browser

## Customization

### Adding New Categories

1. Update the category options in `index.html`:
   ```html
   <select multiple id="filter-categories">
     <option>E-commerce</option>
     <option>CMS</option>
     <!-- Add your new category -->
     <option>Your New Category</option>
   </select>
   ```

2. Add repositories with the new category in `data/repos.json`

### Adding New Languages

1. Update the language options in `index.html`:
   ```html
   <select multiple id="filter-languages">
     <option>JavaScript</option>
     <option>TypeScript</option>
     <!-- Add your new language -->
     <option>Your New Language</option>
   </select>
   ```

### Styling Changes

The app uses Tailwind CSS for styling. You can:
- Modify colors in the Tailwind config section
- Add custom CSS in the `<style>` section
- Update the cyberpunk theme colors and effects

## Data Sources

### Manual Entry
- Edit `data/repos.json` directly
- Use GitHub's web interface to edit files
- Collaborate via pull requests

### Automated Updates (Advanced)

For automated data updates, you can:

1. **GitHub Actions**: Create workflows to fetch repository data
2. **Netlify Functions**: Serverless functions to update data
3. **External APIs**: Integrate with GitHub API for real-time data

Example GitHub Action for updating stars/forks:
```yaml
name: Update Repository Stats
on:
  schedule:
    - cron: '0 0 * * *'  # Daily at midnight
jobs:
  update-stats:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Update repository data
        run: |
          # Your script to fetch and update data
```

## Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Contributing

1. Fork the repository
2. Add new repositories to `data/repos.json`
3. Test your changes locally
4. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

- 📧 Email: support@repostart.com
- 🐛 Issues: [GitHub Issues](https://github.com/your-repo/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/your-repo/discussions)

---

**RepoStart** - Discover the best open source repositories to build your next project! 🚀

