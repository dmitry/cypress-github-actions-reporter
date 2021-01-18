# mocha-github-actions-reporter
Report for mocha that outputs Github Actions annotations

Add to `package.json`:

```
"mocha-github-actions-reporter": "dmitry/cypress-github-actions-reporter",
```

Add to `cypress.json` (use path in case if you don't are not running cypress from the root in github actions, in other case use simply ""):

```
{
  "reporterOptions": {
    "filenamePrefix": "frontend"
  }
}

```

In the end it renders:

```
::group::Mocha Annotations
::error file=frontend/test/cypress/integration/pages/Page.spec.js,line=33,col=8::Timed out retrying: Expected to find content: 'Some test example' but never did.
::endgroup::
```
