# Help with understanding the (possible) use of LaTeX and MarkDown

Hi,
For the moment I'm on Mac and I used rtf-documents to write ideas. That works nice, but on Windows the files open in Word (which is overkill) and also in Linux you don't have a light-weight program like Text-editor for rtf. Also, you have a better Markdown-application in NextCloud, then for rtf. It seems MarkDown is perfect for how I used rtf. In the future, I'll switch to Linux (on a Framework laptop :-) ).

So I started using MarkDown. In NextCloud it works perfect, I find the Mac-MarkDown-programs surprisingly slow or big. A few days ago I discovered Zettlr. I like it. It's bigger then Text-editor, but with a lot of useful functions (like citations, exporting options, ... ).

So far, all good. But after I worked on an idea, I DO want to lay-out it. I thought, that's the part where I can use LaTeX. I can make a template and apply it to any text to export that in the chosen document type. That exist, for instance for scientific papers.
But LaTeX is not MarkDown. If I experiment in OverLeaf, I see the formatting doesn't translate, _this_ is not italic, **this** is not bold. I would have to type \textit{...} and \textbf{...}.
That seems almost the opposite idea of MarkDown: it's not easy to type without distraction, it's really cumbersome just to have a word italic. Also: how would you instert a picture and reference to it, without having to type a whole bunch of code.

So, how to I achieve what I want? Aren't MarkDown and LaTeX the right tools?
What I want: some distraction-free typing tool, like rtf and texteditor or markdown (not txt, I need SOME lay-out options, like lists, bold and italic, maybe a simple table). AND I want a lay-out application (accomplishing the same as with a WYSIWYG-editor, but it doesn't have to be WYSIWYG). And both have to work togheter.

Any input is welcome. I asked the same question in the Zettlr-subreddit, but no-one replied.

[permalink](http://reddit.com/r/LaTeX/comments/16mmpxo/help_with_understanding_the_possible_use_of_latex/)
by *JonasanOniem* (↑ 5/ ↓ 0)

## Comments

##### I would suggest looking into pandoc.  For anything that requires much formatting, I use LaTeX.  But I do write quite a few simple documents that I might need to convert to Word in emacs Org format and then convert to Word or LaTeX using pandoc.  Pandoc will also convert Markdown.  It sounds like the sort of work flow you are looking for. ⏤ by *27183* (↑ 11/ ↓ 0)
├─ You mean writing in whatever format I like, say MarkDown, and then converting it to whatever with Pandoc? Edit lay-out in the converted file, with the appropriate program.
Yes, that could work. I hoped there would be a way of immediately working with the markdown-file. Like, I keep typing in the .md file and once in while compile it with (for instance) LaTeX, to see the result.
I'll remember Pandoc, anyway. ⏤ by *JonasanOniem* (↑ 2/ ↓ 0)
├── You can create a LaTeX template for pandoc that contains all your layout, specific styling, etc. and then do exactly that. ⏤ by *noeticmech* (↑ 2/ ↓ 0)
├─── That's exactly what I wanted to use Zettlr for, it has a built-in pandoc engine.
I guess I 'll start learning LaTeX
:o} ⏤ by *JonasanOniem* (↑ 1/ ↓ 0)
└────

##### You can also look into Typst, it's lighweight and close yo markdown ⏤ by *AkilonI* (↑ 2/ ↓ 0)
├─ Looks interesting. What file format is that?

What I like about MarkDown and LaTeX, is that they are platform-independent, even application-independent. That way, if I ever want to change from mac to linux and also from one editor to another, I don't have any problem with old files.

I work on a Windows computer at work, with no administration rights. It's important I can use my files there as well (which can be in NextCloud, for instance).
I really think mac pages is a very user-friendly text-editor, but it's the worst in being closed to outside users (I know you can edit in a browser in iCloud, but if I switch to Linux, I'm not going to use iCloud anymore). ⏤ by *JonasanOniem* (↑ 1/ ↓ 0)
├── Typst is its own thing. If you're getting started and don't have any reason to prefer LaTeX, then try Typst. Typst is what LaTeX would look like if created today. It's incredibly flexible, has meaningful errors, good defaults and having a nice community (mainly on Discord).

It's open source and runs on any operating system and even on the browser thanks to Web Assembler (if you're not familiar: this means people can create web apps to edit it and the compilation would be local, so you wouldn't _need_ to send your data to a back end). ⏤ by *sergioaffs* (↑ 3/ ↓ 0)
├─── Btw: LaTeX or Typst make sense if your target is pdf. If what you want is to create HTML based on markdown, they're not meant to do that (although you can probably force both into doing it). ⏤ by *sergioaffs* (↑ 1/ ↓ 0)
├──── OK, thank you. At the moment, I'm only thinking of exporting to pdf for print or to word for people who only know that (I never use it).
If it's own file-format, I'm going to look around md and tex a little, see if I can get used to those. ⏤ by *JonasanOniem* (↑ 1/ ↓ 0)
├───── Some people already mentioned it, but it feels relevant: look into pandoc and quarto. Those are tools explicitly meant for parsing between formats. All Word, Markdown, LaTeX and Typst are supported. ⏤ by *sergioaffs* (↑ 2/ ↓ 0)
├────── Yeah, I looked at that Pandoc, it's built-in in Zettlr. ⏤ by *JonasanOniem* (↑ 1/ ↓ 0)
├─── Are graphs in Typst already a thing? And does it have packages like LaTeX? ⏤ by *hopcfizl* (↑ 1/ ↓ 0)
├──── Yes to both. The package for drawing is called [CeTZ](https://github.com/johannes-wolf/cetz) and seems pretty powerful. Also a nice thing: there is built-in support for SVG shapes, so I was able to reproduce in Typst a card game design that took me quite some time to develop in LaTeX. Quickly and without packages.

And that's also in general the approach to packages: they exist, and they enable many fancy features (graphs, textboxes, domain-specific diagrams, glossaries), but there is much more basic functionality that doesn't need a package (e.g. no need to import a package to strike a text through). 

My only little gripe with the current model is that there already are different packages for tables, which is something that is extremely annoying in LaTeX. But the hope is that, as the core Typst evolves, the need for these packages will disappear. ⏤ by *sergioaffs* (↑ 2/ ↓ 0)
├───── We'll definitely improve the built-in table over time, it's just nice that the availability of tablex let's us proceed with that a little more slowly and focus on some other things first. ⏤ by *SymbolicTurtle* (↑ 2/ ↓ 0)
└────

##### Have a look at Obsidian and pandoc integration ⏤ by *Mention-One* (↑ 1/ ↓ 0)
├─ I checked it, but isn't it more or less like Zettlr? ⏤ by *JonasanOniem* (↑ 1/ ↓ 0)
├── I didn't know Zettlr before your mention :) I think it's very similar. So yes, you can write in Zettlr, using markdown and export with pandoc. ⏤ by *Mention-One* (↑ 2/ ↓ 0)
└────

##### I use the Python package DocUtils (I only ever used it on GNU/Linux but I'm sure it also works just fine on Windows and Mac) to convert RestructuredText into LaTeX very easily and then apply a LaTeX style sheet. We use this approach for the documentation at our institute and are quite happy with the results. RST is obviously not Markdown, but it's fairly close and many constructs are compatible.

The reason we are doing this, as opposed to just writing the documentation in LaTeX straight up, is that the syntax of Markdown/RST is a lot simpler and more conscise (as you have already noticed), and that way we can export it into HTML for our wiki or export it to LaTeX with template and get a print-ready copy.

The results (in terms of layout) that you get with this approach are not as good as writing it in LaTeX right away, since with LaTeX you can adjust spacing, figure layout and all this stuff to make it perfect, whereas this way, we just throw a template on it and hope that it looks alright. But it's adequate for a technical documentation. I would never suggest doing this for a research paper or a thesis, however. You have to use the right tool for the job, and Markdown is not the right tool for a research paper. Just use LaTeX. 

Alternatively, you can use something like Ghostwriter (the program; please don't hire an actual ghostwriter). It is, by design, a distraction-free Markdown editor, but I'm not entirely sure how well you it lets you tweak the layout of the output document.

> Also: how would you instert a picture and reference to it, without having to type a whole bunch of code.

All you need is `\includegraphics{picture.jpg}`, which I don't think is less intuitive than `![](picture.jpg)`. Quite the opposite. All the stuff you write around it is there to control the figure layout and give it a caption and a label for referencing. All of these things are optional. ⏤ by *[deleted]* (↑ 1/ ↓ 0)
├─ > I use the Python package DocUtils (I only ever used it on GNU/Linux but I'm sure it also works just fine on Windows and Mac) to convert RestructuredText into LaTeX very easily and then apply a LaTeX style sheet. We use this approach for the documentation at our institute and are quite happy with the results. RST is obviously not Markdown, but it's fairly close and many constructs are compatible.

So what would be the advantage over using MarkDown/Zettlr?

> I would never suggest doing this for a research paper or a thesis, however. You have to use the right tool for the job, and Markdown is not the right tool for a research paper. Just use LaTeX.

Or Zettlr and LaTeX?

> All you need is \includegraphics{picture.jpg}, which I don't think is less intuitive than ![](picture.jpg). Quite the opposite. All the stuff you write around it is there to control the figure layout and give it a caption and a label for referencing. All of these things are optional.

That's true. Maybe writing isn't that difficult once you're used to it? Am I making things more complex by starting in md and going to LaTeX, however I would do that? ⏤ by *JonasanOniem* (↑ 1/ ↓ 0)
├── For us, the reason for using DocUtils is were that we are not limited to a specific text editor to do the Markdown/RST to LaTeX conversion for us. That's a very important thing when you have more than one person working on a project. Some people like Vim, some people like Emacs, some people like VSCode, so separating the writing part from the compilation part (just like LaTeX does as well) is an important feature.

Of course you can write a thesis in Markdown and then convert it to LaTeX. A student at our institute has done that fairly recently and it wasn't unreasonably ugly. I think he used Pandoc if I'm not mistaken. But the hoops he had to jump through to get there made me think (and say) that he should have just used LaTeX right from the start, because this approach was honestly way more complicated than it needed to be.

For example, if you include a figure in Markdown or RST with a caption, most conversion tools will convert that into a `\begin{figure}[H] ... \end{figure}`, with the `[H]` argument being the critical point. It forces the placement of the figure right there, as opposed to leaving it floating. This is fine for technical documentation, but ill-suited for a thesis and goes against the style guide of some research journals. It's just a lot of little things. ⏤ by *[deleted]* (↑ 1/ ↓ 0)
├─── I understand. I can write TeX in Zettlr, you can edit that in different editors as well. For simple projects that don't need printing or publishing, you can use MarkDown. I give them an account on my NextCloud and share a document with them so we can work together.
I don't have to work with other people on projects, the things that need lay-out are only edited by myself.
As I understand it for now, it would be best to write those in LaTeX.

(The "TeX" in Zettlr is a little strange, I notice: I can just write MarkDown and that's rendering correct, even without the most basic
\documentclass{article}
\begin{document}
...
\end{document}) ⏤ by *JonasanOniem* (↑ 1/ ↓ 0)
└────
