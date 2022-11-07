# @criticalmanufacturing/cli documentation

## How to contribute
1. Clone this git repository to your machine. Make sure you checkout the `documentation` branch:
    ```sh
    git clone --branch documentation https://github.com/criticalmanufacturing/cli.git
    ```
    > if you don't have push access, please create a fork and proceed using the new fork.

3. Run the command help pages generator (replace the **path** with your own):
    ```sh
    npm run help:init
    npm run help:gen [path]/bin/Debug/cmf.dll
    ```

4. Now you can build and render the documentation:
    ```sh
    npm run build
    npm run serve
    ```
   > the site is available at http://localhost:8081

## Publishing to GitHub Pages
We raw publish to GitHub Pages. The official repository uses the `gh_pages` branch. Simply push the content of the output folder to this branch. Example:
```sh
cd dist
git init
git remote add origin https://github.com/criticalmanufacturing/cli.git
git add .
git commit -m "publish"
git push origin master:gh_pages -f
```