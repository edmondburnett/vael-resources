# Tech/Admin things

Rebuilding CSS, HTML, text assets:

`RAILS_ENV=production bundle exec rake assets:precompile && sudo systemctl restart mastodon-web`


If you get errors about missing node_modules while rebuilding and compiling assets, from the project dir do:

`yarn config set nodeLinker node-modules`


If CSS/resources are 404'ing / not loading after rebuilding:

- Make sure all paths in the nginx config are correct


# Email

Setting up a new email account in mysql:

- `select * from virtual_domains;`
- If adding a new domain name, choose an unused ID
- `INSERT INTO `mailserver`.`virtual_domains` (`id` ,`name`) VALUES ('<id>', '<domain name>');`

- `select * from virtual_users;`
- Choose an unused ID
- `INSERT INTO `mailserver`.`virtual_users` (`id` ,`domain_id`, `password`, `email`) VALUES ('<id>', <domain_id>', '<encrypted password>', '<email/login>');`

- `select * from virtual_aliases;`
- Choose an unused ID
- `INSERT INTO `mailserver`.`virtual_aliases` (`id`, `domain_id`, `source`, `destination`) VALUES ('<id>', '<domain_id>', '<new alias email address>', '<existing mailbox email address>');`

