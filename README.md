# Typescript + Next.js + storybook + MUI(styled component) starter

# Stack

- VueJS (typescript)
- Vuetify 3
- Prettier
- Axios
- Pinia
- Perfect Scrollbar

<br/>
<br/>

# Requirements
- Node v19.7.0
- pnpm 9.4.0

<br/>
<br/>

# Getting Started

```bash
# run development mode
pnpm dev

# build web application
pnpm build

## Setting up project specifics

- Ensure `Format on save` is enabled in your VSCode workspace settings to facilitate linting and formatting with Prettier

- **Ensure you have updated all `STARTER!:` comments in the codebase**

<br/>
<br/>

# Understanding Husky

Husky is a pre-commit hook that runs package commands, such as formatting and linting, on the codebase before your commits. This is to ensure that the codebase is always consistent and clean.

## Bypassing Husky hooks

In a default flow, Husky will run the pre-commit hooks on every commit. However, there are times where you may want to bypass this, such as when you are committing a WIP. To do so, simply add the `--no-verify` flag to your commit command:

```bash
git commit -m "WIP: this is a work in progress" --no-verify
```

## Setting up Husky (Optional)

Husky requires some additional work in order to play nicely with GUI git clients like [Tower](https://www.git-tower.com/) or [Sourcetree](https://www.sourcetreeapp.com/).

The basic steps to get them running on your GUI client are as follows. **Note:** if you are using nvm as well, you will need to follow up in the subsequent steps.

Create a .huskyrc file in your OSX home directory (~/). Open your terminal and run the following commands:

```bash
cd ~/
touch .huskyrc
vi huskyrc
```

Press i to enter vim's instert mode. Copy paste the following line:

#### Without nvm

```bash
PATH="/usr/local/bin:$PATH"
```

#### [With nvm](https://stackoverflow.com/a/72279243)

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

Press `esc`. Then `:` and `wq`. Finally press `enter`.

<br/>
<br/>

## Code practice

Maintain a consistent code style throughout this codebase. This includes:

### CSS properties order

- functions
- width
- typography
- misc.

Always group properties of similar groups together. E.g. flex, width & max-width, position & top & left, etc.

### Theme usage

Always use theme utilities and properties instead of hardcoding values.

### Clean code

- Ensure there are no unused imports, variables, functions, etc.
- Proper naming conventions