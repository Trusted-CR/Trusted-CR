### Hi there 👋


## Trusted-CR migrator component
The migrator component is the trusted_cr binary that the user interacts with on the command line in the normal world. The migrator controls the other components and migrates the checkpoint data to the secure executor in the secure world via the TEE Client API.
https://github.com/Trusted-CR/trusted_cr


## Trusted-CR API
The Trusted-CR API offers developers two functions:
- Function trusted_cr_migrate_to_sw: to migrate to the secure world
- Function trusted_cr_migrate_back_to_nw: to migrate to the normal world

https://github.com/Trusted-CR/migration_api
