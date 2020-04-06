# Guidewire Software

> [QuickCenter Launcher](https://github.com/QuickCenter/launcher) is a great addition to manage and run separate environments and workspaces.

We recommend a folder hierarchy similar to below. Extract the base Guidewire Software product into the appropriate folder. If using QuickCenter Launcher, the full path will need to be referenced the related property file. 

```text
└── Guidewire
    ├── BillingCenter
    ├── ClaimCenter
    ├── ContactManager
    ├── PolicyCenter
    └── QuickCenter
```

## Configuration Setup

If creating a setup for configuration with your company, follow those instructions to manage the configuration within the version control system (i.e. Git or Subversion). Usually the managed parent folder is  ```modules/configuration``` but can vary.


## Sandbox Setup

Creating a local Sandbox of the base products can be done in several ways. 

### Option 1

Create a separate hierarchy 

```text
└── GuidewireSB
    ├── BillingCenter
    ├── ClaimCenter
    ├── ContactManager
    ├── PolicyCenter
    └── QuickCenter
```

### Option 2

Add the base Guidewire products in separate folders within the parent Guidewire folder. 

```text
└── Guidewire
    ├── BillingCenter
    ├── ClaimCenter
    ├── ContactManager
    ├── PolicyCenter
    ├── QuickCenter
    ├── SBBillingCenter
    ├── SBClaimCenter
    ├── SBContactManager
    └── SBPolicyCenter
```
!> Running a Sandbox version while running a configured version requires separate listening ports to avoid collisions. (A future guide will address this.)
