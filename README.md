# Postman Collection for Digital Ocean API

Postman is a pretty neat way to play around with an API. I've come to enjoy it
more than `curl` (though `curl` will always have a place in my heart).

As I was going through the [DigitalOcean (DO) API v2 Introduction][api-intro], I
started creating a Postman collection to match the `curl` examples on the left.
This is far from complete but I'm likely to add to it as I toy with the API
more. I'm kind of an API guy on the side so I like to play around with the real
API before I jump into a [command line interface], a purpose built library (e.g.
[godo]), or [terraform].

If you like Postman, you might find this to be a good starting point. If you do,
consider helping me flesh out the collection by submitting PRs.

## Install

1. Get [Postman] and install it.
1. Go to File -> Import...
1. Choose Files
1. Select the json file from your workspace and import it.

## How to use it

You need to create an environment like this in Postman.

| Key                   | Value
|-----------------------|---------------------------------------
| access\_token         | \<Get one from DO and paste it here\>
| endpoint              | https://api.digitalocean.com/v2
| region                | nyc2
| droplet\_name         | mydroplet
| droplet\_size         | s-1vcpu-1gb
| image\_slug           | ubuntu-18-04-x64
| ssh\_key\_fingerprint | \<paste yours here\>

You'll find other environment variables references in some of the requests but
this should get you started.

## Naming Standards

The collection is organized such that it should match the [API
intro][api-intro]. The folders correspond to the sections on the left and the
requests are named to match the requests examples. Hopefully, this makes it easy
to follow along.

[api-intro]: https://developers.digitalocean.com/documentation/v2/
[doctl]: https://github.com/digitalocean/doctl
[godo]: https://github.com/digitalocean/godo
[terraform]: https://github.com/terraform-providers/terraform-provider-digitalocean
[postman]: https://www.getpostman.com/apps
