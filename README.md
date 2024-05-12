# Template Project

Welcome to my Template Project! This is a robust starting point designed to facilitate the initiation of new web projects with a strong foundation and adherence to best practices.

## Overview

This template is curated with the goal of streamlining project setup and promoting collaborative work. It encompasses a carefully selected set of technologies, established guidelines, and project structure to enhance productivity and maintainability.

### Apps and Packages

- `docs`: a [Next.js](https://nextjs.org/) app
- `web`: another [Next.js](https://nextjs.org/) app
- `@repo/ui`: a stub React component library shared by both `web` and `docs` applications
- `@repo/eslint-config`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `@repo/typescript-config`: `tsconfig.json`s used throughout the monorepo

### Technologies Used

- [Next.js](https://nextjs.org/): A React framework for building server-side rendered and static web applications.
- [TypeScript](https://www.typescriptlang.org) (`.ts` files): A statically typed superset of JavaScript that enhances code quality and developer productivity.
- [Tailwind](https://tailwindcss.com) (In prgress): CSS framework for styling components. It has the ability to [remove unused CSS](https://tailwindcss.com/docs/optimizing-for-production) to optimize file size and CSS processing speed of the project.
- [Storybook](https://storybook.js.org/) (In progress): An open-source tool for developing UI components in isolation for React, Vue, and Angular.
- [Testing Library](https://testing-library.com/) (In progress): A simple and intuitive testing library for React applications.
- [Cypress](https://www.cypress.io/) (In progress): An end-to-end testing framework for web applications.
- [Turborepo](https://turbo.build/): A monorepo toolset for managing multiple packages and applications.

### Code Quality Tools

- **ESLint**: A pluggable linting utility for JavaScript and TypeScript that identifies and fixes code errors.
- **Prettier**: An opinionated code formatter that ensures consistent code style.
- **Husky (In progress)**: A Git hooks manager that enables running scripts in response to Git events.

## Development

### Commit Convention

Before you create a Pull Request, please check whether your commits comply with
the commit conventions used in this repository.

When you create a commit we kindly ask you to follow the convention
`category(scope or module): message` in your commit message while using one of
the following categories:

- `feat / feature`: all changes that introduce completely new code or new
  features
- `fix`: changes that fix a bug (ideally you will additionally reference an
  issue if present)
- `refactor`: any code related change that is not a fix nor a feature
- `docs`: changing existing or creating new documentation (i.e. README, docs for
  usage of a lib or cli usage)
- `build`: all changes regarding the build of the software, changes to
  dependencies or the addition of new dependencies
- `test`: all changes regarding tests (adding new tests or changing existing
  ones)
- `ci`: all changes regarding the configuration of continuous integration (i.e.
  github actions, ci system)
- `chore`: all changes to the repository that do not fit into any of the above
  categories

  e.g. `feat(components): add new prop to the avatar component`

If you are interested in the detailed specification you can visit
https://www.conventionalcommits.org/ or check out the
[Angular Commit Message Guidelines](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines).

### Build

To build all apps and packages, run the following command:

```
cd my-turborepo
pnpm build
```

### Develop

To develop all apps and packages, run the following command:

```
cd my-turborepo
pnpm dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd my-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Tasks](https://turbo.build/repo/docs/core-concepts/monorepos/running-tasks)
- [Caching](https://turbo.build/repo/docs/core-concepts/caching)
- [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching)
- [Filtering](https://turbo.build/repo/docs/core-concepts/monorepos/filtering)
- [Configuration Options](https://turbo.build/repo/docs/reference/configuration)
- [CLI Usage](https://turbo.build/repo/docs/reference/command-line-reference)
