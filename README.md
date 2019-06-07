# valimail/dependency-manager - CircleCI Orb

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

# Increment ORB_VERSION (below) and publish orb.yml
ORB_VERSION=0.1.2
circleci orb publish orb.yml valimail/dependency-manager@$ORB_VERSION
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
