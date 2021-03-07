# fairdo.org

This is the public repo for [fairdo.org](https://www.fairdo.org), an online resource dedicated to the FAIR Digital Object (FDO) concept. 

## About the site

- This site uses [Jekyll](https://jekyllrb.com/docs/), a Ruby-based static site generator. For more information about using Jekyll and additional install instructions, refer to the [Jekyll documentation](http://jekyllrb.com/docs/home/).

- The site design and template was borrowed from [U.S. Web Design Standards](https://standards.usa.gov), a set of reusable, high-quality components for modern websites. 


### Before you start

You will need to have the following installed on your machine before following the commands below:

- Ruby v2.7.1+, [Installation guides](https://www.ruby-lang.org/en/documentation/installation/)

### Basic setup

1. Install Jekyll and Bundler: `gem install bundler jekyll`
1. Install gem dependencies `bundle install`
1. Install node dependencies `npm install`

Notes for basic setup:

- For basic setup, root or sudo-level access (e.g., `sudo gem install bundler jekyll`) may be required. Enter sudo password when prompted.
- When running `npm install`, an `sha` key will be added to the kind-of dependency in the package-lock.json file. This can be committed to the forked repo but should not be merged with the parent repository. This key is unique to each user.

### Running the site locally

To run the site locally, from the project folder, run:

```
bundle exec jekyll serve
```

If all goes well, visit the site at `http://localhost:4000`.

Note that this method will rebuild the entire site every time you make a change to any file, however, the browser may need to be refreshed to see changes. If you want faster builds, you can use `bundle exec jekyll incrementalserve`, which comes with [some caveats](https://jekyllrb.com/docs/configuration/incremental-regeneration/), notably only changed files will be rebuilt. This means if you change a data file, HTML pages that use that data file won't be updated. Also, `bundle exec jekyll incrementalserve` may require an additional gem install.

### Editing the website 

- Global settings are in `_config.yml`. 
- The landing page is `_pages/home.md`. 
- Each section (Working Groups,Examples etc.) has its own section with an index page. 
- Navigation: `_includes/sidenav.html` and `_data/navigation.yml`. 
- Header: `_includes/header--extended.html` and `_data/header.yml`. 
- Footer is `_includes/footer.html`. 
- News and events: `_data/events.yml`. 

### Color scheme 

In `_sass/_variables.scss`:

```
$border-color: #edd5d9;
$color-blue-light: #ebf3f7;
$color-tan: #f2faf8;
$color-tan-dark: #f0eee8;
```

