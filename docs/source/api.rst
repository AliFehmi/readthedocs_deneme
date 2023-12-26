API
===

.. _api:

.. autosummary::
   :toctree: generated

   lumache


monitoring_panels_dd_go.py
---------------------------

  Generates dynamic monitoring panels for Grafana dashboards using Plotly and Dash.

  **Returns:** JSON configuration for Grafana dashboard panels.

monitoring_dashboard_modular.py
--------------------------------

  Facilitates the modular creation of monitoring dashboards for system performance visualization.

  **Returns:** A Grafana dashboard URL after deploying it to Grafana.

monitoring_dashboard.py
------------------------

  Creates a comprehensive monitoring dashboard for visualizing various metrics of the system in real-time.

  **Returns:** A complete Grafana dashboard JSON object.

observation_standard.py
------------------------

  Standardizes the observation data and prepares it for integration with visualization tools.

  **Returns:** Normalized data suitable for reporting and visualization.

roofline_dashboard.py
----------------------

  Generates a roofline model dashboard for visualizing the computational efficiency of hardware.

  **Returns:** URL to the generated Grafana roofline dashboard.

static_data.py
---------------

  Contains static data structures and configurations used across different modules of the project.

  **Returns:** None (this module acts as a configuration store).

influx_help.py
---------------

  Provides helper functions for interacting with the InfluxDB time-series database.

  **Returns:** Various outputs depending on the function, including success responses or queried data.

observation.py
---------------

  Handles the collection of system observation data and logs it into InfluxDB.

  **Returns:** The duration of the observation process.

probing
-------
  This directory includes scripts that probe the system to gather hardware and performance metrics.

detect_utils.py: 
^^^^^^^^^^^^^^^^
  Utility functions for detecting system hardware and performance characteristics.
  \n **Returns:** Hardware and performance data in a structured format.

remote_probe.py: 
^^^^^^^^^^^^^^^^
  Connects to remote systems to gather necessary metrics for the digital twin.
  \n **Returns:** System metrics and a unique identifier for the probed system.

system_query.py: 
^^^^^^^^^^^^^^^^
  Queries the system to retrieve detailed information about its state and capabilities.
  \n **Returns:** A comprehensive report of the system's current state.

sampling
--------
  This directory contains scripts related to the sampling of system metrics and performance data.

initiate.py: 
^^^^^^^^^^^^
  Initiates the sampling process for gathering system metrics.
  \n **Returns:** The status of the sampling initiation process.

sampling.py: 
^^^^^^^^^^^^
  Handles the sampling of various system metrics for performance analysis.
  \n **Returns:** A process ID for the sampling task.

STREAM
------
  This directory contains scripts for running and parsing the STREAM benchmark, which measures memory bandwidth.

benchmark.py: 
^^^^^^^^^^^^^
  Manages the execution of the STREAM benchmark.
  \n **Returns:** Benchmark results including bandwidth measurements.

detect_utils.py: 
^^^^^^^^^^^^^^^^
  Detects system information relevant to the benchmark.
  \n **Returns:** System information necessary for benchmark configuration.

parse_cpuinfo.py: 
^^^^^^^^^^^^^^^^^
  Parses CPU information to configure the benchmark appropriately.
  \n**Returns:** Parsed CPU data for benchmark setup.

parse_likwid_topology.py: 
^^^^^^^^^^^^^^^^^^^^^^^^^
  Uses LIKWID to parse system topology for benchmark setup.
  \n **Returns:** Topology data to guide benchmark execution.

generate_dt.py
---------------

  Generates the digital twin description based on the collected system data and benchmarks.

  **Returns:** A digital twin description object to be used for further analysis and visualization.

