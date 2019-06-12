# valimail/dependency-manager - CircleCI Orb

[![CircleCI](https://circleci.com/gh/ValiMail/dependency-manager-orb.svg?style=svg&circle-token=540455df00def7479a3c81c9ab9ac8ab4f810178)](https://circleci.com/gh/ValiMail/dependency-manager-orb)

CircleCI Orb for managing dependencies like Ruby gems and JS packages.

Published at https://circleci.com/orbs/registry/orb/valimail/dependency-manager

## Development

Work on files in the `src` directory and when you're ready you can "pack",
"validate", and "publish" the orb.

```bash
# Build orb.yml from files in src folder
circleci config pack src > orb.yml

# Validate orb.yml
circleci orb validate orb.yml

# Increment ORB_VERSION (below) and publish orb.yml.
# Note: only GitHub admins of ValiMail can do this currently.
ORB_VERSION=0.2.7
circleci orb publish orb.yml valimail/dependency-manager@$ORB_VERSION

# Update dependency-manager: version in .circlci/config.yml
```

## Setup

This was created using the following commands:

```bash
# Initial setup of valimail namespace
circleci namespace create valimail github ValiMail

# Create this orb
circleci orb create valimail/dependency-manager
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/ValiMail/dependency-manager-orb.
