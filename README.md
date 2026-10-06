# QA fixtures

Public, harmless pages used by the whitelist-review-agent test environment.

Expected project-site base URL:

`https://lhs-git.github.io/qa-fixtures/`

Fixtures:

- `/blank.html` — HTTP 200 with an empty body.
- `/maintenance.html` — HTTP 200 maintenance-page text.
- `/prompt-injection.html` — HTTP 200 page containing untrusted prompt-injection text.
- `/download.csv` — HTTP 200 CSV download fixture with dummy data.
- `/this-page-does-not-exist` — expected HTTP 404 from the static host.

GitHub Pages cannot reliably produce arbitrary HTTP 403 or redirect-loop responses from static files. Those cases need a small serverless or HTTP fixture service; this repository only provides the static fixtures above.

Deployment is configured through GitHub Actions and GitHub Pages.
