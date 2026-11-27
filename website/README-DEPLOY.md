# Preview and deploy EvidenceLab

Run these commands from the repository root with Quarto installed.

```sh
quarto render website
quarto preview website
```

The pull request build uploads the rendered site as the `evidencelab-preview` artifact. Download and extract it, then serve it locally with `python -m http.server 8000 --directory <extracted-directory>`. Open http://localhost:8000/ to review the site.

## Initial GitHub Pages deployment

1. After review and merge, open **Settings → Pages** and choose **GitHub Actions** as the source.
2. Open **Actions → EvidenceLab website → Run workflow**, select the default branch, and enable **Publish to GitHub Pages**.
3. Check the deployment URL in the workflow. The expected URL is https://amobionovo.github.io/EvidenceLab/.

## Future custom domain

When ready to switch, verify ownership of the custom domain in GitHub. In **Settings → Pages**, set the custom domain to `evidencelab.quantiuminsights.com`. At the DNS provider, add a CNAME for the `evidencelab` subdomain targeting `amobionovo.github.io`. Keep the apex and existing Squarespace records intact. Once GitHub validates the domain and provisions the certificate, enable **Enforce HTTPS**. Update `website.site-url` in `_quarto.yml` to `https://evidencelab.quantiuminsights.com/`, redeploy, and check the navigation and canonical URL.

