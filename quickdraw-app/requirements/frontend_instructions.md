project overview
- webapp that operates like google paint, where users can draw on a canvas and save their work.

feature requirements
- users can draw on a canvas
- users can save their work
- users can see a list of all the drawings as different projects
- users by default start with a blank canvas
- users can copy and paste images into the canvas
- users can download their work
- users can upload their work
- users can delete their work
- users can copy their work
- users can paste their work

Relevant docs
- react js

- nextjs
- shadcn
current file structure
quickdraw/
├── app/
│   ├── page.tsx                 # Home page (redirects to /draw)
│   ├── draw/
│   │   └── page.tsx            # Main drawing canvas page
│   ├── projects/
│   │   └── page.tsx            # Gallery of user's saved projects
│   └── layout.tsx              # Root layout
├── components/
│   ├── canvas/
│   │   ├── drawing-canvas.tsx  # Main canvas component
│   │   ├── toolbar.tsx         # Drawing tools and controls
│   │   └── color-picker.tsx    # Color selection component
│   ├── ui/                     # shadcn components
│   │   ├── button.tsx
│   │   ├── dialog.tsx
│   │   └── dropdown-menu.tsx
│   ├── project/
│   │   ├── project-card.tsx    # Individual project display
│   │   └── project-grid.tsx    # Grid layout for projects
│   └── layout/
│       ├── header.tsx          # App header with navigation
│       └── footer.tsx          # App footer
├── lib/
│   ├── types/
│   │   └── project.ts          # Type definitions
│   └── utils/
│       ├── canvas-utils.ts     # Canvas helper functions
│       └── storage-utils.ts    # Storage helper functions
├── public/
│   └── assets/
├── styles/
│   └── globals.css
└── requirements/
    └── frontend_instructions.md
Rules
- all new components should go in /components and be named like example-component.tsx unless otherwise specified
- all new pages go in /app
- for the pages (seee next.js app directory docs) lets start off with just a draw page that has all of these things. then we will have a button user can click to go to a page where they can see all of their projects. we will use an authentication service to save the user's work.