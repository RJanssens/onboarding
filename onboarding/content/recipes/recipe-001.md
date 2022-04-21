---
title: How to create and publish new recipes
date: 2022-04-20T12:48:06+02:00
draft: true
id: "001"
author: Raf Janssens
categories: ["recipes"]
tags: ["recipe", "hugo", "gitlab"]
summary: How to create and publish new recipes
---
## Introduction

This recipe explains how to add new recipes to the onboarding kit and get them published to the static site.

## Steps

1. If you haven't done so yet, download and install the latest Hugo release from the project's [GitHub Page](https://github.com/gohugoio/hugo). Hugo installation instructions are provided [here](https://gohugo.io/getting-started/installing/). 

2. After installing Hugo, you will probably want to add the directory containing the Hugo executable to your path.

3. Clone the onboarding site from our local GitLab repository:

```
mkdir onboarding
cd onboarding
git clone https://ecoapp.internal.economie.fgov.be/git/ba/onboarding
```

4. Add a new recipe using the hugo executable (replacing xyz below with the recipe identifier:

```
hugo new /recipes/recipe-xyz.md
```

5. You are now ready to create the recipe. A recipe page is a standard markdown page with metadata parameters *id*, *author* and *summary*. Feel free to copy content of this recipe (in directory /content/recipes) or edit the page from scratch:

```
---
title: How to create and publish new recipes
date: 2022-04-20T12:48:06+02:00
draft: true
id: "001"
author: Raf Janssens
summary: How to create and publish new recipes
---
## Introduction

...
```

6. Once you're done, test that the recipe is visible and well-formated by starting Hugo in the onboarding project's base directory:

```
hugo server -D
```

7. When the content is finalized, you can add your changes to the local repository. A CI-CD pipeline will launch when the merge request is approved to publish the changes.

[![Recipes overview](/img/back.png)](/code/recipes)


## Related links

| Link | Description |
| ----------- | ----------- |
| [Hugo](https://github.com/gohugoio/hugo) | Hugo GitHub page |
| [Install Guide](https://gohugo.io/getting-started/installing/) | Hugo installation instructions |
| [Onboarding GitLab site](https://ecoapp.internal.economie.fgov.be/git/ba/onboarding/) | Onboarding GitLab site |
