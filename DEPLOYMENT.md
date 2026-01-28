# Deployment Guide

This guide will walk you through deploying the Ryder Entertainment website to GitHub Pages.

## Prerequisites

- A GitHub account
- Git installed on your computer
- The website files from this repository

## Step-by-Step Deployment

### 1. Create a New Repository on GitHub

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., `ryder-entertainment`)
5. Choose "Public" (required for free GitHub Pages)
6. **Do NOT** initialize with README, .gitignore, or license (we already have these)
7. Click "Create repository"

### 2. Upload Files to GitHub

#### Option A: Using Git Command Line

```bash
# Navigate to the website folder
cd path/to/ryder-entertainment-site

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Ryder Entertainment website"

# Add remote repository (replace YOUR_USERNAME and YOUR_REPO)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

# Push to GitHub
git branch -M main
git push -u origin main
```

#### Option B: Using GitHub Desktop

1. Open GitHub Desktop
2. File > Add Local Repository
3. Select the `ryder-entertainment-site` folder
4. Click "Publish repository"
5. Uncheck "Keep this code private"
6. Click "Publish Repository"

#### Option C: Upload Files Directly

1. On your new repository page, click "uploading an existing file"
2. Drag and drop all files from `ryder-entertainment-site` folder
3. Add commit message: "Initial commit"
4. Click "Commit changes"

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" (gear icon)
3. Scroll down and click "Pages" in the left sidebar
4. Under "Source":
   - Select branch: `main`
   - Select folder: `/ (root)`
5. Click "Save"
6. Wait 1-2 minutes for deployment

### 4. Access Your Website

Your site will be available at:
```
https://YOUR_USERNAME.github.io/YOUR_REPO/
```

For example:
```
https://johnsmith.github.io/ryder-entertainment/
```

## Custom Domain (Optional)

### Using GitHub Pages Custom Domain

1. Purchase a domain from a domain registrar
2. In your repository Settings > Pages:
   - Enter your custom domain (e.g., `www.ryderentertainment.com`)
   - Click "Save"
3. Configure DNS settings with your domain registrar:
   - Add a CNAME record pointing to `YOUR_USERNAME.github.io`
   - Or add A records pointing to GitHub's IP addresses

### DNS Configuration Example

For `www.ryderentertainment.com`:
```
Type: CNAME
Name: www
Value: YOUR_USERNAME.github.io
```

For `ryderentertainment.com` (apex domain):
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

## Troubleshooting

### Site Not Loading

- Wait a few minutes after enabling GitHub Pages
- Check that `index.html` is in the root directory
- Verify the repository is public
- Check the Actions tab for build errors

### Video Not Playing

- Ensure `hero-bg.mp4` is in the same directory as `index.html`
- Check file size (GitHub has a 100MB file limit)
- Consider using Git LFS for large video files

### HTTPS Certificate

- GitHub Pages automatically provides HTTPS
- It may take up to 24 hours for the certificate to be issued
- Check "Enforce HTTPS" in Settings > Pages after certificate is issued

## Using Git LFS for Large Video Files

If your video file is larger than 50MB:

```bash
# Install Git LFS
git lfs install

# Track video files
git lfs track "*.mp4"

# Add .gitattributes
git add .gitattributes

# Add and commit video file
git add hero-bg.mp4
git commit -m "Add video file with Git LFS"
git push
```

## Updating Your Website

After making changes:

```bash
git add .
git commit -m "Description of changes"
git push
```

Changes will be live in 1-2 minutes!

## Performance Optimization

1. **Compress video**: Use a tool like HandBrake to reduce file size
2. **Enable caching**: GitHub Pages handles this automatically
3. **Optimize images**: Use WebP format where possible
4. **Minify code**: Consider minifying HTML/CSS for production

## Support

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Git LFS Documentation](https://git-lfs.github.com/)
- Open an issue in this repository for questions
