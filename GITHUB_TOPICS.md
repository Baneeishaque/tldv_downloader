# GitHub Topics and Tags for TLDV Downloader

This document provides the recommended GitHub topics for this repository and various methods to add them.

## 📋 Suggested GitHub Topics

Based on deep analysis of this repository, the following GitHub topics are recommended:

### Core Functionality Topics
| Topic | Description |
|-------|-------------|
| `tldv` | TLDV platform-specific identifier |
| `video-downloader` | Main purpose of the tool |
| `meeting-recorder` | Downloads meeting recordings |
| `hls-downloader` | Downloads HLS streams |
| `m3u8-downloader` | Downloads M3U8 playlists |

### Technology Stack Topics
| Topic | Description |
|-------|-------------|
| `python` | Main programming language |
| `python3` | Python 3.7+ required |
| `ffmpeg` | Uses FFmpeg for video processing |
| `n-m3u8dl-re` | Uses N_m3u8DL-RE for downloads |

### Feature-Related Topics
| Topic | Description |
|-------|-------------|
| `batch-downloader` | Supports batch downloads |
| `video-download` | Downloads video content |
| `meeting-recordings` | Handles meeting recordings |
| `automation` | Automation tool for downloads |
| `parallel-downloads` | Supports parallel downloading |

### Platform Topics
| Topic | Description |
|-------|-------------|
| `windows` | Windows platform support |
| `macos` | macOS platform support |
| `linux` | Linux platform support |
| `cross-platform` | Works on all major platforms |

### Additional Topics
| Topic | Description |
|-------|-------------|
| `cli-tool` | Command-line interface tool |
| `hls` | HLS protocol support |
| `m3u8` | M3U8 playlist support |
| `requests` | Uses Python requests library |

## 🎯 Complete List of Recommended Topics

```
tldv, video-downloader, meeting-recorder, hls-downloader, m3u8-downloader, 
python, python3, ffmpeg, n-m3u8dl-re, batch-downloader, video-download, 
meeting-recordings, automation, parallel-downloads, windows, macos, linux, 
cross-platform, cli-tool, hls, m3u8
```

**Note:** GitHub allows a maximum of 20 topics per repository. The above list contains 21 topics, so you may need to prioritize based on your preference.

### Top 20 Prioritized Topics (Recommended)

```
tldv, video-downloader, meeting-recorder, hls-downloader, m3u8-downloader, 
python, python3, ffmpeg, batch-downloader, video-download, meeting-recordings, 
automation, parallel-downloads, cross-platform, cli-tool, hls, m3u8, 
windows, macos, linux
```

---

## 🛠️ Methods to Add GitHub Topics

### Method 1: GitHub Web Interface (Easiest)

1. Go to your repository: https://github.com/Baneeishaque/tldv_downloader
2. Click on the **⚙️ gear icon** next to "About" in the right sidebar
3. In the "Topics" field, type your topics separated by commas or press Enter after each
4. Click **Save changes**

### Method 2: GitHub CLI (gh)

First, install the GitHub CLI if not already installed:

```bash
# macOS
brew install gh

# Windows (Chocolatey)
choco install gh

# Windows (winget)
winget install --id GitHub.cli

# Linux (Debian/Ubuntu)
sudo apt install gh

# Linux (Fedora)
sudo dnf install gh
```

Then authenticate:

```bash
gh auth login
```

#### Add Topics Using GitHub CLI

```bash
# Replace topics with specific topics
gh repo edit Baneeishaque/tldv_downloader --add-topic "tldv"
gh repo edit Baneeishaque/tldv_downloader --add-topic "video-downloader"
gh repo edit Baneeishaque/tldv_downloader --add-topic "meeting-recorder"
gh repo edit Baneeishaque/tldv_downloader --add-topic "hls-downloader"
gh repo edit Baneeishaque/tldv_downloader --add-topic "m3u8-downloader"
gh repo edit Baneeishaque/tldv_downloader --add-topic "python"
gh repo edit Baneeishaque/tldv_downloader --add-topic "python3"
gh repo edit Baneeishaque/tldv_downloader --add-topic "ffmpeg"
gh repo edit Baneeishaque/tldv_downloader --add-topic "batch-downloader"
gh repo edit Baneeishaque/tldv_downloader --add-topic "video-download"
gh repo edit Baneeishaque/tldv_downloader --add-topic "meeting-recordings"
gh repo edit Baneeishaque/tldv_downloader --add-topic "automation"
gh repo edit Baneeishaque/tldv_downloader --add-topic "parallel-downloads"
gh repo edit Baneeishaque/tldv_downloader --add-topic "cross-platform"
gh repo edit Baneeishaque/tldv_downloader --add-topic "cli-tool"
gh repo edit Baneeishaque/tldv_downloader --add-topic "hls"
gh repo edit Baneeishaque/tldv_downloader --add-topic "m3u8"
gh repo edit Baneeishaque/tldv_downloader --add-topic "windows"
gh repo edit Baneeishaque/tldv_downloader --add-topic "macos"
gh repo edit Baneeishaque/tldv_downloader --add-topic "linux"
```

#### One-liner to Add All Topics (Recommended)

```bash
# Add all recommended topics at once
for topic in tldv video-downloader meeting-recorder hls-downloader m3u8-downloader python python3 ffmpeg batch-downloader video-download meeting-recordings automation parallel-downloads cross-platform cli-tool hls m3u8 windows macos linux; do
  gh repo edit Baneeishaque/tldv_downloader --add-topic "$topic"
done
```

### Method 3: GitHub REST API

Using curl with a Personal Access Token (PAT):

```bash
# Replace YOUR_TOKEN with your GitHub Personal Access Token
# Token needs 'repo' scope

curl -L \
  -X PUT \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/Baneeishaque/tldv_downloader/topics \
  -d '{"names":["tldv","video-downloader","meeting-recorder","hls-downloader","m3u8-downloader","python","python3","ffmpeg","batch-downloader","video-download","meeting-recordings","automation","parallel-downloads","cross-platform","cli-tool","hls","m3u8","windows","macos","linux"]}'
```

### Method 4: Python Script Using PyGithub

```python
from github import Github

# Replace with your GitHub Personal Access Token
g = Github("YOUR_TOKEN")

repo = g.get_repo("Baneeishaque/tldv_downloader")

topics = [
    "tldv", "video-downloader", "meeting-recorder", "hls-downloader", 
    "m3u8-downloader", "python", "python3", "ffmpeg", "batch-downloader", 
    "video-download", "meeting-recordings", "automation", "parallel-downloads", 
    "cross-platform", "cli-tool", "hls", "m3u8", "windows", "macos", "linux"
]

repo.replace_topics(topics)
print("Topics updated successfully!")
```

### Method 5: Using GitHub GraphQL API

```graphql
mutation {
  updateRepository(input: {
    repositoryId: "YOUR_REPO_NODE_ID",
    description: "A powerful Python script to download videos from tldv.io with support for both single and parallel batch downloads"
  }) {
    repository {
      id
    }
  }
}
```

Note: Topics cannot be directly set via GraphQL; use the REST API for topics.

### Method 6: GitHub Actions Workflow

Create `.github/workflows/update-topics.yml`:

```yaml
name: Update Repository Topics

on:
  workflow_dispatch:

jobs:
  update-topics:
    runs-on: ubuntu-latest
    steps:
      - name: Update Topics
        uses: actions/github-script@v7
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          script: |
            await github.rest.repos.replaceAllTopics({
              owner: context.repo.owner,
              repo: context.repo.repo,
              names: [
                'tldv', 'video-downloader', 'meeting-recorder', 'hls-downloader',
                'm3u8-downloader', 'python', 'python3', 'ffmpeg', 'batch-downloader',
                'video-download', 'meeting-recordings', 'automation', 'parallel-downloads',
                'cross-platform', 'cli-tool', 'hls', 'm3u8', 'windows', 'macos', 'linux'
              ]
            });
            console.log('Topics updated successfully!');
```

---

## 📊 Topic Categories Summary

| Category | Topics Count |
|----------|-------------|
| Core Functionality | 5 |
| Technology Stack | 4 |
| Features | 5 |
| Platforms | 4 |
| Additional | 4 |
| **Total** | **22** |

## ⚠️ Important Notes

1. **Maximum Topics**: GitHub allows a maximum of **20 topics** per repository
2. **Topic Format**: Topics must be lowercase and can contain letters, numbers, and hyphens
3. **Topic Length**: Each topic can be up to 50 characters long
4. **Visibility**: Topics help users discover your repository through GitHub search and topic pages

## 🔍 Related GitHub Topic Pages

After adding topics, your repository will appear on these GitHub topic pages:

- https://github.com/topics/python
- https://github.com/topics/video-downloader
- https://github.com/topics/ffmpeg
- https://github.com/topics/hls
- https://github.com/topics/m3u8
- And more...

---

*Last Updated: December 2025*
