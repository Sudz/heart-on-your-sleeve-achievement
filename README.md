# Heart On Your Sleeve Achievement Guide

## Overview
The **Heart On Your Sleeve** achievement on GitHub is earned by reacting to comments and issues across public repositories (including your own) with a ❤️ (heart) emoji.

## How to Unlock the Achievement

### Manual Method
1. Navigate to any public GitHub repository discussion, issue, or pull request
2. Find comments from other users
3. Click on the "Add or remove reactions" button (usually represented by a smiley face icon)
4. Select the ❤️ (heart) emoji from the reaction menu
5. Repeat this process across multiple comments and issues
6. The achievement will be unlocked after reacting to a sufficient number of items

### Step-by-Step Example
1. Visit GitHub discussions, issues, or pull requests in public repositories
2. Look for the reaction button next to each comment
3. Click to open the emoji picker
4. Choose the ❤️ heart emoji
5. Continue reacting to various comments across different repositories

## Best Practices

### Do's
- ✅ React to comments that you genuinely appreciate or find helpful
- ✅ Spread reactions across multiple repositories and discussions
- ✅ React to both your own repository issues and others'
- ✅ Be authentic - only react when the content resonates with you
- ✅ Use reactions as a way to show support without cluttering threads with "+1" comments

### Don'ts
- ❌ Don't spam reactions just to get the achievement
- ❌ Don't react inappropriately to sensitive or serious discussions
- ❌ Don't use bots or automation that violates GitHub's Terms of Service
- ❌ Don't remove and re-add reactions repeatedly

## Automation Options

### Browser Extensions
While manual reactions are recommended for authenticity, some users explore automation:

**⚠️ Warning**: Automated interactions may violate GitHub's Terms of Service. Use at your own risk.

1. **Custom Browser Extensions**
   - Create a browser extension using the GitHub DOM structure
   - Target reaction buttons programmatically
   - Add delays to mimic human behavior
   - Must comply with GitHub's automation policies

2. **User Scripts (Tampermonkey/Greasemonkey)**
   - Write custom scripts to automate clicking
   - Use selectors to find reaction buttons
   - Implement rate limiting to avoid detection

### API Approach
GitHub provides an official API for reactions:

```bash
# Add a heart reaction to a comment
curl -X POST \
  -H "Authorization: token YOUR_PERSONAL_ACCESS_TOKEN" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/OWNER/REPO/issues/comments/COMMENT_ID/reactions \
  -d '{"content":"heart"}'
```

**API Reaction Content Types:**
- `heart` ❤️
- `+1` 👍
- `-1` 👎
- `laugh` 😄
- `hooray` 🎉
- `confused` 😕
- `rocket` 🚀
- `eyes` 👀

### Python Script Example
```python
import requests
import time

# Configuration
TOKEN = 'your_github_token'
HEADERS = {
    'Authorization': f'token {TOKEN}',
    'Accept': 'application/vnd.github.v3+json'
}

def add_heart_reaction(owner, repo, comment_id):
    url = f'https://api.github.com/repos/{owner}/{repo}/issues/comments/{comment_id}/reactions'
    data = {'content': 'heart'}
    response = requests.post(url, headers=HEADERS, json=data)
    return response.status_code == 201

# Example usage
# add_heart_reaction('octocat', 'hello-world', 12345)
```

### JavaScript Bookmarklet
Create a bookmarklet to quickly add heart reactions:

```javascript
javascript:(function(){
  const buttons = document.querySelectorAll('button[aria-label="heart"]');
  buttons.forEach((btn, index) => {
    setTimeout(() => btn.click(), index * 1000);
  });
})();
```

## Ethical Considerations

1. **Authenticity Matters**: Reactions should reflect genuine appreciation
2. **Community Guidelines**: Follow GitHub's community guidelines and ToS
3. **Rate Limiting**: Don't overwhelm servers with rapid-fire requests
4. **Meaningful Engagement**: Use achievements as motivation for real participation, not just collection

## Tips for Success

- Participate in discussions you care about
- React to helpful answers in GitHub Discussions
- Show appreciation for bug reports and feature requests
- Support open source maintainers by reacting to their updates
- Join the GitHub Community discussions to find more content

## Resources

- [GitHub Reactions Documentation](https://docs.github.com/en/rest/reactions)
- [GitHub Community Discussions](https://github.com/orgs/community/discussions)
- [GitHub REST API Reference](https://docs.github.com/en/rest)
- [GitHub Achievements Guide](https://github.com/Schweinepriester/github-profile-achievements)

## Conclusion

The Heart On Your Sleeve achievement celebrates positive engagement within the GitHub community. Whether you pursue it through manual reactions or explore automation options, remember that genuine participation enriches the open source ecosystem.

**Happy Reacting! ❤️**

---

*Last updated: October 26, 2025*
*Repository: github.com/Sudz/heart-on-your-sleeve-achievement*
