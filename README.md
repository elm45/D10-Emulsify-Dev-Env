# Drupal 10 Dev Environment for Emulsify
This is a Drupal 10 environment set up for developing components for Emulsify. The components will have their own repo and will not be saved here.

## Instal for Emulsify Developemnt
2. git clone the repo locally
3. cd into `D10-Emulsify-Dev-Env` and `composer install`
4. `ddev start` to start environment
5. `ddev cim` to import config


### Composer
If composer install fails and asks for a token for github, try updating to the latest version of composer to resolve.

## Development and Maintenance of the Drupal Repo

### Install for Development and maintenance
1. Fork the repo
2. git clone your fork locally
3. set the remote upstream
3. cd into `D10-Emulsify-Dev-Env` and `composer install`
4. `ddev start` to start environment
5. `ddev cim` to import config

### Emulsify Dev Theme
The Emulsify Dev Theme was created using Emulsify CLI using the following the [instructions in the Emulsify documentation](https://docs.emulsify.info/emulsify-drupal/emulsify-drupal).

The `.info` file was hand updated to be D10 compatible by updating the core_version_requirement line to include 10:

`core_version_requirement: ^8 || ^9 || ^10`

### Emulsify Twig Module
The Emulsify Twig module is not D10 compatible. There is an issue and a commit for D10 compatibility in the github repo that hasn't been merged so in the interim, we are using a forked version that we maintain.

When the real module has been updated, composer should be updated to stop using our github fork and should go back to using to the original module. To do this, set the version to the latest version on drupal and remove the additiona repo in composer.json: "https://github.com/elm45/emulsify_twig.git"