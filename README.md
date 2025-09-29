# Phonely Documentation

This repository contains the documentation for Phonely - AI phone agents and conversation flows.

## Development Setup

### Prerequisites

- Node.js (version 18.10.0 or higher)

### Installation

Install the [Mintlify CLI](https://www.npmjs.com/package/mintlify) to preview the documentation changes locally:

<CodeGroup>

```bash npm
npm i -g mintlify
```

```bash yarn
yarn global add mintlify
```

</CodeGroup>

### Running Locally

1. Go to the docs directory (where you can find `mint.json`) and run:

```bash
mintlify dev
```

The documentation website is now available at `http://localhost:3000`.

#### Custom Ports

Mintlify uses port 3000 by default. You can use the `--port` flag to customize the port:

```bash
mintlify dev --port 3333
```

You will see an error like this if you try to run Mintlify in a port that's already taken:

```md
Error: listen EADDRINUSE: address already in use :::3000
```

### Updating Mintlify

Each CLI is linked to a specific version of Mintlify. Please update the CLI if your local website looks different than production:

<CodeGroup>

```bash npm
npm i -g mintlify@latest
```

```bash yarn
yarn global upgrade mintlify
```

</CodeGroup>

## Deployment

Unlimited editors available under the [Startup Plan](https://mintlify.com/pricing).

You should see the following if the deploy successfully went through:

<Frame>
  <img src="/images/checks-passed.png" style={{ borderRadius: '0.5rem' }} />
</Frame>

### Publishing Changes

Install our Github App to auto propagate changes from your repo to your deployment. Changes will be deployed to production automatically after pushing to the default branch. Find the link to install on your [dashboard](https://dashboard.mintlify.com).

#### Clone your docs locally

During the onboarding process, we created a repository on your Github with your docs content. You can find this repository on our [dashboard](https://dashboard.mintlify.com). To clone the repository locally, follow these [instructions](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) in your terminal.

#### Push your changes

[Commit and push your changes to Git](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository#about-git-push) for your changes to update in your docs site. If you push and don't see that the Github app successfully deployed your changes, you can also manually update your docs through our [dashboard](https://dashboard.mintlify.com).

## Updating Your Docs

Add content directly in your files with MDX syntax and React components. You can use any of our components, or even build your own.

### Available Features

- **Style Your Docs** - Add flair to your docs with personalized branding
- **Add API Endpoints** - Implement your OpenAPI spec and enable API user interaction
- **Integrate Analytics** - Draw insights from user interactions with your documentation
- **Host on a Custom Domain** - Keep your docs on your own website's subdomain

## Troubleshooting

Here's how to solve some common problems when working with the CLI:

### Mintlify is not loading
Update to Node v18. Run `mintlify install` and try again.

### No such file or directory on Windows
Go to the `C:/Users/Username/.mintlify/` directory and remove the `mint` folder. Then Open the Git Bash in this location and run `git clone https://github.com/mintlify/mint.git`.

Repeat step 3.

### Getting an unknown error
Try navigating to the root of your device and delete the ~/.mintlify folder. Then run `mintlify dev` again.

### Other Common Issues

- **Mintlify dev isn't running** - Run `mintlify install` it'll re-install dependencies.
- **Page loads as a 404** - Make sure you are running in a folder with `mint.json`

Curious about what changed in a CLI version? [Check out the CLI changelog.](/changelog/command-line)