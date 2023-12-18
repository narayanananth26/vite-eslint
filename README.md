NOTE: Vite comes with ESLint preconfigured, so there's no need to explicitly install the 'vite-plugin-eslint' plugin now.

# ESLint configuration in Vite React app in VS Code
1.  Download the ESLint extension

3.  Run the following command in terminal   
    ```
    npm i eslint vite-plugin-eslint eslint-config-react-app --save-dev
    ```
3. Create a `.eslintrc.json` file and paste the following snippet into it  

   ```json
   {
     "extends": "react-app"
   }
   ```
5. Update the `vite.config.js` file as follows:

   ```javascript
   import { defineConfig } from "vite";
   import react from "@vitejs/plugin-react";
   import eslint from "vite-plugin-eslint";
  
   // https://vitejs.dev/config/
   export default defineConfig({
   	plugins: [react(), eslint()],
   });
   ```
   
