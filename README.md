# theforeman.org

This repo contains the source code for
[theforeman.org](http://theforeman.org). All of the site's content is written in
[Markdown](http://daringfireball.net/projects/markdown/syntax). If you're not familiar with it, fear not; it's easy
to learn and to become rapidly productive!

Everything you push into the gh-pages branch goes live immediately!

## Testing locally

To test your changes locally use

    # rake

to generate your site in the \_site directory, or

    # rake server

To start Jekyll server locally.

## Contributing

1. Fork this repo to your account.
2. Clone the fork.
3. Run `bundle install` in the root of the freshly cloned repo. This
   will install Jekyll, the tool we use to build the site.
4. Run `jekyll serve --watch` and open your browser to http://localhost:4000.
5. Make some changes, refresh your browser to preview them.
6. Submit a pull request.

## Updating API Auto-Generated Docs by apipie

Generate API docs in Foreman
1. cd to foreman directory
2. rake apipie:cache

Copy docs to repo
3. cd to theforeman.org directory
4. cp -r dir/to/foreman/public/apipie-cache/apidoc api/
5. cp dir/to/foreman/public/apipie-cache/apidoc.* api/

Update href in html files
6. Edit file api/apidoc/v1.html - change `href="../apidoc/v1` to `href="../apidoc/v1.html`
7. Edit file api/apidoc/v2.html - change `href="../apidoc/v2` to `href="../apidoc/v2.html`

