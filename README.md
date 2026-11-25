# ENP 2.0 vs BMC Validator

Static site, no build step. All processing happens in the browser; files are never uploaded.

## Deploy
**Vercel CLI**
```
npm i -g vercel
cd enp-bmc-validator
vercel          # preview
vercel --prod   # production
```
When asked, accept the defaults (no framework, no build command, output directory `.`).

**GitHub**: push this folder to a repo, then in Vercel choose *Add New → Project → Import*.
Framework preset: *Other*. Leave build command and output directory empty.

## Run locally
```
npx serve .
```

## Defaults (editable on the page)
- ENP 2.0: `Water ID`, `Total Dues`
- BMC: `UPDATED_CONNECTIONID`, `TOTAL_DUE`
- Result: TRUE (match) / FALSE (differs) / N/A (missing in one file)
