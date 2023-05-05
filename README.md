# Nx Nest React Monorepo Template

This is a monorepo template for a project with an API built using Nest.js and a frontend built using React and Vite. It uses Nx to manage the monorepo structure and provides a shared-types library for sharing types between the API and the frontend.

## Workspace Setup

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
   nx generate @nrwl/nest:application api
   ```

6. Create a new React frontend with Vite:

   ```bash
   nx g @nx/react:app frontend --bundler=vite
   ```

7. Create a shared-types library:

   ```bash
   nx generate @nrwl/js:library shared-types
   ```
   
Choose tsc as the library builder when prompted.

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
  
