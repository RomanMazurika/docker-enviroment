### Quick setup:

1. Create project directory:
    ```$bash
    mkdir ~/project
    cd ~/project
    ``` 
    
2. Clone `Docker` repo in the `project` directory:
    ```$bash
    git clone git@github.com:RomanMazurika/docker-enviroment.git
    ```

3. Enter the `OrderyDockerHosting` folder and rename `env.dev` to `.env`
    ```$bash
    cp env.dev .env
    ```
    
4. Run your containers:
    ```$bash
    docker-compose up -d
    ```
