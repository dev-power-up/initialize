# Guidewire Software

> [Dev Power-Up! Launcher](https://github.com/dev-power-up/launcher) is a great addition to manage and run separate environments and workspaces.

We recommend a folder hierarchy similar to below. Extract the base Guidewire Software product into the appropriate folder. If using Dev Power-Up! Launcher, the full path will need to be referenced the related property file. 

```text
└── Guidewire
    └── Suite
        ├── BillingCenter
        ├── ClaimCenter
        ├── ContactManager
        ├── PolicyCenter
    └── Dev-Power-Up
```

## Configuration Setup

If creating a setup for configuration with your company, follow those instructions to manage the configuration within the version control system (i.e. Git or Subversion). Usually the managed parent folder is  ```modules/configuration``` but can vary.


## Sandbox Setup

Creating a local Sandbox of the base products can be done in several ways. 

### Option 1

This is our favorite option to organize a workspace. In this example, a separate Suite hierarchy is created under the root Guidewire folder.

```text
└── Guidewire
    └── Suite
        ├── BillingCenter
        ├── ClaimCenter
        ├── ContactManager
        ├── PolicyCenter
    └── Suite-SB
        ├── BillingCenter
        ├── ClaimCenter
        ├── ContactManager
        ├── PolicyCenter
    └── Dev-Power-Up
```

### Option 2

Folder organization is a matter of personal preference and Dev Power-Up! Launcher is flexible with any option. Most developers adhere to a Guidewire root folder with the product directly below. In this example, add base Guidewire products in separate unique folders within the parent Guidewire folder. 

```text
└── Guidewire
    ├── BillingCenter
    ├── ClaimCenter
    ├── ContactManager
    ├── PolicyCenter
    ├── SBBillingCenter
    ├── SBClaimCenter
    ├── SBContactManager
    ├── SBPolicyCenter
    └── Dev-Power-Up
```

### Option 3

Similar to Option 2, the Guidewire root folder holds the products directly beneath. In this example, create another root Guidewire folder with a second Dev Power-Up! configuration.

```text
└── Guidewire
    ├── BillingCenter
    ├── ClaimCenter
    ├── ContactManager
    ├── PolicyCenter
    └── Dev-Power-Up

└── GuidewireSB
    ├── BillingCenter
    ├── ClaimCenter
    ├── ContactManager
    ├── PolicyCenter
    └── Dev-Power-Up
```

!> Running a Sandbox version while running a configured version requires separate listening ports and database configurations to avoid collisions.