# ISRAS Adoption Status

## Current status

`Iron-Signal-Systems/security-governance` is **not ISRAS-adopted**.

This repository is the organizational security-governance boundary. It shall not
claim an accepted ISRAS project pin unless an exact accepted ISRAS release
actually supports this repository and its authorized adoption process is
completed and verified.

## Current accepted adoption boundary

The currently accepted Engineering Standards release used by ISS-ENG-001 is:

`isras-v26.08.05`

Its accepted source commit is:

`f375b397a3039d82e96d76f269b444bef16adeb1`

The accepted 26.08.05 first-adoption boundary supports an existing Iron Signal
Systems **Go repository** through the exact release validator and explicit
`--go-defaults` initialization.

That accepted boundary does not implement non-Go initialization.

## Security-governance disposition

This repository is not a Go software project and is not converted into one merely
to satisfy an adoption mechanism.

Therefore:

- no dummy `go.mod` shall be created;
- no dummy Go source shall be created;
- `.isras/` shall not be hand-authored to imitate adoption;
- an Engineering Standards development branch shall not be used as accepted
  adoption authority; and
- the repository shall not claim ISRAS adoption while no accepted profile
  supports its actual repository boundary.

ISS-ENG-001 governs how this repository consumes and records authoritative ISRAS
engineering results. That organizational relationship does not itself make this
repository an ISRAS-adopted consuming project.

## Re-evaluation trigger

Reevaluate this status when:

- an accepted ISRAS release provides a profile that legitimately supports this
  repository;
- this repository materially changes its actual engineering boundary; or
- a governed decision changes whether consuming-project ISRAS adoption applies.

Until then, the truthful state is:

`PROFILE_NOT_CURRENTLY_SUPPORTED`
