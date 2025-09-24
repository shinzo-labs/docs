# Mintlify Starter Kit

Use the starter kit to get your docs deployed and ready to customize.

Click the green **Use this template** button at the top of this repo to copy the Mintlify starter kit. The starter kit contains examples with

- Guide pages
- Navigation
- Customizations
- API reference pages
- Use of popular components

**[Follow the full quickstart guide](https://starter.mintlify.com/quickstart)**

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```
npm i -g mint
```

Run the following command at the root of your documentation, where your `docs.json` is located:

```
mint dev
```

View your local preview at `http://localhost:3000`.

## Publishing changes

Install our GitHub app from your [dashboard](https://dashboard.mintlify.com/settings/organization/github-app) to propagate changes from your repo to your deployment. Changes are deployed to production automatically after pushing to the default branch.

## Need help?

### Troubleshooting

- If your dev environment isn't running: Run `mint update` to ensure you have the most recent version of the CLI.
- If a page loads as a 404: Make sure you are running in a folder with a valid `docs.json`.

### Resources
- [Mintlify documentation](https://mintlify.com/docs)


---
title: 'Development'
description: 'Preview changes locally to update your docs'
---

<Info>
  **Prerequisites**:
  - Node.js version 19 or higher
  - A docs repository with a `docs.json` file
</Info>

Follow these steps to install and run Mintlify on your operating system.

<Steps>
<Step title="Install the Mintlify CLI">

```bash
npm i -g mint
```
</Step>

<Step title="Preview locally">

Navigate to your docs directory where your `docs.json` file is located, and run the following command:

```bash
mint dev
```

A local preview of your documentation will be available at `http://localhost:3000`.

</Step>
</Steps>

## Custom ports

By default, Mintlify uses port 3000. You can customize the port Mintlify runs on by using the `--port` flag. For example, to run Mintlify on port 3333, use this command:

```bash
mint dev --port 3333
```

If you attempt to run Mintlify on a port that's already in use, it will use the next available port:

```md
Port 3000 is already in use. Trying 3001 instead.
```

## Mintlify versions

Please note that each CLI release is associated with a specific version of Mintlify. If your local preview does not align with the production version, please update the CLI:

```bash
npm mint update
```

## Validating links

The CLI can assist with validating links in your documentation. To identify any broken links, use the following command:

```bash
mint broken-links
```

## Deployment

If the deployment is successful, you should see the following:

<Frame>
  <img src="/images/checks-passed.png" alt="Screenshot of a deployment confirmation message that says All checks have passed." style={{ borderRadius: '0.5rem' }} />
</Frame>

## Code formatting

We suggest using extensions on your IDE to recognize and format MDX. If you're a VSCode user, consider the [MDX VSCode extension](https://marketplace.visualstudio.com/items?itemName=unifiedjs.vscode-mdx) for syntax highlighting, and [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) for code formatting.

## Troubleshooting

<AccordionGroup>
  <Accordion title='Error: Could not load the "sharp" module using the darwin-arm64 runtime'>

    This may be due to an outdated version of node. Try the following:
    1. Remove the currently-installed version of the CLI: `npm remove -g mint`
    2. Upgrade to Node v19 or higher.
    3. Reinstall the CLI: `npm i -g mint`
  </Accordion>

  <Accordion title="Issue: Encountering an unknown error">
  
    Solution: Go to the root of your device and delete the `~/.mintlify` folder. Then run `mint dev` again.
  </Accordion>
</AccordionGroup>

Curious about what changed in the latest CLI version? Check out the [CLI changelog](https://www.npmjs.com/package/mintlify?activeTab=versions).
