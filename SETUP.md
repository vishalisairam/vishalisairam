# GitHub Pages Setup Instructions

This document provides step-by-step instructions to deploy Vishali's professional portfolio website using GitHub Pages.

## Prerequisites

1. GitHub account (vishalisairam)
2. Git installed on your local machine

## Deployment Steps

### Step 1: Create GitHub Repository
1. Go to [GitHub](https://github.com) and log in as `vishalisairam`
2. Create a new repository named `vishalisairam.github.io` 
3. Make sure it's **public** (required for GitHub Pages free tier)
4. Don't initialize with README (we already have one)

### Step 2: Upload Files to Repository

Option A: Using GitHub Web Interface
1. Go to your new repository `vishalisairam/vishalisairam.github.io`
2. Click "uploading an existing file"
3. Drag and drop all files from the `vishalisairam` folder

Option B: Using Git Command Line
```bash
cd /Users/vinod/Desktop/Personal/Vishali/Webpage/vishalisairam
git init
git add .
git commit -m "Initial commit: Professional portfolio website"
git branch -M main
git remote add origin https://github.com/vishalisairam/vishalisairam.github.io.git
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. Go to repository Settings
2. Scroll down to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Click Save

### Step 4: Configure Custom Domain (Optional)
If you want to use a custom domain:
1. Add a `CNAME` file with your domain name
2. Configure DNS settings with your domain provider
3. Enable "Enforce HTTPS" in Pages settings

## Site Structure

```
vishalisairam.github.io/
├── _config.yml          # Site configuration
├── _data/
│   └── navigation.yml   # Navigation menu
├── _pages/
│   ├── about.md         # About page
│   ├── experience.md    # Experience timeline
│   ├── publications.md  # Publications and research
│   └── skills.md        # Skills and expertise
├── assets/
│   └── docs/
│       └── Vishali_Sairam_Resume.pdf
├── images/
│   └── vishali.jpg      # Profile photo
├── index.md             # Homepage
├── Gemfile              # Ruby dependencies
└── README.md            # Repository documentation
```

## Customization Options

### Updating Content
- **Personal Info**: Edit `_config.yml` author section
- **Homepage**: Modify `index.md`
- **Individual Pages**: Edit files in `_pages/` directory
- **Navigation**: Update `_data/navigation.yml`

### Changing Theme Colors
Add to `_config.yml`:
```yaml
minimal_mistakes_skin: "air"  # Options: default, air, aqua, contrast, dark, dirt, neon, mint, plum, sunrise
```

### Adding Google Analytics
Add to `_config.yml`:
```yaml
analytics:
  provider: "google-gtag"
  google:
    tracking_id: "GA_TRACKING_ID"
```

## Expected Timeline

- **Setup**: 5-10 minutes
- **GitHub Processing**: 5-10 minutes  
- **First Deployment**: Up to 10 minutes
- **Subsequent Updates**: 1-3 minutes

## Accessing the Website

Once deployed, the website will be available at:
- **Primary URL**: https://vishalisairam.github.io
- **Status Check**: Repository Settings → Pages section

## Updating Content

To update the website content:

1. **Via GitHub Web Interface**:
   - Navigate to the file you want to edit
   - Click the pencil icon to edit
   - Make changes and commit

2. **Via Local Development**:
   ```bash
   git pull origin main        # Get latest changes
   # Make your edits
   git add .
   git commit -m "Update content"
   git push origin main        # Deploy changes
   ```

## Troubleshooting

### Common Issues

1. **Site Not Loading**
   - Check repository name is exactly `vishalisairam.github.io`
   - Verify repository is public
   - Wait 10-15 minutes for initial deployment

2. **Images Not Displaying**
   - Ensure images are in the `images/` directory
   - Check file paths in markdown files
   - Verify image file names match exactly

3. **Styling Issues**
   - Confirm `_config.yml` has correct `remote_theme` setting
   - Check for YAML syntax errors

### Build Errors
- GitHub will send email notifications if there are build errors
- Check the "Actions" tab in your repository for detailed logs
- Common issues: YAML formatting, missing files, plugin conflicts

## Professional Maintenance

### Regular Updates
- **Experience**: Update `_pages/experience.md` when changing roles
- **Publications**: Add new research to `_pages/publications.md`
- **Skills**: Keep `_pages/skills.md` current with new technical skills
- **Resume**: Replace PDF in `assets/docs/` directory

### SEO Optimization
- Update page titles and descriptions
- Add relevant keywords to content
- Ensure all images have alt text
- Submit sitemap to Google Search Console

## Support

For technical issues with GitHub Pages:
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Minimal Mistakes Theme Docs](https://mmistakes.github.io/minimal-mistakes/)

---

*This setup creates a professional, mobile-responsive website optimized for academic and professional portfolios.*