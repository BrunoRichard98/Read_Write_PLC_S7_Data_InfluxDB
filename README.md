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
1. Ensure you have Conda installed.
2. Install the dependencies:
   ```bash
   pip install influxdb_client 
   pip install pandas
   ```
Workspace
(rerun without)
Collecting workspace information

Run the script in Jupyter Notebook to query data from InfluxDB.
Node-Red
Import the flow Read_Write_S7_Data_Node-Red_InfluxDB.json into Node-Red.
Configure the nodes:
s7 endpoint: Set the IP address, port, rack, and slot of the PLC.
influxdb: Set the hostname, port, and bucket of InfluxDB.
Start the flow to read and write data.
Node-Red Flow
Description
The flow performs the following steps:

Read data from the PLC: Using the s7 in node.
Format the payload: Using the function node.
Send to InfluxDB: Using the influxdb out node.
Notes
Ensure that InfluxDB is configured and accessible at http://localhost:8086.
Replace authentication and configuration values as needed.
License
This project is distributed under the MIT license. See the LICENSE file for more details.

Contact
For questions or support, contact us at: support@example.com. ```
