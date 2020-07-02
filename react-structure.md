# React Folders Structure

```
.
├── @types
├── scripts
├── src
│   ├── api
│   ├── components
│   │   ├── base
│   │   │   ├── button
│   │   │   │   ├── index.tsx
│   │   │   │   └── styles.ts
│   │   │   └── text-field
│   │   │       ├── index.tsx
│   │   │       └── styles.ts
│   │   ├── containers
│   │   └── modals
│   ├── contexts
│   ├── hooks
│   ├── res
│   │   ├── assets
│   │   │   ├── fonts
│   │   │   ├── icons
│   │   │   └── images
│   │   ├── colors
│   │   ├── constants
│   │   ├── dimens
│   │   ├── env-config
│   │   ├── i18n
│   │   └── theme
│   ├── store
│   │   └── user
│   │       ├── actions.ts
│   │       ├── reducer.ts
│   │       └── selectors.ts
│   ├── utils
│   └── views
│       ├── dashboard
│       │   ├── __tests__
│       │   ├── components
│       │   │   └── header
│       │   │       ├── index.tsx
│       │   │       └── styles.ts
│       │   ├── helpers.ts
│       │   ├── hooks
│       │   ├── index.tsx
│       │   ├── routes.ts
│       │   ├── styles.ts
│       │   └── types.ts
│       └── profile
│           ├── __tests__
│           ├── components
│           ├── contexts
│           ├── helpers.ts
│           ├── hooks
│           ├── index.tsx
│           ├── routes.ts
│           ├── sections
│           │   ├── account
│           │   │   ├── components
│           │   │   ├── index.tsx
│           │   │   └── styles.ts
│           │   ├── change-password
│           │   │   ├── index.tsx
│           │   │   └── styles.ts
│           │   └── settings
│           │       ├── index.tsx
│           │       └── styles.ts
│           ├── store
│           │   ├── actions.ts
│           │   ├── reducer.ts
│           │   └── selectors.ts
│           ├── styles.ts
│           └── types.ts
└── test-utils
```

## Folders

### **@types**

The area where all augmentation modules are placed, we can patch existing objects by importing and then updating them.

### **scipts**

Here, we are going to place all pre-commit, pos-commit and build scripts.

### **src/api**

It holds all the functions related to API calls and its helpers.

### **src/components**

Here, we would have all our shared components that are being used in the app more than once or are not a screen.

### **src/contexts**

Here, we can have all shared contexts that are being used in the app more than once in multiple screens.

### **src/hooks**

All shared custom hooks that are being used in multiple screens and components.

### **src/res**

Resource path where we can place all our assets, colors, constants, dimens, env-config, i18n, themes and so on.

### **src/store**

Redux data that is shared in most or all screens.

### **src/utils**

It holds all helpers and utils that are used in multiple screens and components.

### **src/views**

All important screens/views in the project, each screen/view can have their own tests, contexts, hooks, store paths related to that the screen/view mainly, as well as, their own types.ts (only types that need to be exported), routes.ts, helpers.ts and styles.ts files. The idea here is having multiple sections under specific screens like tabs or steps (if applicable). If those tabs/steps have its own "sections", they may be a good fit to have its own space under views path. That way, we can keep the structure organised and prevent too deep and complex nested hierarchy.

### test-utils

Here we can place all settings and setup files needed for test libraries, such as Jest, React Testing Library, Enzyme and Cypress.
