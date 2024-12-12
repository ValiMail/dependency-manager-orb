# valimail/dependency-manager - CircleCI Orb

[![CircleCI](https://circleci.com/gh/ValiMail/dependency-manager-orb.svg?style=svg&circle-token=CCIPRJ_52w9NUfpNFGfikTxqmEGps_71de7acbfb47a8c93958c5d350aa3711f3105166)](https://circleci.com/gh/ValiMail/dependency-manager-orb)

CircleCI Orb for managing dependencies like Ruby gems and JS packages.

Published at https://circleci.com/orbs/registry/orb/valimail/dependency-manager

The following repos utilize `dependency-manager-orb`:
- auth_manager
- coppertonetone
- dns_adapter
- dmarc_creator
- dmarc_ingester
- domain_email_auth_analyzer
- domain_iq_service
- domain_name_util
- mimir
- sender_id

## Development

Work on files in the `src` directory and when you're ready you can "pack",
"validate", and "publish" the orb.

```bash
# Set up CircleCI CLI

# Install CircleCI CLI via brew
brew install circleci

# Get a token
circleci setup
```

```bash
# Build orb.yml from files in src folder
circleci config pack src > orb.yml

# Validate orb.yml
circleci orb validate orb.yml

# For a mutable "dev" version, increment DEV_ORB_VERSION (below) and publish orb.yml.
DEV_ORB_VERSION=dev:0.5.19
circleci orb publish orb.yml valimail/dependency-manager@$DEV_ORB_VERSION

# For an immutable release, increment ORB_VERSION (below) and publish orb.yml.
# Note: only GitHub admins of ValiMail can do this currently.
ORB_VERSION=0.5.19
circleci orb publish orb.yml valimail/dependency-manager@$ORB_VERSION

# Update version for tests in .circleci/config.yml
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
