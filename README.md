Opauth-mixi
=============
[Opauth][1] strategy for mixi Graph API.

Implemented based on http://developer.mixi.co.jp/connect/mixi_graph_api/ using OAuth 2.0.

Opauth is a multi-provider authentication framework for PHP.

Getting started
----------------
1. Install Opauth-mixi:
   ```bash
   cd path_to_opauth/Strategy
   git clone git://github.com/ritou/opauth-mixi.git Mixi
   ```

2. Create a mixi Graph API Service at https://sap.mixi.jp/home.pl
   - Select 'mixi Graph API' tab and create new service
   - Make sure that redirect URI is set to actual OAuth 2.0 callback URL, usually `http://path_to_opauth/mixi/oauth2callback`

   
3. Configure Opauth-Mixi strategy.

4. Direct user to `http://path_to_opauth/mixi` to authenticate


Strategy configuration
----------------------

Required parameters:

```php
<?php
'Mixi' => array(
	'client_id' => 'YOUR CLIENT ID',
	'client_secret' => 'YOUR CLIENT SECRET'
)
```

Optional parameters:
`scope`,`state`


References
----------
- [mixi Graph API](http://developer.mixi.co.jp/connect/mixi_graph_api/)
- [mixi Graph API Authentication and Authorization](http://developer.mixi.co.jp/connect/mixi_graph_api/api_auth/)

License
---------
Opauth-mixi is MIT Licensed  
Copyright © 2012 Ryo Ito (http://d.hatena.ne.jp/ritou)

[1]: https://github.com/uzyn/opauth
