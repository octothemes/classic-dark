# Octopress Themes - Classic Dark Theme

![Octopress Classic Dark Theme thumbnail](https://s3.amazonaws.com/static.octopressthemes.com/thumbnails/dark-thumbnail.png)

Classic dark theme is a theme hand made for Octopress blogging framework. It is compatible with Octopress 2. Updates will be provided from this repository.

## Installation

You can choose to install as a Git submodule. Or you can download as a zip archive and copy the files manually.

### Install as Git submodule

These instructions will create a git submodule under the __.themes/dark__ directory. From your blog directory, run these commands.

``` sh
git submodule add git://github.com/octopress-themes/classic-dark.git .themes/dark
```

You should then commit the changes.

``` sh
git add .themes
git commit -m "added classic dark theme"
```

Next, you should apply the theme to your blog and generate the stylesheets. Follow the [install instructions](#applying-the-dark-theme-to-your-blog).

### Install from downloaded zip archive

If you are more comfortable with just the theme files, you can download our zip archives from [S3](https://s3.amazonaws.com/static.octopressthemes.com/themes/classic-dark-v0.1.0.zip).

1. Once you have downloaded the package, uncompress the archive.
2. Go to your Octopress blog's directory. There should be a hidden directory called __.themes__.
3. Your theme should be a single directory called __dark__ containing the theme files. Copy the __dark__ directory to the __.themes__ directory on your Octopress blog's directory.

Next, you should apply the theme to your blog and generate the stylesheets. Follow the [install instructions](#applying-the-dark-theme-to-your-blog).

## Updating the theme

### With Git submodules

From your Octopress blog's directory, assuming your theme directory is called __dark__.

``` sh
cd .themes/dark
git pull origin master
```

Next, you should apply the theme to your blog and generate the stylesheets. Follow the [install instructions](#applying-the-dark-theme-to-your-blog).

### With downloaded packages

It is largely similar to the install process. We want to overwrite the theme with the new files. Lastly, to run install to apply the changes.

1. Download the new packages from [S3](https://s3.amazonaws.com/static.octopressthemes.com/themes/classic-dark-v0.1.0.zip).
2. Once you have downloaded the package, uncompress the archive.
3. Go to your Octopress blog's directory. There should be a hidden directory called __.themes__.
4. Your downloaded files should be a single directory called __dark__ containing the theme files. Copy the __dark__ directory to the __.themes__ directory on your Octopress blog's directory.

Next, you should apply the theme to your blog and generate the stylesheets. Follow the [install instructions](#applying-the-dark-theme-to-your-blog).

## Removing the theme

### If you installed as a Git submodule

From your Octopress blog's directory,

Remove the theme entry from the __.gitmodules__ file. The entry should look like this:
```
[submodule ".themes/dark"]
  path = .themes/dark
  url = https://github.com/octopress-themes/classic-dark.git
```

Remove the theme from the __.git/config__ file. The entry should look like this:
```
[submodule ".themes/dark"]
  url = https://github.com/octopress-themes/classic-dark.git
```

Remove the theme files with Git.
``` sh
git rm  --cached .themes/dark
```

Your files should be removed. If you want to go back to using the default theme, follow the [Octopress default theme install instructions](#applying-the-classic-theme-to-your-blog).

### If you installed as a download package

From your Octopress blog's directory,

1. Remove the __dark__ directory from __.themes/dark__.
2. Follow the [Octopress default theme install instructions](#applying-the-classic-theme-to-your-blog).

## Applying the dark theme to your blog

Follow this set of instructions whenever you made a new install or update to your themes.

``` sh
rake install[dark]
rake generate
```

Take a look at the changes using the in built Octopress local server at http://localhost:4000

``` sh
rake preview
```

If everything looks ok, deploy it.

``` sh
rake deploy
```

## Applying the classic theme to your blog

Follow this set of instructions when you want to install the default Octopress theme. It is largely similar to the instructions for installing a new theme. Only the name of the theme has changed.

``` sh
rake install[classic]
rake generate
```

Take a look at the changes using the in built Octopress local server at http://localhost:4000

``` sh
rake preview
```

If everything looks ok, deploy it

``` sh
rake deploy
```

## Support

Should you have any problems, raise an issue on this repository.

## Note

[Octopress themes](http://octopressthemes.com) is not affiliated with the official Octopress project.

A link to [Octopress themes](http://octopressthemes.com) has been added to the footer. You can remove it if you want to.

## Other themes

More themes are available on [Octopress themes](http://octopressthemes.com). Feel free to take a look.

## License

Copyright &copy; 2012. Wong Liang Zan. MIT License
