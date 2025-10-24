
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