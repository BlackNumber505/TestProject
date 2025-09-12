Return error if we try to initialize storage with new genesis (#4547)
## Motivation

#4543 started treating
storage initialization as idempotent but it is still useful to detect if
we try to initialize it for a network that has a different Genesis
config.

## Proposal

Return (and log) an error if the new genesis config is different from
the one our storage is initialized with.

## Test Plan

CI

## Release Plan

- These changes should be backported to the latest `testnet` branch,
then
    - be released in a new SDK,


## Links
#4543
- [reviewer
checklist](https://github.com/linera-io/linera-protocol/blob/main/CONTRIBUTING.md#reviewer-checklist)
