# Celtic Support website

A fast, accessible, single-page information website for `celticsupport.com.au`. It uses plain HTML and CSS—no subscriptions, build tools, tracking, cookies or paid form service.

## Preview it

Open `index.html` in a web browser. All links and styling work directly from the folder.

## Publish free with GitHub Pages

1. Create or sign in to a free account at [github.com](https://github.com/).
2. Create a **new public repository**, for example `celtic-support-website`. Add no starter files.
3. Upload every file from this folder to the top level of the repository and commit the upload.
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**. Select the `main` branch and `/ (root)`, then save.
6. Wait a few minutes. GitHub will show the temporary `github.io` website address.

The included `CNAME` file tells GitHub Pages that the final address is `celticsupport.com.au`.

## Point the Wix domain to GitHub Pages

Before changing anything, take a screenshot of the existing Wix DNS records. Do **not** remove or change Microsoft 365 records such as MX, TXT, SPF, DKIM, autodiscover or verification records—those keep email working.

In Wix, open **Domains → celticsupport.com.au → Advanced → Manage DNS Records**. DNS screen names can change slightly over time.

For the root domain (`@`), add these four **A records**:

| Host | Value |
|---|---|
| `@` | `185.199.108.153` |
| `@` | `185.199.109.153` |
| `@` | `185.199.110.153` |
| `@` | `185.199.111.153` |

For `www`, add a **CNAME record**:

| Host | Value |
|---|---|
| `www` | `YOUR-GITHUB-USERNAME.github.io` |

Replace `YOUR-GITHUB-USERNAME` with the GitHub account name that owns the repository. Remove only older conflicting website A/AAAA records for `@` and a conflicting CNAME for `www`. Leave all email-related records untouched.

Back in **GitHub → repository Settings → Pages**, confirm the custom domain is `celticsupport.com.au`. After DNS is recognised, select **Enforce HTTPS**. DNS changes can take up to 48 hours, though they are often faster.

## Before launch

- Read all wording and confirm the services accurately reflect what Celtic Support offers.
- Have an Australian legal/compliance professional review the disclaimer and business obligations if needed.
- Test the email link on a phone and computer.
- Update the copyright year in `index.html` when required.

## Make future changes

Edit `index.html` for words and `styles.css` for appearance, then upload the changed file to the repository. GitHub Pages republishes automatically.
