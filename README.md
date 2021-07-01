# Overview

This repo is used to host Swagger for API documentation

## Steps to manually configure in your own repository

1. Download the latest stable release of the Swagger UI [here](https://github.com/swagger-api/swagger-ui/releases).

2. Extract the contents and copy the "dist" directory to the root of your repository.

3. Move the file "index.html" from the directory "dist" to the root of your repository.
    ```
    mv dist/index.html .
    ```

4. Copy the YAML specification file for your API to the root of your repository:
 - [docs/catalog-repo.yaml](docs/catalog-repo.yaml)

5. Edit [index.html](index.html) and change the `url` property to reference your local YAML file.
    ```javascript
        const ui = SwaggerUIBundle({
            url: "./docs/catalog-repo.yaml",
        ...
    ```
