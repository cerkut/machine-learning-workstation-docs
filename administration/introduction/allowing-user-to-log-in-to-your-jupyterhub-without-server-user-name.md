# Allowing user to log in to your JupyterHub without server user name

## Allowing anyone to log in to your JupyterHub[@tljh](https://tljh.jupyter.org/en/latest/howto/auth/firstuse.html#allowing-anyone-to-log-in-to-your-jupyterhub)

By default, you need to manually create user accounts before they will be able to log in to your JupyterHub. If you wish to allow **any** user to access the JupyterHub, run the following command.

```
tljh-config set auth.FirstUseAuthenticator.create_users true
tljh-config reload
```
