# home assistant setup

Home assistant has very limited remote login.
users cant be created or revoked by an automated system by homme assistant
so users inside home assistant need to be created manualy. 
you cant log them out disableing a discord group if already loged in.


## config 
set up [ldap-discord-oath](https://github.com/project-chrimera/ldap-discord-oath)

install [openid hacs](https://github.com/cavefire/hass-openid) on home assistant

setup a config

```
openid:
  client_id: dummy
  client_secret: dummy
  configure_url: "https://auth.yetanotherprojecttosavetheworld.org/auth/.well-known/openid-configuration"
  username_field: "preferred_username"
  scope: "openid email profile"
  block_login: false
  openid_text: "Login with Discord"

```

add home assistant users with the binded email as username
