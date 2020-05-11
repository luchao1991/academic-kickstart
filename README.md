<p align="center"><a href="https://sourcethemes.com/academic/" target="_blank" rel="noopener"><img src="https://sourcethemes.com/academic/img/logo_200px.png" alt="Academic logo"></a></p>
# Academic Kickstart: The Template for [Academic Website Builder](https://sourcethemes.com/academic/)

## add publication
### Manually

Alternatively, publications can be manually created using the command:

```
hugo new --kind publication publication/<my-publication>
```

where <my-publication> is the name of your publication, using hyphens (-) instead of spaces.

Then edit the parameters in content/publication/<my-publication>/index.md to include the details of your publication. The main parameters include:

title: the title of your publication
date: the date that your publication was first published (must be in a valid TOML date format)
publication_types: use the following legend to specify the type of your publication, e.g. "1" for conference proceedings:
0 = Uncategorized
1 = Conference paper
2 = Journal article
3 = Preprint / Working Paper
4 = Report
5 = Book
6 = Book section
7 = Thesis (v4.2+ required)
8 = Patent (v4.2+ required)
publication: where your title was published - Markdown formatting is enabled here for italic etc.
abstract: the summary of your publication
Further details on your publication can be written in the body of the document (after the YAML/TOML front matter) using Markdown for formatting. This text will be displayed on the publication’s page.

To enable visitors to read your work, either paste a link to your PDF in url_pdf or **add a PDF file with the same name as your publication’s own folder to your publication’s folder and a PDF link will be automatically generated.** For example, if your publication is located at publication/photons/index.md, place a PDF at publication/photons/photons.pdf.

To enable visitors to easily cite your work, export a BibTeX citation file named cite.bib from your reference management tool to your publication’s own folder and a citation link will be automatically generated.

### Linking other resources

The url_ links can either point to local or web content. Associated local publication content, may be copied to the publication’s folder and referenced like url_code = "code.zip".

## deployment

To create the `academic-kickstart` repository, [**fork**](https://github.com/sourcethemes/academic-kickstart#fork-destination-box) the *Academic Kickstart* repository and clone your fork with Git (download it to your computer) by replacing `` in the following command with your Github username:

```
git clone https://github.com/<USERNAME>/academic-kickstart.git My_Website
cd My_Website
git submodule update --init --recursive
```

In your `config.toml` file, set `baseurl = "https://.github.io/"`, where `` is your Github username. Stop Hugo if it’s running and delete the `public`directory if it exists (by typing `rm -r public/`).

Add your *.github.io* repository into a submodule in a folder named *public*, replacing with your Github username:

```
git submodule add -f -b master https://github.com/<USERNAME>/<USERNAME>.github.io.git public
```

Add everything to your local git repository and push it up to your remote repository on GitHub:

```
git add .
git commit -m "Initial commit"
git push -u origin master
```

Whilst running the above commands you may be prompted for your Github username and password.

Next, **regenerate** your website’s HTML code by running Hugo and uploading the *public* submodule to GitHub:

```
hugo
cd public
git add .
git commit -m "Build website"
git push origin master
cd ..
```

Once Git has finished uploading your site to Github, you can open your new `https://.github.io` website in your browser, substituting with your Github username.

[**Academic**](https://github.com/gcushen/hugo-academic) makes it easy to create a beautiful website for free using Markdown, Jupyter, or RStudio. Customize anything on your site with widgets, themes, and language packs. [Check out the latest demo](https://academic-demo.netlify.com/) of what you'll get in less than 10 minutes, or [view the showcase](https://sourcethemes.com/academic/#expo).

**Academic Kickstart** provides a minimal template to kickstart your new website.

- 👉 [**Get Started**](#install)
- 📚 [View the **documentation**](https://sourcethemes.com/academic/docs/)
- 💬 [Chat with the **Academic community**](https://spectrum.chat/academic) or [**Hugo community**](https://discourse.gohugo.io)
- 🐦 Twitter: [@source_themes](https://twitter.com/source_themes) [@GeorgeCushen](https://twitter.com/GeorgeCushen) [#MadeWithAcademic](https://twitter.com/search?q=%23MadeWithAcademic&src=typd)
- 💡 [Request a **feature** or report a **bug**](https://github.com/gcushen/hugo-academic/issues)
- ⬆️ **Updating?** View the [Update Guide](https://sourcethemes.com/academic/docs/update/) and [Release Notes](https://sourcethemes.com/academic/updates/)
- :heart: **Support development** of Academic:
  - ☕️ [**Donate a coffee**](https://paypal.me/cushen)
  - 💵 [Become a backer on **Patreon**](https://www.patreon.com/cushen)
  - 🖼️ [Decorate your laptop or journal with an Academic **sticker**](https://www.redbubble.com/people/neutreno/works/34387919-academic)
  - 👕 [Wear the **T-shirt**](https://academic.threadless.com/)
  - :woman_technologist: [**Contribute**](https://sourcethemes.com/academic/docs/contribute/)

[![Screenshot](https://raw.githubusercontent.com/gcushen/hugo-academic/master/academic.png)](https://github.com/gcushen/hugo-academic/)

## Install

You can choose from one of the following four methods to install:

* [**one-click install using your web browser (recommended)**](https://sourcethemes.com/academic/docs/install/#install-with-web-browser)
* [install on your computer using **Git** with the Command Prompt/Terminal app](https://sourcethemes.com/academic/docs/install/#install-with-git)
* [install on your computer by downloading the **ZIP files**](https://sourcethemes.com/academic/docs/install/#install-with-zip)
* [install on your computer with **RStudio**](https://sourcethemes.com/academic/docs/install/#install-with-rstudio)

Then [personalize your new site](https://sourcethemes.com/academic/docs/get-started/).

## Ecosystem

* **[Academic Admin](https://github.com/sourcethemes/academic-admin):** An admin tool to import publications from BibTeX or import assets for an offline site
* **[Academic Scripts](https://github.com/sourcethemes/academic-scripts):** Scripts to help migrate content to new versions of Academic

## License

Copyright 2017-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/sourcethemes/academic-kickstart/blob/master/LICENSE.md) license.

[![Analytics](https://ga-beacon.appspot.com/UA-78646709-2/academic-kickstart/readme?pixel)](https://github.com/igrigorik/ga-beacon)

