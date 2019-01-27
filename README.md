# Generate certificates with Let's Encrypt

1. Add the necessary domains into the `domains.conf` file.
2. Create an `.env` file following the template `.env.template`.
3. Run docker.
4. Find your certs on the `ssl` folder.

## Docker run command

`docker-compose run --rm gen-certs`

## Get lexicon provider information

`docker run -it --rm adferrand/letsencrypt-dns lexicon route53 --help`

[List of providers in lexicon information](https://github.com/AnalogJ/lexicon#providers)

You can add the variables into the env file concatenating the `LEXICON_`, the provider and the variable needed by the provider.

For instance, route53 needs 2 variables:

* ACCESS_KEY -> LEXICON_ROUTE53_ACCESS_KEY
* ACCESS_SECRET -> LEXICON_ROUTE53_ACCESS_SECRET
