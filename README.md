# koushin

## Usage

    go run ./cmd/koushin imaps://mail.example.org:993 smtps://mail.example.org:465

See `-h` for more information.

## Themes

They should be put in `public/themes/<name>/`.

Templates in `public/themes/<name>/*.html` override default templates in
`public/*.html`. Assets in `public/themes/<name>/assets/*` are served by the
HTTP server at `themes/<name>/assets/*`.

## Plugins

Lua plugins are supported. They can be dropped in `plugins/*.lua`.

API:

* `koushin.on_render(name, f)`: prior to rendering the template `name`, call
  `f` with the template data
* `koushin.set_filter(name, f)`: set a template function

## License

MIT
