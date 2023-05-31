# mokelentertainment.com
A website I maintain for my brother.

## Congrats Mike!
Rachel and I are so proud of you graduating high school! To celebrate, we've
made you a website to capture the Mokel Entertainment brand. You can use this
website to build your professional portfolio, or something else. This page will
always be here to help you figure out how to make changes and update your site.
You can update your site without knowing a lick of code.

## First Time Setup

1. First, you'll need to [create a Github
account](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home).

1. Next, install
[git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). Git is a
command line tool that helps you manage the content in this repository.

1. Install [`node package manager`](https://nodejs.org/en/download).

1. Run `git-bash`, which should open up a black command line. **Don't panic!**
We're going to sign into Github in your command line. You only have to do this
once! Run the following, and make sure to include quotes in the command!

    * `git config --global user.name "<insert-your-github-username-here">

    * `git config --global user.email "<insert-your-github-email-here">

1. Next, you're going to be "pulling" the code from github to your local
machine. While still in `git-bash`, you'll need to navigate to the folder where
you want the project to live. I know you aren't super familiar with command
line, so here are the commands you need to know to navigate your filesystem:

    * `pwd` - prints your current working directory

    * `ls` - lists files in your directory.

    * `cd <directory>` - change directory. You can run "`cd ..`" to go up a
    directory.

1. Now that you're in the directory where you want to pull the code from Github,
run the following:

    ```
    git clone https://github.com/nsaccente/mokelentertainment.com.git
    ```

1. Now you can `cd` into the newly pulled project by running `cd mokelentertainment.com`. Next, run `npm install`.

1. Finally, [click
here](https://github.com/gohugoio/hugo/releases/download/v0.112.5/hugo_extended_0.112.5_windows-amd64.zip)
to install `hugo`. Hugo is the command line tool that actually **builds** the
project.


## Getting Oriented with Project Files

Hugo projects all follow a pretty uniform structure, which means that searching
for answers to questions online is often pretty straightforward. Let's look at
the directory structure:

```
.
├── archetypes 
│   ├── blog.md
│   ├── drone.md
│   ├── film.md
│   ├── music.md
│   └── video.md
├── configTaxo.toml
├── config.toml
├── content
│   ├── about.md
│   ├── blog
│   ├── contact.md
│   ├── drone
│   ├── film
│   ├── _index.md
│   ├── music
│   └── video
├── data
│   ├── features.json
│   └── slide.json
├── layouts
│   └── shortcodes
├── netlify.toml
├── package.json
├── package-lock.json
├── postcss.config.js
├── public
│   └── ...
├── README.md
├── resources
│   └── _gen
├── static
│   ├── css
│   ├── favicon-32x32.png
│   └── img
├── tailwind.config.js
└── themes
    └── tella
```

### archetypes

These are templates for new content. You don't need to worry so much about this,
but if you ever want to write your own templates, see [this
video](https://www.giraffeacademy.com/static-site-generators/hugo/archetypes/).

### config.toml

Configure metadata about your site, such as the website name, configuration of
the home page, etc.

### content

THIS is where your actual content lives. I've set up a few different types of **content types** to get you started. Those content types are: `blog`, `drone`, `film`, `music`, and `video`. You can 

### data

* `data/features.json` controls the small "features" section of the home page

* `data/slide.json` controls the slideshow on the home page

### static

This is where static content lives.

* `static/css` is where custom css lives. If you want to write custom css to alter the look of your site, this is where you do it.

* `static/img` is where images live! This is organized in the following way:

    * `static/img/content/<content type>/<name>` - The directory for photos to go along with `content`.


## Creating New Content

It's super easy to create new content. In your command line, navigate to the
project directory using the commands like I showed you above. 

1. Blog Content

    By default, blog files are named by the date of the post.

    ```
    hugo new content/blog/<date>.md
    ```

1. Drone, Film, Music, Video Content

    By default, this kind of content is named using the Youtube video ID (see
    [here](https://gohugo.io/content-management/shortcodes/#youtube) for more info).

    ```
    hugo new content/video/<youtube-id>.md
    ```

Once you use hugo to create a new file, open that file in a text editor, and
writing your content. Hugo takes advantage of
[`frontmatter`](https://gohugo.io/content-management/front-matter), which you
can edit to make your posts easy to find in search engines.

You'll write your content in [Markdown](https://www.markdownguide.org/).

## Testing 

It can be difficult to tell how your project is going to look from a text editor. Run the following to see changes you make to your site in real time (you might have to refresh the page sometimes):

```
hugo server --disableFastRender
```

Watch the output from this command, and look for something that says something similar to:

```
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
```

Now, open a browser, and navigate to `http://localhost:1313/` to view your site.

## Publishing Changes

Now that you've made changes, you'll want to publish them! This is achieved through the `git` command.

In `git-bash`, run the following:

```
git add -A
git commit -m "<put a message here that describes what you've changed>"
git push
```

Upon pushing to git, this will invoke an automated job that builds and deploys
the code to [netlify.com](https://www.netlify.com/). Check your website, and
make sure the changes worked! Happy editing!