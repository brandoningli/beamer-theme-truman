# Truman Beamer Theme

This beamer theme is [based on the Caltech-beamer-theme](https://github.com/jsh9/Caltech-beamer-theme).

This unofficial theme includes the Truman State University logo and (lookalike) fonts following the [identity standards](https://identity.truman.edu). The included Truman color theme also follows these standards, so it is advised against editing it. The `Raleway` font is required, and is included in TexLive distributions. The included logo files must be stored in the same directory as the theme sty files.

Sample Beamer presentation content is from Overleaf.

## Layout Types

This features a few options for formatting.
+ `minimal` uses a standard title-on-top layout and puts the logo on the bottom-right corner
+ `sidebarleft` puts a sidebar with a table-of-contents on the left side, and the logo in the top-left corner. Shows subsections of the section you're currently in.
+ `sidebarright` puts a sidebar with a table-of-contents on the right side, and the logo in the top-right corner. Shows subsections of the section you're currently in.
+ `sidebarleftnosub` is like `sidebarleft`, but doesn't show any subsections.
+ `sidebarrightnosub` is like `sidebarright`, but doesn't show any subsections.

## Altered and New Commands

The `\maketitle` command has been renewed to make it easier to create properly formatted title frames. When using a sidebar option, the content will be shifted up by the headline height so it is properly centered on the frame with a "hidden" headline bar (on the minimal option, there is no headline, so title content is not shifted). Fill out all title information as usual, but **do not** wrap the `\maketitle` command in a frame; it will provide one for you. Just use `\maketitle` by itself to create your title frame. That's it. Nothing else.

Use the `\sectiontitle` command to create a section title page. It takes two parameters, a title and a subtitle. Either can be left blank.

To hide the logo from a frame, use the `plain` option in your frame. Only use this in `minimal`, though, as it also removes the sidebar in the other modes.
```latex
\begin{frame}[plain]{No Logo}
    Some content here.
\end{frame}
```
