# 🚀 GitHub Profile Setup Guide

This guide will help you set up all the automated GitHub Actions for your profile README.

## 📋 Table of Contents

1. [GitHub Actions Overview](#github-actions-overview)
2. [WakaTime Setup](#wakatime-setup)
3. [Enabling GitHub Actions](#enabling-github-actions)
4. [Customization](#customization)
5. [Troubleshooting](#troubleshooting)

---

## 🤖 GitHub Actions Overview

Your profile now includes 4 automated workflows:

| Workflow | Purpose | Frequency |
|----------|---------|-----------|
| **update-activity.yml** | Updates recent GitHub activity | Every 6 hours |
| **update-quote.yml** | Updates daily inspirational quote | Daily at midnight UTC |
| **update-wakatime.yml** | Updates coding time statistics | Every 4 hours |
| **snake-animation.yml** | Generates contribution snake animation | Daily |

---

## ⏱️ WakaTime Setup

WakaTime tracks your coding activity and displays beautiful stats on your profile.

### Step 1: Create WakaTime Account

1. Go to [wakatime.com](https://wakatime.com)
2. Sign up for a free account
3. Install WakaTime plugin for your code editor:
   - **VS Code**: Search "WakaTime" in extensions
   - **IntelliJ/PyCharm**: Install from plugins marketplace
   - **Other editors**: Check [WakaTime plugins](https://wakatime.com/plugins)

### Step 2: Get Your WakaTime API Key

1. Go to [WakaTime Settings](https://wakatime.com/settings/account)
2. Copy your **Secret API Key**
3. Keep this safe - you'll need it in the next step

### Step 3: Add Secret to GitHub

1. Go to your profile repository: `https://github.com/Maxwell-Fernandes/Maxwell-Fernandes`
2. Click **Settings** tab
3. Click **Secrets and variables** → **Actions**
4. Click **New repository secret**
5. Name: `WAKATIME_API_KEY`
6. Value: Paste your WakaTime API key
7. Click **Add secret**

---

## ✅ Enabling GitHub Actions

### Step 1: Enable Actions

1. Go to your repository
2. Click **Settings** tab
3. Click **Actions** → **General** (in left sidebar)
4. Under **Actions permissions**, select:
   - ✅ **Allow all actions and reusable workflows**
5. Under **Workflow permissions**, select:
   - ✅ **Read and write permissions**
   - ✅ **Allow GitHub Actions to create and approve pull requests**
6. Click **Save**

### Step 2: Trigger Workflows Manually (First Time)

1. Go to **Actions** tab in your repository
2. You'll see 4 workflows in the left sidebar
3. Click each workflow one by one:
   - Update GitHub Activity
   - Update Quote of the Day
   - Update WakaTime Stats
   - Generate Snake Animation
4. Click **Run workflow** → **Run workflow**
5. Wait for the green checkmark ✅

---

## 🎨 Customization

### Update Personal Information

Edit `README.md` and replace:

- `maxwell.fernandes@example.com` → Your real email
- `https://linkedin.com/in/maxwell-fernandes` → Your LinkedIn URL
- `https://twitter.com/maxwell_dev` → Your Twitter/X handle

### Change Theme Colors

All graphics use the **Tokyo Night** theme. To change:

1. Search for `theme=tokyonight` in README.md
2. Replace with other themes:
   - `radical`
   - `merko`
   - `gruvbox`
   - `onedark`
   - `cobalt`
   - `synthwave`
   - `dracula`

### Adjust Update Frequency

Edit workflow files in `.github/workflows/`:

```yaml
# Current: Every 6 hours
schedule:
  - cron: '0 */6 * * *'

# Change to every 12 hours:
schedule:
  - cron: '0 */12 * * *'

# Change to daily at 9 AM UTC:
schedule:
  - cron: '0 9 * * *'
```

### Add More Sections

You can add more dynamic sections:

- **Spotify**: [Spotify Now Playing](https://github.com/novatorem/novatorem)
- **Blog Posts**: [Blog Post Workflow](https://github.com/gautamkrishnar/blog-post-workflow)
- **Twitter**: [Twitter Embed](https://github.com/zhiiiyang/zhiiiyang)

---

## 🐛 Troubleshooting

### WakaTime Stats Not Showing

**Problem**: Stats show "No activity tracked yet"

**Solutions**:
1. ✅ Verify WakaTime plugin is installed and active in your editor
2. ✅ Check that you've added the `WAKATIME_API_KEY` secret correctly
3. ✅ Wait 24 hours for WakaTime to collect data
4. ✅ Run the "Update WakaTime Stats" workflow manually

### GitHub Activity Not Updating

**Problem**: Activity section shows placeholder text

**Solutions**:
1. ✅ Verify workflow permissions (read & write) are enabled
2. ✅ Check that the workflow ran successfully in Actions tab
3. ✅ Make sure the repository name matches your GitHub username
4. ✅ Run the workflow manually from Actions tab

### Snake Animation Not Appearing

**Problem**: Snake animation broken or not showing

**Solutions**:
1. ✅ Wait for the workflow to complete (check Actions tab)
2. ✅ Verify an `output` branch was created in your repository
3. ✅ Clear browser cache and refresh the page
4. ✅ Run the "Generate Snake Animation" workflow manually

### Workflows Not Running Automatically

**Problem**: Scheduled workflows aren't executing

**Solutions**:
1. ✅ Push a commit to trigger workflows initially
2. ✅ GitHub may disable scheduled workflows on inactive repos
3. ✅ Make sure Actions are enabled in repository settings
4. ✅ Check for any workflow errors in the Actions tab

---

## 📚 Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [WakaTime Documentation](https://wakatime.com/help)
- [GitHub Profile README Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/)
- [Shields.io Badge Generator](https://shields.io/)

---

## 🎉 You're All Set!

Your profile will now automatically update with:
- ⏱️ Real-time coding statistics
- 🎯 Recent GitHub activity
- 💡 Daily inspirational quotes
- 🐍 Animated contribution graph

**Need help?** Open an issue in this repository!

---

<div align="center">

### Made with ❤️ and GitHub Actions

</div>
