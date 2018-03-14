### Quick setup:

1. Create project directory:
    ```$bash
    mkdir ~/project
    cd ~/project
    ``` 
    
2. Clone `Docker` repo in the `project` directory:
    ```$bash
    git clone git@github.com:red-y/OrderyDockerHosting.git
    ```

3. Clone `API` repo in the `project` directory:
    ```$bash
    git clone git@github.com:red-y/OrderyDelivery.git
    ```
    
4. Clone `APP` repo in the `project` directory:
    ```$bash
    git clone git@github.com:red-y/OrderyWebApp.git
    ```
    
5. Enter the `OrderyDockerHosting` folder and rename `env.dev` to `.env`
    ```$bash
    cp env.dev .env
    ```
    
6. Run your containers:
    ```$bash
    docker-compose up -d
    ```
7. Open your project’s .env file and set the following:
