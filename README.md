# testing
testing solidworks in git

This is a git repository created as a proof-of-concept, showing that it is possible to version control Solidworks parts in Git and create documentation to go alongside it.

In production, we would split the 3D models and documentation into their own parallel file trees.

## What you need to run the documentation on your own computer:

- Git, of course:
  - Git allows you to clone the repository and push your changes. You can use a GUI interface or the command line.
- [Quarto](https://quarto.org)
  - Quarto powers the website and documentation itself. It is easiest to use with the [VSCode extension](https://quarto.org/docs/tools/vscode.html#installation)
  - The quarto website is stored as markdown files (*.qmd). These can be crossreferenced like so: `[Link text](filename.qmd)`. You can also add images: `![Image caption](filename.jpg)` and links to files elsewhere in the repository, as well as links to external resources.
  - After making changes to the documentation, run `quarto render` before pushing the changes; this will update the website output in the `/docs` folder.
  - While making changes, you can run `quarto preview` to preview the website and make sure everything is correct.
  - Quarto allows you to include just about anything:
    - Enclose \LaTeX in dollar signs: `$equation$` for inline equations, `$$ Long equation $$` for standalone
    - You can put html and iframes directly into the markdown documents
    - Normal Markdown formatting applies: get *italics* with single \*s, **bold** with double \**s, ~~strikethrough~~ with \~\~ tildes, titles with \#, lines with \---
      - Check out the [pandoc reference](https://pandoc.org/MANUAL.html#pandocs-markdown) for a very complete list of things you can do
    - You can add working R, Python, or Julia code blocks with triple backticks: ` \`\`\`julia `
    - Navigation can be done through standalone pages or a sidebar (the sidebar is a better choice for our wiki)
    - And much more. Check out the [documentation](https://quarto.org/docs/guide/)
