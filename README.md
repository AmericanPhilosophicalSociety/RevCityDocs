# RevCityDocs

This GitHub repository stores the source code for the [documentation](https://americanphilosophicalsociety.github.io/RevCityDocs/) for [The Revolutionary City: A Portal for the Nation's Founding](https://therevolutionarycity.org) (Rev City). Though its primary audience is the staff who contribute material to Rev City, edits for the documentation are welcome.

The documentation pages are written in [Jekyll](https://jekyllrb.com/) and use the [Just the Docs](https://just-the-docs.com/) theme. Pages are written in Markdown. The site is published via [GitHub actions](https://jekyllrb.com/docs/continuous-integration/github-actions/).

For help using Markdown, please take this [Markdown tutorial](https://www.markdowntutorial.com/) and see this [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

# Contributing

Anyone can contribute to improving the documentation. 

Rev City administrators should edit the Markdown files directly.

For all others, please do one of the following:

- Open an [issue](https://github.com/AmericanPhilosophicalSociety/RevCityDocs/issues) and describe the changes you would like to see;
- Make a [pull request](https://github.com/AmericanPhilosophicalSociety/RevCityDocs/pulls) and propose changes yourself.

# Editing and Running the Site Locally

You can test and run the site locally through the following workflow.

1. Install [Ruby](https://www.ruby-lang.org/en/downloads/) and [Jekyll](https://jekyllrb.com/docs/).
2. In your terminal, navigate to where you want to put the site, then clone this repo and move into the directory the process creates:

```
git clone https://github.com/AmericanPhilosophicalSociety/RevCityDocs.git
cd RevCityDocs
```
3. Install the Jekyll dependencies:

```
bundle install
```
4. Run the site locally:

```
bundle exec jekyll serve
```
5. Navigate to http://localhost:4000/ to preview the site.
