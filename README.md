![alt text](https://github.com/jutaporn13/SubQuery-M3-1/blob/8a10376e9fec58c90f177460b41e90ff843d0c2b/Ubuntu%2064-bit%20-%20Subquery%20Module%203%20-%20Jutaporn-2021-12-20-05-47-09.png)

# What is SubQuery?

SubQuery powers the next generation of Polkadot dApps by allowing developers to extract, transform and query blockchain data in real time using GraphQL. In addition to this, SubQuery provides production quality hosting infrastructure to run these projects in.

# SubQuery Example - Account transfers

This subquery example indexes the amount transferred of each account and it is an example of a 1-many entity relationshp. In other words, one account can have many receiving addresses.

# Getting Started

### 1. Clone the entire subql-example repository

```shell
git clone https://github.com/subquery/tutorials-account-transfers.git

```

### 2. Install dependencies

```shell
cd <folder>
yarn
```

### 3. Generate types

```shell
yarn codegen
```

### 4. Build the project

```shell
yarn build
```

### 5. Start Docker

```shell
docker-compose pull & docker-compose up
```

### 6. Run locally

Open http://localhost:3000/ on your browser

### 7. Example query to run

```shell
query{
  transfers(first: 3){
    nodes{
      id
      amount
      blockNumber
      to{
        id
      }
      }
    }
  }
```

