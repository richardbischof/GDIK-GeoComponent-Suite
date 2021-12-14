# MP Map
Interactive map as a web component based on the master portal API

## Usage
### Development setup
To start a development environment for development purposes follow these steps:
1. npm install
2. add *import 'babel-polyfill'* to index.js
3. npm run dev

### Import web component as npm package
The recommended way to integrate the web component is to install the npm package. To do this follow the steps below:
1. If you still need a [personal access token](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html) for gitlab, create it now.
2. Create a .npmrc file in the root directory of your project if it does not already exist
3. Add the following code to your .npmrc file:
    ```
   @lgln-gitlab:registry=https://gitlab.com/api/v4/projects/31983335/packages/npm/
   //gitlab.com/api/v4/projects/31983335/packages/npm/:_authToken=<Git-Token>
   ```
4. Now execute the following command in the root directory:
    ```
    npm i @lgln/waas-web-mp-map
    ```
5. To use the component u have to import it with ``import '@lgln/waas-web-mpmap/src/index'``

### Attributes
####Tag: <mp-map>

| Name       | Required | Type       | Default    | Reactive | Description |
|------------|----------|------------|------------|----------|-------------|
| lon        | no       | string     | 448360.0   | yes      | center position |
| lat        | no       | string     | 5888434.0  | yes      | center position |
|layer       | no       | string     | 1001       | yes      | 
| config-url | no       | string     | -          | no       | zoom level |
| map-height | no       | string     | 100%       | no       | height of the map, css value |
| map-width  | no       | string     | 100%       | no       | width of the map, css value |

###Examples
#### Example usage in Vue
```<mp-map config-url="data/config.json" :lon="center[0]" :lat="center[1]"></mp-map>```
