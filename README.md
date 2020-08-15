# accessinfo.hk

This repository contains the theme for customising accessinfo.hk, the website for making Code of Access to Information requests in Hong Kong.

## Deployment

We use [Capistrano](https://alaveteli.org/docs/installing/deploy/#capistrano) to deploy accessinfo.hk. We deploy the [`production`](https://github.com/Civicsight/alaveteli/tree/production) branch of [our fork of Alaveteli](https://github.com/Civicsight/alaveteli). This allows us to control the version we're deploying by updating the version of the `production` branch.

Our site is configured to deploy this theme from the `master` branch.

To deploy using Capistrano you'll need the following `config/deploy.yml` on your local machine:

```yaml
production:
  repository: git://github.com/Civicsight/alaveteli.git
  branch: production
  server: accessinfo.hk
  user: alaveteli
  rails_env: production
  deploy_to: /var/www/alaveteli
  daemon_name: alaveteli
```

You'll also need your SSH key added to the `alaveteli` user.

## Copyright and license

Copyright (c) 2011 mySociety, released under the MIT license

Copyright (c) 2015 Guy Freeman, released under the MIT license
