# Notes:
Basically the Github Pages have certain constraints
- **Personal Pages (One per Account)**:
  Each GitHub user or organization can have one personal GitHub Pages site. This is hosted at https://<username>.github.io/.
- **Project Pages (Unlimited per Account)**:
  You can create a GitHub Pages site for each repository you have. These are hosted as https://<username>.github.io/<repository-name>/.

Next time look on here and not spending to much thinking the problem is otherwise.

### Path in Development vs Deployment
in development, set the `baseurl` to `""` and for deployment, set the baseurl on which url as teh starting point.
> the baseurl will be a variable that can be use for pathing.

For variable one set like this to ensure the baseUrl is in the path when in deployment
```html
<span class="image">
    <img src="{{ site.baseurl }}/{{ page.image }}" alt="">
</span>
```
And for the static pages, use both `site.baseurl` and combination of `% links %` for the improve pathing for static files
```html
<span class="image fit">
    <img src="{{ site.baseurl }}/{% link assets/images/glasses-poster.png %}" alt="">
</span>
```

Typical project structure on Jekyll
```yaml
.
├── _config.yml ## Main Config File
├── _includes/  ## Contains reusable partials like headers, footers, or navbars
├── _layouts/   ## Houses the templates that define the structure of different types of pages.
├── _posts/     ## Contains blog posts written in Markdown or HTML  
├── _data/      ## Stores custom data files (in YAML, JSON, or CSV) that can be used throughout the site.
├── _sass/      ## Contains SCSS partials for styling, which can be imported into a main SCSS file.
├── assets/     ## Stores static assets like CSS, JavaScript, images, and fonts.
├── _site/      ## The output folder where the generated static site is placed. (Automatic)
├── index.html
└── other_pages.md
```

# Chirpy Starter

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

When installing the [**Chirpy**][chirpy] theme through [RubyGems.org][gem], Jekyll can only read files in the folders
`_data`, `_layouts`, `_includes`, `_sass` and `assets`, as well as a small part of options of the `_config.yml` file
from the theme's gem. If you have ever installed this theme gem, you can use the command
`bundle info --path jekyll-theme-chirpy` to locate these files.

The Jekyll team claims that this is to leave the ball in the user’s court, but this also results in users not being
able to enjoy the out-of-the-box experience when using feature-rich themes.

To fully use all the features of **Chirpy**, you need to copy the other critical files from the theme's gem to your
Jekyll site. The following is a list of targets:

```shell
.
├── _config.yml
├── _plugins
├── _tabs
└── index.html
```

To save you time, and also in case you lose some files while copying, we extract those files/configurations of the
latest version of the **Chirpy** theme and the [CD][CD] workflow to here, so that you can start writing in minutes.

## Usage

Check out the [theme's docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki).

## Contributing

This repository is automatically updated with new releases from the theme repository. If you encounter any issues or want to contribute to its improvement, please visit the [theme repository][chirpy] to provide feedback.

## License

This work is published under [MIT][mit] License.

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE
