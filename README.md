# Drupal 7 on OpenShift

### Git commands

This repo was created with the following commands:

```
git remote add -f drupal https://github.com/pressflow/7.git
git subtree add --prefix php drupal pressflow-7.23 --squash
```

When a new Drupal version (like 7.26) comes out, you should be able to upgrade it with the following command:

```
git remote add -f drupal https://github.com/pressflow/7.git
git subtree merge --prefix=php pressflow-7.26 --squash
```

### Creating an app

If you are using OpenShift Online, do the following:

`rhc app-create drupal php-5.3 mysql-5.5 cron https://cartreflect-claytondev.rhcloud.com/reflect?github=smerrill/openshift-community-pressflow7 --from-code=https://github.com/smerrill/pressflow-7-quickstart.git`

If you are using OpenShift Origin or Enterprise, do the following:

`rhc app-create drupal php-5.3 mysql-5.1 cron https://cartreflect-claytondev.rhcloud.com/reflect?github=smerrill/openshift-community-pressflow7 --from-code=https://github.com/smerrill/pressflow-7-quickstart.git`
