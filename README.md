# Tools for static testing Magento code

To use this package, you need to have access to Magento composer repository. Either do this on project level or set it up globally:

```
composer global config repositories.magento composer https://repo.magento.com/
```

Afterwards, simply require this package (again globally if you do not want to bloat projects):
```
composer global require inchoodev/lmeqp
```

Then, provided that `vendor/bin` has been added to your `$PATH` (if not, specify full path to `phpcs`), run following:

```
phpcs --config-set installed_paths ../../inchoodev/lmeqp,../../magento/marketplace-eqp
```

To verify installation is running, execute:

```
phpcs -i
```

Which should list (among others) following: _lMEQP2, lMEQP1, MEQP2 and MEQP1_.
