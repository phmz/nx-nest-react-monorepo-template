# Nx Nest React Monorepo Template

This is a monorepo template for a project with an API built using Nest.js and a frontend built using React and Vite. It uses Nx to manage the monorepo structure and provides a shared-types library for sharing types between the API and the frontend.

## Getting Started with the Template

1. Clone the repository:

   ```bash
   git clone git@github.com:phmz/nx-nest-react-monorepo-template.git <project-name>
    ```
   Replace `<project-name>` with the name of your project.

2. Change to the project directory:

   ```bash
   cd <project-name>
   ```
   
3. Remove the `.git` directory:

   ```bash
    rm -rf .git
    ```
   
4. Initialize a new git repository:

   ```bash
   git init
   git add .
   git commit -m "chore: initial commit"
   git remote add origin <remote-url>
   git push -u origin main
   ```
   
## Customizing the template

1. Change the npmScope value in the `nx.json` file:

   ```json
   {
     "npmScope": "app"
   }
   ```

2. Change the name value in the `package.json` file:

   ```json
   {
     "name": "nx-nest-react-monorepo-template"
   }
   ```

## Running the Projects

- To run the API:

  ```bash
  nx serve api
  ```

- To run the frontend:

  ```bash
  nx serve frontend
  ```

- To run e2e tests for the API:

  ```bash
  nx e2e api-e2e
  ```

## Workspace Setup

The following commands were used to generate this template. You don't need to run these commands again, as the generated files are already included in the repository. These instructions are for reference purposes.

1. Update the Nx CLI globally:

   ```bash
   npm install -g nx@latest
   ```

2. Create a new Nx workspace:

   ```bash
   npx create-nx-workspace@latest nx-nest-react-monorepo-template --preset=empty --packageManager=pnpm
   ```

3. Change to the workspace directory:

   ```bash
   cd nx-nest-react-monorepo-template
   ```

4. Add Nest.js support to the workspace:

   ```bash
   pnpm add -D @nrwl/nest
   ```

5. Create a new Nest.js API:

   ```bash
   nx g @nrwl/nest:application api
   ```

6. Create a new React frontend with Vite:

   ```bash
   nx g @nx/react:app frontend --bundler=vite
   ```

7. Create a shared-types library:

   ```bash
   nx g @nrwl/js:library shared-types
   ```
    Choose tsc as the library builder when prompted.

8. Create a custom eslint rule

   ```bash
   nx g @nx/linter:workspace-rule custom-rule
   ```
