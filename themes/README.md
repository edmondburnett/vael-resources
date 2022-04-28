# How to install the theme

This will set our theme as the default and the one that is used publicly. Eventually this should be handled by ansible.

Copy `vvvv.scss` to `app/javascript/styles/vvvv.scss`

Copy `themes.yml` to `config/themes.yml`

Copy `en.yml` to `config/locales/en.yml`

To have this take effect you will need to rebuild the webpack assets on the server with `RAILS_ENV=production bundle exec rake assets:precompile` then restart the web application. Clearing the cache can be done if needed with `rake assets:clean`.
