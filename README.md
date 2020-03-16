# piretship.github.io

PIReT Web Site.  This is a Jekyll site.

We use the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) Jekyll theme.

## Local Testing

If you want to build and test the web site on your computer, you first need to install `ruby` and `bundler`.

With those installed, run:

    bundle install
    bundle exec jekyll serve

You can then connect to http://localhost:4000 to browse the site.

## Accessibility Notes

**Our web page must be accessible**, by Idaho state law and Boise State University policy.

The [WebAIM Accessibility Evaluation Tool](https://wave.webaim.org/) is useful for checking accessibility.

Some points to help:

- Use semantic markup.  Using Markdown instead of custom HTML whenever possible helps a lot with this.
- All images must have ALT text.  If an image is purely decorative, give it empty alt text to signal that
  it is deliberately a decorative image.

## Sources of Media

If you're looking for pictures to use:

- [Unsplash](https://unsplash.com) is a good source of free photographs.  The home page photo came from there.
- [The Noun Project](https://thenounproject.com/) has icons.  If you find an icon there you want to use, send a link
  to Michael and he will get a version we can use freely.
- We can also use images from sites like Flickr if the image has a Creative Commons license.

## Adding Publications

To add a publication, add a new Markdown file in the `_pubs` directory.  Do **not** add it to `pubs`; this is for managing output.

The markdown file needs a couple of things.  For an example, see `ComplexRec18-literate.md`.

-   The frontmatter should contain the title, publication date, and project, like this:

        title: "Paper Title"
        date: 2018-08-15
        project: literate
        type: paper

    If the paper title contains a colon (`:`), it **must** be put in quotes.  The quotes
    are optional in most other cases.

    If the paper has a DOI or arXiv ID, include that in the header as well, as a `doi` or `arxiv` field.  The `type` should be one of:

    - paper
    - demo
    - thesis

-   The first paragraph of the file should be a citation, with two special pieces of formatting:

    - The *paper title* should be a link to the location `#`, e.g. `[My Paper Title](#)`.
    - The first line of the paragraph needs to be the text `{: .citation}` to mark it as a citation paragraph.
      This is a Kramdown [inline block attribute list](https://kramdown.gettalong.org/syntax.html#block-ials).

-   The *Links and Resources* section should include links to:

    - The offical paper page (e.g. its page in the ACM Digital Library)
    - Paper PDF if available via public link
    - Conference or proceedings
    - Anything else useful (e.g. the project, code to reproduce, etc.)