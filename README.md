# Reddit Homelab Data Analyzer

Personal read-only research tool using Reddit API (PRAW) to analyze public data from homelab/tech subreddits.

## Purpose
- Fetch posts/comments from r/NixOS, r/selfhosted, r/homelab.
- Analyze trends (e.g., popular NixOS configs, Docker tools) for my self-hosted setup (Jellyfin, Pi-hole, Tailscale).
- Low-volume: &lt;50 API calls/day, no posting/modification.
- Data stored privately on NixOS homelab server.

## Compliance
- Adheres to Reddit Data API Terms and Responsible Builder Policy.
- Read-only access; respects rate limits.

## Example Usage
```python
import praw
reddit = praw.Reddit(...)  # OAuth script app
sub = reddit.subreddit('NixOS')
for post in sub.hot(limit=10):
    print(post.title)
```

No public data sharing.
