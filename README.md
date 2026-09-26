# Kolachalama Laboratory website

Source for [vkola-lab.github.io](https://vkola-lab.github.io), built with Jekyll and served by GitHub Pages. Pushing to `master` publishes the site.

## Editing content

Most updates only touch YAML files in `_data/`; no HTML needed.

| To change… | Edit |
|---|---|
| News (home page + /news/) | `_data/news.yml`: add new items at the **top**. Start a headline with `New paper!`, `New grant!` or `New award!` to tag it. |
| People | `_data/team_members.yml`: `group` 0 PI · 1 postdoc · 2 grad/MD student · 3 staff · 4 undergrad · 5 affiliate · 8 alumni. Photos go in `images/teampic/` (square, ~480 px, JPEG). |
| Featured papers | `_data/publist.yml`: `highlight: 1` shows a paper as featured; the first four also appear on the home page. Thumbnails go in `images/pubpic/`. |
| Code & models | `_data/tools.yml` |
| Research themes | `_data/themes.yml` |
| Press & podcasts | `_data/press.yml` |
| Videos | `_data/videos.yml` (YouTube IDs) |
| Funders | `_data/funders.yml` |
| Site-wide settings | `_config.yml` (title, description, links, optional GA4 ID and contact email) |

Page templates live in `_pages/`, shared pieces in `_includes/`, and all styling is in `css/main.css` (plain CSS with light and dark themes).

## Images

Keep photos small: about 480 px square for people and 1200 px wide for figures, saved as JPEG (quality ~82). A 12 MB phone photo slows the Team page for every visitor.

```bash
# Example with ImageMagick
magick input.png -resize 480x480^ -gravity center -extent 480x480 -quality 82 images/teampic/firstname_lastname.jpg
```

## Preview locally

```bash
bundle install
bundle exec jekyll serve   # then open http://localhost:4000
```

## Credits

Originally based on the [Sanders lab](https://sanderslab.github.io) templates, which build on work by [D. Allan Drummond](http://www.allanlab.org/aboutwebsite.html) and [Trevor Bedford](https://bedford.io/misc/about/).
