# HelloWorld — An app generated with [Kckstrt][]

## Setup
Run `script/setup` for a one-step complete installation.

## Asset Helpers
### `asset_path`
```erb
<img src="<%= asset_path 'kckstrt.png' %>" alt="Kckstrt">
```

`asset_path` uses Sprockets’ `digest_path` to find the asset within `app/assets/(images|javascripts|stylesheets)`.

--
### `javascript_include_tag` & `stylesheet_link_tag`
```erb
<head>
  <title>Kckstrt</title>
  <%= stylesheet_link_tag :styles %>
  <%# => <link rel="stylesheet" href="/assets/styles.css"> %>
</head>
<body>
  <%= javascript_link_tag :scripts %>
  <%# => <script src="/assets/scripts.js"></script> %>
</body>
```

--
### `inline_script_tag`
```erb
<%= inline_script_tag :scripts %>
<%# => <script>console.log('content of scripts.js')</script> %>
```

## Deployment
This app is [Heroku][]-ready.<br>
Don’t forget to set the `ENV['ASSET_HOST']` environment variable. We strongly suggest using [Amazon CloudFront][CloudFront] for a plug and play CDN host. Otherwise you’ll have to pre-compile your assets. Such script isn’t included.

### Staging
```sh
rake deploy:staging
```
Push `dev` to `origin/dev` & `staging/master`

### Production
```sh
rake deploy:production
```
Push `master` to `origin/master` & `production/master`

## Credits
[Rafael][rafBM] & [Etienne][EtienneLem]

[Kckstrt]: https://github.com/heliom/kckstrt
[Heroku]: http://www.heroku.com
[CloudFront]: http://aws.amazon.com/cloudfront
[rafBM]: https://github.com/rafBM
[EtienneLem]: https://github.com/EtienneLem
