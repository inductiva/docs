
# Inductiva.AI Documentation Repository

This repository contains all the documentation and static assets for **Inductiva.AI**. It is structured to support multiple simulators, tutorials, FAQs, webinars, and other resources. The content is organized so that it can be directly used to generate a structured website.

---

## Repository Structure

The repository is divided into two main folders:

```

/docs    -> All Markdown documentation files
/public  -> All static files needed by the Markdown files (images, gifs, etc.)

```

Both folders follow the same structure by simulator:

```

/docs/<simulator>
/public/<simulator>

```

### Example:

```

docs/openfoam/
├── 0.versions-and-containers.md
├── 1.tutorials
│   ├── 0.setup-test.md
│   ├── 1.quick-start.md
│   ├── convert-allrun-script-into-python-commands.md
│   ├── generate-wind-tunnel-dataset
│   │   ├── index.md
│   │   └── sections
│   │       ├── section1.md
│   │       ├── section2.md
│   │       ├── section3.md
│   │       ├── section4.md
│   │       ├── section5.md
│   │       └── section6.md
│   ├── mpi-cluster-tutorial.md
│   ├── openfoam-mpi-setup
│   │   ├── openfoam-behaviour.md
│   │   └── sections
│   │       ├── openfoam-esi.md
│   │       └── openfoam-foundation.md
│   └── run-occdrivaerstaticmesh-case
│       ├── index.md
│       └── sections
│           ├── section1.md
│           ├── section2.md
│           ├── section3.md
│           └── section4.md
├── 2.faq
│   └── faq.md
├── 3.webinars
│   ├── openfoam-cfd-dataset.md
│   └── openfoam-video-tutorial.md
└── index.md

```

---

## Documentation Guidelines

### Index Files

- Each simulator folder must have an `index.md` file.  
- Each subfolder inside /docs/simulator represents a submenu in the website and should also have an `index.md` file.
- On some cases the index will not be shown to make the docs cleaner. If you need to have the index present on the menu make sure to add this to the markdown file:

```
navigation:
  title: Name to show on the menu
  show: true 
```
In this case, title will be the text shown on the menu (optional).

> **Note**: Since index files do not show on the url we have some less than ideal behaviours with url links. For example, if you are at `/guides/recipes` the borwser thinks recipes is a file (because index is omited). So, if you have a relative link to `./storage-related/` it will not work because the browser will look for `/guides/storage-related/` instead of `/guides/recipes/storage-related/`. To avoid this, either use absolute links (starting with /).

### Menu Structure

- Subfolders inside a simulator folder create **submenus** on the final website.  
- Files inside each folder (or subfolder) will automatically be displayed in the submenu.

### Controlling Menu Order

The website sorts menu entries **alphabetically by filename**. To enforce a custom order:

- Prefix filenames with numbers: `1.filename.md`, `2.filename.md`, etc.  
- The prefix will **not** appear in the URL; it is only used for sorting the menu.

Example:

```

1.quick-start.md
2.advanced-setup.md

```

This ensures `quick-start` appears before `advanced-setup` in the menu.

---

### Controlling Sub-Menu text

Like it was stated before, subfolders inside a simulator folder create **submenus** on the final website. This submenus will
have the text of the index title or the folder actual name. But there is a way to control this behaviour. In order to configure a submenu
entry just create a file called `.navigation.yml` with the following content:

```
title: Minor Versions
icon: i-lucide-tag
```

Here title will control the text on the menu and icon will define an icon for that sub menu (optional).

> **Note**: This navigation file will also affect the breadcrumbs, meaning, if you have a navigation file in a simulator
folder with the title `Openfoam` in the breadcrumbs it will appear Openfoam instead of the title of the index.

## Public Folder Guidelines

- All static assets (images, gifs, videos, etc.) referenced in the Markdown files should be placed under `/public/<simulator>`.  
- The folder structure in `/public` should should be similar to `/docs` just to keep things organized, but its not mandatory. If many markdowns share an asset it can be placed in a common folder inside public.

---


## Notes

* The numbering prefix in filenames is **optional** but recommended to control menu order.
* Nested folders in tutorials or other submenus will automatically be displayed in the final website menu hierarchy.

---

## How to add new simulators to the menu

In order to add a new simulator to the simulators menu a new entry needs to be added to the file `menu.json`.
Keep in mind that title will be the text shown in the menu and the top left corner of the simulator documentation page and the path is the path to the simulator folder in reference to docs/. Meaning, for OpenFOAM this is the entry that needs to be added:

```
        {
          "title": "OpenFOAM",
          "path": "openfoam/"
        },
```