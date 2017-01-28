## Don't panic!

**Hints and tricks**

*Set the correct OAuth2 server FQDN to GeoServer*

```bash
$ sudo vi /usr/share/geoserver/data/security/filter/geonode-oauth2/config.xml
# edit the configuration of GeoServer security for the oauth2 provider
```

Change default with these values:

```xml
<!-- GeoNode accessTokenUri -->
<accessTokenUri>http://localhost:8888/o/token/</accessTokenUri>
<!-- GeoNode userAuthorizationUri -->
<userAuthorizationUri>http://localhost:8888/o/authorize/</userAuthorizationUri>
<!-- GeoServer Public URL -->
  <redirectUri>http://localhost:8888/geoserver</redirectUri>
<!-- GeoNode checkTokenEndpointUrl -->
<checkTokenEndpointUrl>http://localhost:8888/api/o/v4/tokeninfo/</checkTokenEndpointUrl>
<!-- GeoNode logoutUri -->
<logoutUri>http://localhost:8888/account/logout/</logoutUri>
```

