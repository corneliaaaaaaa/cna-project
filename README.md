# cn-project
by amber, erica, jtc, daphne, wsa

## Setup
### Backend & Database Setup

```shell
cd be
cp .env.example .env
cp docker-compose.yaml.example docker-compose.yaml
```

Fill in necessary environment variables in `.env`.
```
MONGO_URI="mongodb://root:example@host.docker.internal:27017"
DATABASE="network-project"
SERVICE_ADDRESS=":8000"
```

Then run
```shell
docker-compose up --build -d
```
You may check whether the database is up from `localhost:8082`, and the websocket connection endpoint is `ws://<SERVICE_ADDRESS>/socket`


### Frontend Setup

```shell
cd fe
cp .env.example .env
```

Fill in the below environment variable in `.env`.
```shell
REACT_APP_ClIENT_ADDRESS="ws://localhost:8000/socket"
```

Then run
```
yarn start
```

## How to start and play
Open http://localhost:3000.
