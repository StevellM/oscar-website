
## Website for the Oscar project.

Sebastian Gutsche <gutsche@mathematik.uni-siegen.de>, May 2018

### How to contribute

Fork this repository on GitHub, and provide a Pull Request to it.
To test your changes locally, run
```
jekyll serve
```
in the main directory.

### How to contribute a News post

To contribute a new News post, please follow these steps

1. Create a new `.md` file in the folder `news/_posts`. The filename
   must be of the format `YYYY-MM-DD-title-of-post.md`.

2. At the beginning of your `.md` file, put
```
---
layout: post
title: Title of your post
---
```
3. Afterwards, you can write your post in markdown syntax. Please note that the title
   is put in automatically, so you do not have to put it in the post separately.

### How to contribute an example notebook

To contribute a new example notebook, please follow these steps

1. Create a binder-ready repository on GitHub, containing the notebook file.
   Assume the repository is `https://github.com/myusername/mybinderrepo`
   and the notebook file is `mynotebook.ipynb` inside this repository.

   For an example repository, see [OSCARBinder](https://github.com/oscar-system/OSCARBinder).

2. Create a thumbnail for the notebook, say `mythumbnail.png` and store it in `/public/thumbnails`.

3. Create a new `.md` file in the folder `examples/_posts`. The filename
   must be of the format `YYYY-MM-DD-title-of-notebook.md`.

4. At the beginning of your `.md` file, add the following lines:
```
---
layout: post
title: My new notebook
repository: myusername/mybinderrepo
filename: mynotebook
author: My Name
thumbnail: mythumbnail.png
---
```
Please adjust all entries accordingly. All further content of the file is ignored.

### How to add a new documentation URL

Please add a new entry to the `_data/documentation_pages.yml` file, of the following form:
```
- name: Singular.jl
  documentation_url: https://www.singular.uni-kl.de
  description: The interface to Singular
               from Julia
```

### How to add a new contributor

Please add a new entry to the `_data/contributors.yml` file, of the following form:
```
- name: Sebastian Gutsche
  affiliation: University of Siegen
  email: gutsche@mathematik.uni-siegen.de
  website: http://sebasguts.github.io
```
All three entries, `affiliation`, `email`, and `website` are optional. If you provide an `email` and a `website`, the name will link to the website.

### How to add a new software dependency

Please add a new entry to the `_data/used_software.yml` file, of the following form:
```
- name: GAP
  website: http://www.gap-system.org
```

### How to add a new meeting subpage

Send an email to [Sebastian Gutsche](mailto:gutsche@mathematik.uni-siegen.de) and ask for help.

