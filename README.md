# Lab 4: NoSQL and Column-oriented Databases

In Lab 4, we will explore NoSQL databases and column-oriented databases. The lab introduces the concept of NoSQL databases as an alternative to traditional relational databases, focusing on their ability to efficiently handle unstructured or semi-structured data.

Additionally, the lab covers column-oriented databases (or column stores), a type of database optimized for storing and querying columnar data. You will learn about the advantages of columnar storage for analytics workloads, including improved query performance.


## Setup Instructions (Docker)

We will be using a docker environment similar to the one we used in previous labs. Download the lab folder on your local machine, and from the lab directory, run this command (where your `docker-compose.yml` file is located):

```bash
$ docker-compose up --build
```

After running the docker-compose command, you will see a URL in the terminal output. Paste the URL in the web browser, or if you are using VSCode, you can paste it after selecting `jupyter kernel` in VSCode to open the Jupyter notebook.


## Turning In Your Lab 4

You will upload the following question notebooks on Canvas:

- `lab4_NoSQL_questions.ipynb`
- `lab4_columnsStore_questions.ipynb`