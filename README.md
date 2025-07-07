![Node-RED](https://img.shields.io/badge/Node--RED-%238F0000.svg?style=for-the-badge&logo=node-red&logoColor=white) 
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 
![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=for-the-badge&logo=InfluxDB&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

# Project: Data Integration with InfluxDB and Node-Red

This project demonstrates how to integrate data from a PLC (Programmable Logic Controller) with the InfluxDB database using Node-Red and Python. It includes two main files: a Python script for reading data from InfluxDB and a Node-Red flow for reading and writing data to the PLC.

---

## Project Structure

### Files
- **`Read_Data_InfluxDB_Python.ipynb`**: Python script for querying data from InfluxDB and converting it to a DataFrame using the Pandas library.
- **`Read_Write_S7_Data_Node-Red_InfluxDB.json`**: Node-Red flow for reading data from a Siemens S7 PLC and sending it to InfluxDB.

---

## Technologies Used

### Python
- **Library `influxdb_client`**: Used to connect and query data from InfluxDB.
- **Library `pandas`**: Used for data manipulation and analysis.
- **Conda Environment**: Recommended for managing dependencies and packages.

### Node-Red
- **Node `s7 in`**: Used for communication with Siemens S7 PLC.
- **Node `function`**: For formatting payload and timestamp.
- **Node `influxdb out`**: For sending data to InfluxDB.
- **Node `debug`**: For displaying debug messages.

### InfluxDB
- **Version 2.0**: Time-series database used for data storage.
- **Flux Query Language**: Language used for querying data in InfluxDB.

---

## Configuration and Execution

### Python
To set up and execute the Python script:
1. **Install Conda**: Ensure Conda is installed on your system.
2. **Install Dependencies**: Run the following commands to install required libraries:
   ```bash
   pip install influxdb_client
   pip install pandas

3. Run the Script: Open the Read_Data_InfluxDB_Python.ipynb file in Jupyter Notebook and execute the cells to query data from InfluxDB.


### Node-Red
To set up and execute the Node-Red flow:

1. **Import the Flow**: Import the Read_Write_S7_Data_Node-Red_InfluxDB.json file into Node-Red.
2. **Configure Nodes**:
- S7 Endpoint: Set the IP address, port, rack, and slot of the Siemens S7 PLC.
- InfluxDB Node: Configure the hostname, port, and bucket for InfluxDB.
3. **Start the Flow**: Deploy and start the flow to read and write data.

**Node-Red Flow Description**
The Node-Red flow performs the following steps:

1. Read Data from PLC: Using the s7 in node to fetch data from the Siemens S7 PLC.
2. Format Payload: Using the function node to format the payload and timestamp.
3. Send Data to InfluxDB: Using the influxdb out node to store the data in InfluxDB.

**Notes**
Ensure InfluxDB is properly configured and accessible at http://localhost:8086.
Update authentication and configuration values as needed for your environment.