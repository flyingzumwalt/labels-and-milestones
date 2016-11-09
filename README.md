# labels-and-milestones

> Sync labels and milestones across Github repositories

This is a fork of [haadcode/labels-and-milestones](https://github.com/haadcode/labels-and-milestones). We are using it in a particular way. Check out the Readme in that repo for the "normal" usage instructions.

## Usage

### Prerequisites

- Set `GITHUB_TOKEN` env var to Github personal access token
- Install node/npm
- Clone this repo

### Syncing

#### Running locally

First install dependencies

```bash
npm install
```

Create a config file, or choose one of the existing config files like `js-ipfs.json` or `ipfs-pm-and-community.json`

Then run the sync tool, providing the config file you want to use

```bash
./node_modules/.bin/github-sync-labels-milestones -v -c your-config-file.json -t $GITHUB_TOKEN
```

This command will read `your-config-file.json` and sync the labels and milestones to the target repos.

#### Running via CI

This will need some work. See [haadcode/labels-and-milestones](https://github.com/haadcode/labels-and-milestones) for more info.
