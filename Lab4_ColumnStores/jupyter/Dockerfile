# Use an official Python runtime as a parent image
FROM python:3.8

# Set the working directory in the container
WORKDIR /app

# Install required Python packages
RUN pip install jupyter pandas sqlalchemy ipython-sql numpy psycopg2-binary clickhouse-driver pandas scikit-learn clickhouse-sqlalchemy

# Expose the port for Jupyter Notebook
EXPOSE 8888

# Start Jupyter Notebook when the container launches
CMD ["jupyter", "notebook", "--ip='*'", "--port=8888", "--no-browser", "--allow-root", "--notebook-dir=/app", "--ServerApp.iopub_data_rate_limit=1000000000"]
