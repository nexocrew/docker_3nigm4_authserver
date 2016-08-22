# Supported tags and respective `Dockerfile` links

-	[`0.1.0_alpha`, `latest` (*0.1/Dockerfile*)](https://github.com/nexocrew/docker_3nigm4_authserver/0.1/Dockerfile)

# What is 3nigm4 Authentication Server?
Official 3nigm4 Authentication Server image implements a RPC frontend to manage user authentication in 3nigm4. It's one of the internal microservices composing the 3nigm4 framewrok.

This component is intended for behind firewall usage (private network) to provide authentication service to frontend components (3nigm4 APIs), do not expose it directly in the internet it can be subject to security issues.

# How to use this image

## start a authserver instance

The following example links to a mongodb container from the official [MongoDb image](https://hub.docker.com/_/mongo/).

```console
$ docker run -d --name auth-service -p 19773:19773 --link mongodb:mongodb nexo/3n4auth
```
