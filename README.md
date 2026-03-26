# Lab 4: NoSQL and Column-oriented Databases

In Lab 4, we will explore NoSQL databases and column-oriented databases. The lab introduces the concept of NoSQL databases as an alternative to traditional relational databases, focusing on their ability to efficiently handle unstructured or semi-structured data.

Additionally, the lab covers column-oriented databases (or column stores), a type of database optimized for storing and querying columnar data. You will learn about the advantages of columnar storage for analytics workloads, including improved query performance.

---

### Download Data
Visit the following link and put the content of the folders in your cloned repository.

https://drive.google.com/drive/folders/1ccDEAMC6fqKa5ySIpT9PnYWeY-A12rFJ?usp=sharing


## Setup Instructions (Docker)

We will be using a docker environment similar to the one we used in previous labs. Download the lab folder on your local machine, and from the lab directory, run this command (where your `docker-compose.yml` file is located):

```bash
$ docker-compose up --build
```

After running the docker-compose command, you will see a URL in the terminal output. Paste the URL in the web browser, or if you are using VSCode, you can paste it after selecting `jupyter kernel` in VSCode to open the Jupyter notebook.

---

## Lab 4 Files and Setup

The Lab 4 folder contains two sub-folders:

- `Lab4_ColumnStores`
- `Lab4_NoSQL`

### Lab4_ColumnStores

- This folder contains `jupyter`, `postgres`, `configs` and the `data` subfolder.
- The `lab4_columnsStore_questions` and `lab4_columnsStore_tutorial` notebooks are located inside the `jupyter` folder.
- The `data` folder contains the datasets; the other folders are used for the configuration of PostgreSQL and ClickHouse.
- For running the notebooks you can run the docker-compose command from the `Lab4_ColumnStores` folder, which contains the `docker-compose.yml` file.

### Lab4_NoSQL

- This folder contains `data`, `dump`, and `notebooks` subfolders.
- The `lab4_NoSQL_questions` and `lab4_NoSQL_tutorial` notebooks are located inside the `notebooks` folder.
- The `data` folder contains the datasets; the other folders are used for configuration of MongoDB.
- For running the notebooks you can run the docker-compose command from the `Lab4_NoSQL` folder, which contains the `docker-compose.yml` file.

### Important: Additional Setup for Lab4_NoSQL

To run the notebook and load the dataset into the MongoDB container, follow these steps:

1. Run `docker compose up --build` in the main folder where `docker-compose.yml` is present to start your Jupyter notebook and create your MongoDB container.
2. Open another terminal and run the following to get inside the Mongo container:
   ```bash
   docker exec -it my-mongo-container bash
   ```
3. Run the following inside the Mongo container to load data into MongoDB:
   ```bash
   mongorestore --db movie_recommend /dump/movie_recommend
   ```

---

## Turning In Your Lab 4

You will upload the following question notebooks on Canvas:

- `lab4_NoSQL_questions.ipynb`
- `lab4_columnsStore_questions.ipynb`