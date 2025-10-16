# Test PR for DesignCheck

This is a simple test folder to verify the DesignCheck GitHub App integration.

## Purpose

When you create a PR with this folder, DesignCheck should:
1. ✅ Receive the PR webhook
2. ✅ Capture screenshots of your application
3. ✅ Post a comment on the PR with the review link
4. ✅ Show the review in your `/reviews` dashboard

## How to Test

1. Create a new branch:
   ```bash
   git checkout -b test/designcheck-integration
   ```

2. Commit this folder:
   ```bash
   git add test-pr/
   git commit -m "Test: Add test folder for DesignCheck integration"
   ```

3. Push to GitHub:
   ```bash
   git push origin test/designcheck-integration
   ```

4. Open a Pull Request on GitHub

5. Check that DesignCheck comments on your PR with the review link!

## Expected Result

You should see a comment from the DesignCheck bot with:
- 📸 Screenshots of your app at different routes
- 📱 Multiple device views (Desktop, Mobile)
- 🔗 Link to full design review at designcheck.app

## Troubleshooting

If the bot doesn't comment:
- Check that the GitHub App is installed on the repository
- Verify webhook delivery in GitHub Settings → Webhooks
- Check server logs: `pm2 logs designcheck`
