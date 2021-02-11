# Trusted-CR Repository

This repository contains all the code for the Trusted-CR implementation.

## Trusted-CR migrator component
The migrator component is the trusted_cr binary that the user interacts with on the command line in the normal world. The migrator controls the other components and migrates the checkpoint data to the secure executor in the secure world via the TEE Client API.

https://github.com/Trusted-CR/trusted_cr

## Trusted-CR checkpointing & restoring component
Trusted-CR uses a modified version of CRIU as checkpointing and restoring component. CRIU has been modified to supports executing a single system call and checkpointing a binary at the start.

https://github.com/Trusted-CR/criu/tree/v3.15_trusted-cr

## Trusted-CR secure execution component
The secure execution component is responsible for restoring the checkpoint in the secure world and for migrating the updated state back to the normal world after execution finishes.

https://github.com/Trusted-CR/optee_os/blob/trusted_cr/core/pta/trusted_cr.c

## Modified OP-TEE
OP-TEE has been modified to support checkpointing binaries running in S-EL0.

https://github.com/Trusted-CR/optee_os/tree/trusted_cr

## Trusted-CR API
The Trusted-CR API offers developers two functions:
- Function trusted_cr_migrate_to_sw: to migrate to the secure world
- Function trusted_cr_migrate_back_to_nw: to migrate to the normal world

https://github.com/Trusted-CR/migration_api
