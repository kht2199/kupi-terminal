# Install with docker

-   Install [docker](https://www.docker.com/)
-   Install [nodejs](https://nodejs.org/en/)
-   Install [yarn](https://yarnpkg.com/en/docs/install)
-   Copy ignored by default files ```cp -R ./defaults/. ./```
-   Fill stocks private keys in ```./private/keys.json``` [guide](https://github.com/kupi-network/kupi-terminal/blob/master/KEYS.md)
-   Set mongo password in ```./private/mongo.json``` and ```./private/mongo.env```
-   Set auth password in ```./private/auth.json```
-   install nodejs packages
    ```
    yarn
    ```
-   Build and run containers
    -   for server+mongo version (react or vue need run separately)
        ```
        docker-compose up
        ```
    - for express+mongo+react version (in development, not ready)
        ```
        docker-compose -f docker-compose-react.yml up
        ```
    - for express+mongo+vue version (vue frontend not ready)
        ```
        docker-compose -f docker-compose-vue.yml up
        ```
    - for mongo
        ```
        docker-compose -f docker-compose-mongo.yml up
        ```
-   Open ```http://localhost:8080``` for vue-client or ```http://localhost:8041``` for react-client
