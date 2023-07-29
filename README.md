# What?
- This repo is a copy of https://git.drupalcode.org/project/promote_disable
- Original Drupal module: https://www.drupal.org/project/promote_disable

# Why?
- Can't fork modules on git.drupalcode.org
- Maintainer did not validate D10 patch
- Can't require the module and apply the patch lately because of `^9` requirement not met in D10 installation

# Modifications:
- Created a new branch `10.x-1.x`
- Bumped version `^10` into `promote_disable.info.yaml`
- Tagged a new release `2.0.1`

# How to install?

1. Add the second block under `"repositories"` in your `composer.json`:

```json
    "repositories": [
        {
            "type": "composer",
            "url": "https://packages.drupal.org/8"
        },
        {
            "type": "package",
            "package": {
                "name": "germain-italic/drupal_module-promote_disable",
                "version": "2.0.1",
                "type":"drupal-custom-module",
                "source": {
                    "url": "https://github.com/germain-italic/drupal_module-promote_disable.git",
                    "type": "git",
                    "reference": "10.x-1.x"
                }
            }
        }
    ],
```

2. Run `composer require germain-italic/drupal_module-promote_disable:2.0.1`

# How to activate and use?

- Follow original instruction in [README.txt]README.txt
- TL;DR:
  - Activate in /admin/modules
  - Configure in /admin/config/content/promote_disable
