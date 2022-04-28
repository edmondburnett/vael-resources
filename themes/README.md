# How to install the theme

This will set our theme as the default and the one that is used publicly. Eventually this should be handled by ansible.

Copy `vvvv.scss` to `app/javascript/styles/vvvv.scss`

Copy `themes.yml` to `config/themes.yml`

Copy `en.yml` to `config/locales/en.yml`

To have this take effect you will need to rebuild the webpack assets on the server then restart the application.
