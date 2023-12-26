INTERNALS
=========

.. _internals:

Dashboard
---------

.. autosummary::
   :toctree: generated

   lumache

1) generate_plotly_panels_dd_go.py
++++++++++++++++++++++++++++++++++

This section documents the functions defined in the ``generate_plotly_panels_dd_go.py`` file.

.. _get_next_color:

1.1) get_next_color()
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

The ``get_next_color()`` function cycles through a predefined list of color codes, 

.. rubric:: ⚙ Parameters

- `next_color`: A global variable that keeps track of the current position in the **colors** list.
- `colors`: A global list containing the hexadecimal color codes to be cycled through.

.. rubric:: ↩ Returns

- `Return Type:` `string`
- `Description:` Returns a hexadecimal color code (e.g., `#4A90E2`). This is the next color in the `colors` list.

.. _round_power_of_2(number):

1.2) _round_power_of_2(number)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

The ``_round_power_of_2(number)`` function rounds a given number to the nearest higher power of two. 

.. rubric:: ⚙ Parameters

- `number`: The number to be rounded.

.. rubric:: ↩ Returns

- `Return Type:` `int`
- `Description:` The nearest higher power of two to the given number.

.. _carm_eq:

1.3) carm_eq(ai, bw, fp)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Calculates the minimum of the product of arithmetic intensity (ai) and bandwidth (bw), and floating-point performance (fp).

.. rubric:: ⚙ Parameters

- `ai`: Arithmetic Intensity.
- `bw`: Bandwidth.
- `fp`: Floating Point performance.

.. rubric:: ↩ Returns

- **Return Type:** `float`
- **Description:** The calculated value based on the provided parameters.

.. _upload_to_grafana:

1.4) upload_to_grafana(json, server, api_key, verify)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Uploads a JSON-formatted dashboard to a Grafana server using the provided API key.

.. rubric:: ⚙ Parameters

- `json`: Dashboard in JSON format.
- `server`: Grafana server name.
- `api_key`: API key with read and write privileges.
- `verify`: Boolean to determine SSL verification.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** Post request response from the Grafana server.

.. _get_dashboard_json:

1.5) get_dashboard_json(dashboard, overwrite, message)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates JSON from a Grafana dashboard object for uploading.

.. rubric:: ⚙ Parameters

- `dashboard`: The Grafana dashboard object.
- `overwrite`: Boolean to indicate if the dashboard should be overwritten.
- `message`: Message to accompany the dashboard update.

.. rubric:: ↩ Returns

- **Return Type:** `string`
- **Description:** JSON string of the Grafana dashboard.

.. _template_dict:

1.6) template_dict()
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Creates a template dictionary with default settings for a Grafana dashboard.

.. rubric:: ⚙ Parameters

None.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary template for a Grafana dashboard with default settings.

.. _return_line:

1.7) return_line(ai, eq, name, color, dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Constructs a dictionary representing a line plot for Plotly.

.. rubric:: ⚙ Parameters

- `ai`: X-axis values for the plot.
- `eq`: Y-axis values for the plot.
- `name`: Name of the plot line.
- `color`: Color code for the line.
- `dash`: Type of line dash pattern.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary for a line plot compatible with Plotly.

.. _line_spec:

1.8) line_spec(color, dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates a specification for the style of a line in a Plotly graph.

.. rubric:: ⚙ Parameters

- `color`: The color of the line.
- `dash`: The dash style of the line.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary specifying the line's style.

.. _two_templates_one:

1.9) two_templates_one(data, layout)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Creates a Grafana panel with specific data and layout settings for displaying a Plotly graph.

.. rubric:: ⚙ Parameters

- `data`: Data to be displayed in the panel.
- `layout`: Layout configuration for the panel.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A Grafana panel template with data and layout.

.. _all_these_lines:

1.10) all_these_lines(datalines, data, ai, thread, color)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates multiple lines/traces for plotting based on performance data.

.. rubric:: ⚙ Parameters

- `datalines`: Existing lines or traces.
- `data`: Performance data.
- `ai`: Arithmetic Intensity values.
- `thread`: Thread count information.
- `color`: Color for the line.

.. rubric:: ↩ Returns

- **Return Type:** `list`
- **Description:** A list of lines/traces augmented with new data.

.. _return_traces:

1.11) return_traces(data, ai, thread)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates traces for plotting based on provided data, arithmetic intensity, and thread information.

.. rubric:: ⚙ Parameters

- `data`: The benchmark data.
- `ai`: Arithmetic Intensity.
- `thread`: Thread count information.

.. rubric:: ↩ Returns

- **Return Type:** `list`
- **Description:** A list of traces for visualization.

.. _return_subtraces:

1.12) return_subtraces(data, ai, thread, index)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates subtraces for a specific thread and index, based on performance data and arithmetic intensity.

.. rubric:: ⚙ Parameters

- `data`: The benchmark data.
- `ai`: Arithmetic Intensity.
- `thread`: Thread count.
- `index`: Specific index for the subtrace.

.. rubric:: ↩ Returns

- **Return Type:** `list`
- **Description:** A list of subtraces for detailed visualization.

.. _thread_group:

1.13) thread_group(fig, thread, color, data, ai, ai_list)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Adds multiple traces to a Plotly figure for a specific thread count.

.. rubric:: ⚙ Parameters

- `fig`: The Plotly figure object.
- `thread`: Thread count.
- `color`: Color code

.. _thread_groups:

1.14) thread_groups(fig, thread, color, data, ai, ai_list)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Adds multiple grouped traces to a Plotly figure for different thread counts.

.. rubric:: ⚙ Parameters

- `fig`: The Plotly figure object.
- `thread`: Thread count.
- `color`: Color code for the plot.
- `data`: Benchmark data.
- `ai`: Arithmetic Intensity.
- `ai_list`: List of AI values.

.. rubric:: ↩ Returns

- **Return Type:** `object`
- **Description:** The updated Plotly figure with grouped traces.


.. _grafana_layout:

1.15) grafana_layout(fig)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Adjusts the layout of a Plotly figure to fit well within a Grafana dashboard.

.. rubric:: ⚙ Parameters

- `fig`: The Plotly figure object to be adjusted.

.. rubric:: ↩ Returns

- **Return Type:** `object`
- **Description:** The Plotly figure object with an adjusted layout for Grafana integration.

.. _main:

1.16) main(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Main function orchestrating the creation of a performance analysis dashboard.

.. rubric:: ⚙ Parameters

- `SuperTwin`: Object or data structure representing the context or data for the dashboard.

.. rubric:: ↩ Returns

- **Return Type:** `string` or `dict`
- **Description:** URL or data structure representing the generated Grafana dashboard.

2) monitoring_dashboard_modular.py
++++++++++++++++++++++++++++++++++

This section documents the functions defined in the ``monitoring_dashboard_modular.py`` file.

.. _get_next_id:

2.1) get_next_id()
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates and returns a unique identifier by incrementing a global counter.

.. rubric:: ↩ Returns

- **Return Type:** `int`
- **Description:** The next unique identifier.


.. _get_params:

2.2) get_params(td, measurement)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Retrieves parameters for a specific measurement from a digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.
- `measurement`: The specific measurement to retrieve parameters for.

.. rubric:: ↩ Returns

- **Return Type:** `list`
- **Description:** A list of parameters relevant to the specified measurement.


.. _get_params_interface_known:

2.3) get_params_interface_known(td, interface, measurement)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Fetches parameters for a given measurement from a specified interface in the digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.
- `interface`: The specified interface.
- `measurement`: The specific measurement to retrieve parameters for.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** Parameters for the specified measurement and interface.


.. _get_topology:

2.4) get_topology(td)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Analyzes and returns the system topology from its digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** The topology of the system.


.. _stat_panel:

2.5) stat_panel(SuperTwin, h, w, x, y, color_scheme, metric, empty_dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Adds a statistical panel to a Grafana dashboard.

.. rubric:: ⚙ Parameters

- `SuperTwin`: Digital twin or similar object.
- `h`: Height of the panel.
- `w`: Width of the panel.
- `x`, `y`: Position coordinates of the panel.
- `color_scheme`: Color scheme for the panel.
- `metric`: Specific metric to display.
- `empty_dash`: Dashboard template to modify.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** The updated dashboard template with the new panel.


.. _name_panel:

2.6) name_panel(SuperTwin, empty_dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Adds a panel displaying the name of the digital twin to the dashboard.

.. rubric:: ⚙ Parameters

- `SuperTwin`: Digital twin or similar object.
- `empty_dash`: Dashboard template to modify.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** The updated dashboard template with the new name panel.


.. _comprehend:

2.7) comprehend(topology, wanted, unit)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Filters and returns elements from the system topology based on specified criteria.

.. rubric:: ⚙ Parameters

- `topology`: The system topology.
- `wanted`: List of desired elements.
- `unit`: The unit or type of elements to filter.

.. rubric:: ↩ Returns

- **Return Type:** `list`
- **Description:** Filtered elements from the topology.


.. _freq_clock_panel:

2.8) freq_clock_panel(SuperTwin, h, w, x, y, threads, empty_dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Creates a dashboard panel for displaying frequency clock data for specified threads.

.. rubric:: ⚙ Parameters

- `SuperTwin`: Digital twin or similar object.
- `h`, `w`, `x`, `y`: Panel dimensions and position.
- `threads`: List of thread identifiers.
- `empty_dash`: Dashboard template to modify.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** The updated dashboard template with the new panel.


.. _load_clock_panel:

2.9) load_clock_panel(SuperTwin, h, w, x, y, empty_dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Adds a load clock panel to the dashboard for system load visualization.

.. rubric:: ⚙ Parameters

- `SuperTwin`: Digital twin or similar object.
- `h`, `w`, `x`, `y





3) monitoring_dashboard_saved.py
++++++++++++++++++++++++++++++++

This section documents the functions defined in the ``monitoring_dashboard_saved.py`` file.

.. _get_next_id:

3.1) get_next_id()
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates and returns a unique identifier by incrementing a global counter.

.. rubric:: ↩ Returns

- **Return Type:** `int`
- **Description:** The next unique identifier.


.. _get_params:

3.2) get_params(td, measurement)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Retrieves parameters for a specific measurement from a digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.
- `measurement`: The specific measurement to retrieve parameters for.

.. rubric:: ↩ Returns

- **Return Type:** `list`
- **Description:** A list of parameters relevant to the specified measurement.


.. _get_params_interface_known:

3.3) get_params_interface_known(td, interface, measurement)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Fetches parameters for a given measurement from a specified interface in the digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.
- `interface`: The specified interface.
- `measurement`: The specific measurement to retrieve parameters for.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** Parameters for the specified measurement and interface.


.. _get_topology:

3.4) get_topology(td)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Analyzes and returns the system topology from its digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** The topology of the system.


.. _generate_monitoring_dashboard:

3.5) generate_monitoring_dashboard(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Orchestrates the creation of a monitoring dashboard for a given digital twin.

.. rubric:: ⚙ Parameters

- `SuperTwin`: The digital twin or similar object for which the dashboard is being created.

.. rubric:: ↩ Returns

- **Return Type:** `string`
- **Description:** The URL of the generated Grafana dashboard.



4) monitoring_dashboard.py
++++++++++++++++++++++++++

This section documents the functions defined in the ``monitoring_dashboard.py`` file.

.. _get_next_id:

4.1) get_next_id()
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Increments and returns the next unique identifier from a global counter.

.. rubric:: ↩ Returns

- **Return Type:** `int`
- **Description:** The next unique identifier in the sequence.


.. _get_params:

4.2) get_params(td, measurement)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Retrieves parameter information for a specified measurement from a digital twin description.

.. rubric:: ⚙ Parameters

- `td`: The digital twin description.
- `measurement`: The specific measurement for which parameters are required.

.. rubric:: ↩ Returns

- **Return Type:** `list` of `dict`
- **Description:** A list of dictionaries containing the alias and parameter names for the specified measurement.


.. _get_params_interface_known:

4.3) get_params_interface_known(td, interface, measurement)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Fetches parameter information for a specified measurement from a known interface within a digital twin description.

.. rubric:: ⚙ Parameters

- `td`: The digital twin description.
- `interface`: The specific interface to be queried.
- `measurement`: The measurement for which parameters are needed.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary containing the alias and parameter name for the specified measurement and interface.


.. _get_topology:

4.4) get_topology(td)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Analyzes a digital twin description to determine the system topology, specifically mapping sockets to their corresponding cores and threads.

.. rubric:: ⚙ Parameters

- `td`: The digital twin description.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary representing the system topology.


.. _generate_monitoring_dashboard:

4.5) generate_monitoring_dashboard(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

Generates a Grafana monitoring dashboard for the given digital twin, configuring panels and metrics based on the twin's description.

.. rubric:: ⚙ Parameters

- `SuperTwin`: The digital twin object for which the monitoring dashboard is being created.

.. rubric:: ↩ Returns

- **Return Type:** `string`
- **Description:** The URL of the newly generated Grafana dashboard.


5) monitoring_panels.py
+++++++++++++++++++++++

.. _stat_panel:

5.1) stat_panel(datasource, _id, h, w, x, y, color_scheme, title)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a configuration for a Grafana statistic panel.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `h`: Height of the panel.
  - `w`: Width of the panel.
  - `x`: X position of the panel.
  - `y`: Y position of the panel.
  - `color_scheme`: Color scheme for the panel.
  - `title`: Title of the panel.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a Grafana statistic panel.

.. _stat_query:

5.2) stat_query(datasource, alias, measurement, param)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a query configuration for a Grafana statistic panel.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `alias`: Alias for the query.
  - `measurement`: The measurement to query.
  - `param`: The parameter to query.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the query configuration for a Grafana statistic panel.

.. _name_panel_html:

5.3) name_panel_html(datasource, _id, hostname)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a HTML panel for displaying a hostname in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `hostname`: The hostname to display.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a text panel in Grafana.

.. _name_panel:

5.4) name_panel(datasource, _id, hostname)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a statistic panel for displaying a hostname in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `hostname`: The hostname to display.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a statistic panel in Grafana.

.. _clock_panel:

5.5) clock_panel(datasource, _id, h, w, x, y, color_scheme, title)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a heatmap panel for displaying time-based data in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `h`: Height of the panel.
  - `w`: Width of the panel.
  - `x`: X position of the panel.
  - `y`: Y position of the panel.
  - `color_scheme`: Color scheme for the panel.
  - `title`: Title of the panel.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a heatmap panel in Grafana.

.. _clock_query:

5.6) clock_query(datasource, alias, measurement, param)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a query for a heatmap panel in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `alias`: Alias for the query.
  - `measurement`: The measurement to query.
  - `param`: The parameter to query.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the query for a heatmap panel in Grafana.

.. _small_single_timeseries:

.. _small_single_timeseries:

5.7) small_single_timeseries(datasource, _id, h, w, x, y, title)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a small single timeseries panel for Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `h`: Height of the panel.
  - `w`: Width of the panel.
  - `x`: X position of the panel.
  - `y`: Y position of the panel.
  - `title`: Title of the panel.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a timeseries panel in Grafana.

.. _small_single_query:

5.8) small_single_query(datasource, alias, measurement)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a query for a small single timeseries panel in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `alias`: Alias for the query.
  - `measurement`: The measurement to query.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the query for a small single timeseries panel in Grafana.

.. _all_network_panel:

5.9) all_network_panel(datasource, _id, h, w, x, y)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a network panel for displaying network data in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `h`: Height of the panel.
  - `w`: Width of the panel.
  - `x`: X position of the panel.
  - `y`: Y position of the panel.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a network panel in Grafana.

.. _disk_panel:

5.10) disk_panel(datasource, _id, h, w, x, y, title)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a disk panel for displaying disk data in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `h`: Height of the panel.
  - `w`: Width of the panel.
  - `x`: X position of the panel.
  - `y`: Y position of the panel.
  - `title`: Title of the panel.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a disk panel in Grafana.

.. _general_panel:

5.11) general_panel(datasource, _id, h, w, x, y, title)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a general panel for displaying various types of data in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `h`: Height of the panel.
  - `w`: Width of the panel.
  - `x`: X position of the panel.
  - `y`: Y position of the panel.
  - `title`: Title of the panel.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a general panel in Grafana.

.. _name_panel_last:

5.12) name_panel_last(datasource, _id, hostname)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a name panel for displaying a hostname as the last panel in Grafana.

.. rubric:: ⚙ Parameters

  - `datasource`: The Grafana datasource.
  - `_id`: Unique identifier for the panel.
  - `hostname`: The hostname to display.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary representing the configuration for a name panel in Grafana.

6) observation_standard.py
++++++++++++++++++++++++++


.. _next_y:

6.1) next_y()
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Calculates the next y-coordinate for a Grafana panel.

.. rubric:: ↩ Returns

  - **Return Type:** `int`
  - **Description:** The next y-coordinate value.

.. _current_y:

6.2) current_y()
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Retrieves the current y-coordinate for a Grafana panel.

.. rubric:: ↩ Returns

  - **Return Type:** `int`
  - **Description:** The current y-coordinate value.

.. _upload_to_grafana:

6.3) upload_to_grafana(json, server, api_key, verify=True)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Uploads a Grafana dashboard configuration to a Grafana server.

.. rubric:: ⚙ Parameters

  - `json`: Dashboard configuration in JSON format.
  - `server`: The URL of the Grafana server.
  - `api_key`: API key for authentication.
  - `verify`: Flag to verify the server's SSL certificate.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** Response from the Grafana server.

.. _get_dashboard_json:

6.4) get_dashboard_json(dashboard, overwrite, message="Updated by grafanalib")
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Generates a JSON representation of a Grafana dashboard.

.. rubric:: ⚙ Parameters

  - `dashboard`: The Grafana dashboard object.
  - `overwrite`: Flag indicating whether to overwrite an existing dashboard.
  - `message`: A message to include with the dashboard configuration.

.. rubric:: ↩ Returns

  - **Return Type:** `str`
  - **Description:** JSON string of the dashboard configuration.

.. _template_dict:

6.5) template_dict(observation_id)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Creates a template dictionary for a Grafana dashboard.

.. rubric:: ⚙ Parameters

  - `observation_id`: Identifier for the observation.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A template dictionary for a Grafana dashboard.

.. _find_my_socket:

6.6) find_my_socket(socket_threads, thread)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Finds the socket associated with a given thread.

.. rubric:: ⚙ Parameters

  - `socket_threads`: A dictionary of sockets and their threads.
  - `thread`: The thread to find the socket for.

.. rubric:: ↩ Returns

  - **Return Type:** `str`
  - **Description:** The socket associated with the specified thread.

.. _find_from_likwid_pin:

6.7) find_from_likwid_pin(SuperTwin, affinity)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Resolves thread affinity from LIKWID pinning.

.. rubric:: ⚙ Parameters

  - `SuperTwin`: The SuperTwin object.
  - `affinity`: The affinity string from LIKWID.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary of sockets and their threads based on LIKWID pinning.

.. _find_from_likwid_pin_old:

6.8) find_from_likwid_pin_old(affinity)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Resolves thread affinity from an older LIKWID pinning format.

.. rubric:: ⚙ Parameters

  - `affinity`: The affinity string from LIKWID.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary of sockets and their threads based on the older LIKWID pinning format.

.. _involved_resolve:

6.9) involved_resolve(threads)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Resolves involved threads into a structured format.

.. rubric:: ⚙ Parameters

  - `threads`: A list of involved threads.

.. rubric:: ↩ Returns

  - **Return Type:** `dict`
  - **Description:** A dictionary of sockets and their threads.

.. _get_field_and_metric:

6.10) get_field_and_metric(SuperTwin, involved, pmu_metric)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Retrieves field and metric information based on PMU metrics.

.. rubric:: ⚙ Parameters

  - `SuperTwin`: The SuperTwin object.
  - `involved`: A dictionary of involved sockets and threads.
  - `pmu_metric`: The PMU metric to retrieve information for.

.. rubric:: ↩ Returns

  - **Return Type:** `tuple`
  - **Description:** A tuple containing the field and metric name.

.. _main:

6.11) main(SuperTwin, observation)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Main function to generate a Grafana dashboard for a given observation.

.. rubric:: ⚙ Parameters

  - `SuperTwin`: The SuperTwin object.
  - `observation`: The observation data.

.. rubric:: ↩ Returns

  - **Return Type:** `str`
  - **Description:** The URL of the generated Grafana dashboard.

.. _multinode:

6.12) multinode(st1, o1, st2, o2, st3, o3, st4, o4)
^^^^^^^^^^^^^^^^^^^^^^^^^

.. rubric:: ➤ Functionality

  Generates a Grafana dashboard for multi-node observations.

.. rubric:: ⚙ Parameters

  - `st1`, `st2`, `st3`, `st4`: SuperTwin objects for each node.
  - `o1`, `o2`, `o3`, `o4`: Observation data for each node.

.. rubric:: ↩ Returns

  - **Return Type:** `str`
  - **Description:** The URL of the generated multi-node Grafana dashboard.


7) panels_multinode.py
++++++++++++++++++++++

This section documents the functions defined in the ``panels_multinode.py`` file.

.. _ret_ts_panel:

7.1) ret_ts_panel(y, title)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function returns a time series panel configuration for Grafana.

- **Parameters**:

    - **y** (*int*): The y-coordinate for the panel's position.
    - **title** (*str*): The title of the panel.

- **Returns**:

    - A dictionary representing the time series panel configuration.


.. _ret_query:

7.2) ret_query(alias, measurement, field, tag, datasource)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function generates a query configuration for Grafana panels.

- **Parameters**:

    - **alias** (*str*): The alias for the query.
    - **measurement** (*str*): The measurement to be queried.
    - **field** (*str*): The field to be selected in the query.
    - **tag** (*str*): The tag to filter the query.
    - **datasource** (*str*): The UID of the datasource.

- **Returns**:

    - A dictionary representing the query configuration.


.. _ret_gauge_panel:

7.3) ret_gauge_panel(title, y)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function returns a gauge panel configuration for Grafana.

- **Parameters**:

    - **title** (*str*): The title of the gauge panel.
    - **y** (*int*): The y-coordinate for the panel's position.

- **Returns**:

    - A dictionary representing the gauge panel configuration.

8) panels_standard.py
++++++++++++++++++++++

This section documents the functions defined in the ``panels_standard.py`` file.

.. _ret_ts_panel:

8.1) ret_ts_panel(datasource, y, title)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function returns a time series panel configuration for Grafana.

- **Parameters**:

    - **datasource** (*str*): The datasource UID for the panel.
    - **y** (*int*): The y-coordinate for the panel's position.
    - **title** (*str*): The title of the panel.

- **Returns**:

    - A dictionary representing the time series panel configuration.


.. _ret_query:

8.2) ret_query(alias, measurement, field, tag)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function generates a query configuration for Grafana panels.

- **Parameters**:

    - **alias** (*str*): The alias for the query.
    - **measurement** (*str*): The measurement to be queried.
    - **field** (*str*): The field to be selected in the query.
    - **tag** (*str*): The tag to filter the query.

- **Returns**:

    - A dictionary representing the query configuration.


.. _ret_gauge_panel:

8.3) ret_gauge_panel(datasource, title, y)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function returns a gauge panel configuration for Grafana.

- **Parameters**:

    - **datasource** (*str*): The datasource UID for the panel.
    - **title** (*str*): The title of the gauge panel.
    - **y** (*int*): The y-coordinate for the panel's position.

- **Returns**:

    - A dictionary representing the gauge panel configuration.


.. _grafana_layout_2:

8.4) grafana_layout_2(fig)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function updates the layout configuration for a Plotly figure to match a specific Grafana style.

- **Parameters**:

    - **fig** (*plotly.graph_objs.Figure*): The figure to update the layout for.

- **Returns**:

    - The updated Plotly figure with the new layout configuration.


.. _two_templates_two:

8.5) two_templates_two(data, layout)
^^^^^^^^^^^^^^^^^^^^^^^^^

This function creates a Grafana panel template for displaying Plotly figures.

- **Parameters**:

    - **data** (*list*): The data for the Plotly figure.
    - **layout** (*dict*): The layout configuration for the Plotly figure.

- **Returns**:

    - A dictionary representing the Grafana panel template.

9) roofline_dashboard_back.py
+++++++++++++++++++++++++++++

.. _next_panel_id:

9.1) next_panel_id
^^^^^^^^^^^^^^^^^^^^^^^^^

Increments and returns the global variable `glob_panel_id`, used for tracking Grafana panel IDs.

- **Returns**:

    - Integer: The next panel ID in the sequence.

.. _get_json_static_panel:

9.2) get_json_static_panel(h, w, x, y, title, emp, target)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a JSON structure for a static panel in Grafana.

- **Parameters**:

    - **h** (*int*): Panel height.
    - **w** (*int*): Panel width.
    - **x** (*int*): X-coordinate in the dashboard grid.
    - **y** (*int*): Y-coordinate in the dashboard grid.
    - **title** (*str*): Panel title.
    - **emp** (*str*): Color mode ("value" or "background").
    - **target** (*str*): Target data field.

- **Returns**:

    - Dictionary: JSON object for the static panel.

.. _get_stream_bw:

9.3) get_stream_bw(twin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Calculates the maximum bandwidth from STREAM benchmark results.

- **Parameters**:

    - **twin** (*dict*): Data structure containing twin information.

- **Returns**:

    - Float: Maximum bandwidth in GB/s.

.. _peak_theoretical_flop:

9.4) peak_theoretical_flop(no_procs, core_per_proc, clock_speed, no_fma_units, max_vector_size)
^^^^^^^^^^^^^^^^^^^^^^^^^

Calculates the peak theoretical floating-point operations per second.

- **Parameters**:

    - **no_procs** (*int*): Number of processors.
    - **core_per_proc** (*int*): Cores per processor.
    - **clock_speed** (*float*): Processor clock speed in GHz.
    - **no_fma_units** (*int*): Number of FMA units.
    - **max_vector_size** (*int*): Maximum vector size.

- **Returns**:

    - Float: Peak GFLOP/s.

.. _get_ridge_point:

9.5) get_ridge_point(bw, flop)
^^^^^^^^^^^^^^^^^^^^^^^^^

Calculates the ridge point of a roofline model.

- **Parameters**:

    - **bw** (*float*): Bandwidth.
    - **flop** (*float*): Floating-point operations per second.

- **Returns**:

    - Float: Ridge point value.

.. _get_roof_values:

9.6) get_roof_values(max_bw, peak_g_flop, ridge_point)
^^^^^^^^^^^^^^^^^^^^^^^^^

Determines roofline model values.

- **Parameters**:

    - **max_bw** (*float*): Maximum bandwidth.
    - **peak_g_flop** (*float*): Peak GFLOP/s.
    - **ridge_point** (*float*): Ridge point.

- **Returns**:

    - Tuple: Lists of Arithmetic Intensities (AIs) and corresponding performance values (Y).

.. _get_flops_values:

9.7) get_flops_values(twin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Extracts FLOPS values from a given twin data structure.

- **Parameters**:

    - **twin** (*dict*): Twin data structure.

- **Returns**:

    - Tuple: FLOPS values for different operations.

.. _get_dram_roofline_panel:

9.8) get_dram_roofline_panel(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a DRAM roofline panel for a Grafana dashboard.

- **Parameters**:

    - **SuperTwin**: Object containing twin and system information.

- **Returns**:

    - Dictionary: Grafana panel configuration for the DRAM roofline.

.. _get_stream_results:

9.9) get_stream_results(twin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Extracts STREAM benchmark results from the twin data.

- **Parameters**:

    - **twin** (*dict*): Twin data structure.

- **Returns**:

    - Tuple: Results of the STREAM benchmark and the list of thread counts.

.. _get_stream_scaling_panel:

9.10) get_stream_scaling_panel(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates a Grafana panel for STREAM benchmark multicore scaling.

- **Parameters**:

    - **SuperTwin**: Object containing twin and system information.

- **Returns**:

    - Dictionary: Grafana panel configuration for STREAM scaling.

.. _get_hpcg_results:

9.11) get_hpcg_results(twin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Extracts HPCG benchmark results from the twin data.

- **Parameters**:

    - **twin** (*dict*): Twin data structure.

- **Returns**:

    - Tuple: Results of the HPCG benchmark and the list of thread counts.

.. _get_hpcg_scaling_panel:

9.12) get_hpcg_scaling_panel(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a Grafana panel for HPCG benchmark multicore scaling.

- **Parameters**:

    - **SuperTwin**: Object containing twin and system information.

- **Returns**:

    - Dictionary: Grafana panel configuration for HPCG scaling.

.. _generate_roofline_dashboard:

9.13) generate_roofline_dashboard(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates a complete Grafana dashboard for roofline analysis.

- **Parameters**:

    - **SuperTwin**: Object containing twin and system information.

- **Returns**:

    - String: URL of the generated Grafana dashboard.

10) roofline_dashboard_panels.py
++++++++++++++++++++++++++++++++

.. _two_templates_one:

10.1) two_templates_one(data, layout, datasource)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a Grafana panel template for displaying a Plotly figure related to the Cache Aware Roofline Model.

- **Parameters**:

    - **data** (*list*): The data for the Plotly figure.
    - **layout** (*dict*): The layout configuration for the Plotly figure.
    - **datasource** (*str*): The UID for the Grafana datasource.

- **Returns**:

    - Dictionary: JSON object for the Grafana panel.

.. _two_templates_two:

10.2) two_templates_two(data, layout, datasource)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a Grafana panel template for displaying system hardware information using a Plotly figure.

- **Parameters**:

    - **data** (*list*): The data for the Plotly figure.
    - **layout** (*dict*): The layout configuration for the Plotly figure.
    - **datasource** (*str*): The UID for the Grafana datasource.

- **Returns**:

    - Dictionary: JSON object for the Grafana panel.

.. _two_templates_three:

10.3) two_templates_three(data, layout, h, w, x, y, datasource, title, id)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a customizable Grafana panel template for displaying Plotly figures.

- **Parameters**:

    - **data** (*list*): The data for the Plotly figure.
    - **layout** (*dict*): The layout configuration for the Plotly figure.
    - **h** (*int*): Height of the panel.
    - **w** (*int*): Width of the panel.
    - **x** (*int*): X-coordinate in the dashboard grid.
    - **y** (*int*): Y-coordinate in the dashboard grid.
    - **datasource** (*str*): The UID for the Grafana datasource.
    - **title** (*str*): Title of the panel.
    - **id** (*int*): Panel ID.

- **Returns**:

    - Dictionary: JSON object for the Grafana panel.

.. _grafana_layout:

10.4) grafana_layout(fig)
^^^^^^^^^^^^^^^^^^^^^^^^^

Updates the layout configuration of a Plotly figure for a Grafana dashboard with specific aesthetic preferences.

- **Parameters**:

    - **fig** (*plotly.graph_objs.Figure*): The figure to update the layout for.

- **Returns**:

    - The updated Plotly figure with the new layout configuration.

.. _grafana_layout_2:

10.5) grafana_layout_2(fig)
^^^^^^^^^^^^^^^^^^^^^^^^^

Updates the layout configuration of a Plotly figure for a Grafana dashboard, tailored for a specific visual style.

- **Parameters**:

    - **fig** (*plotly.graph_objs.Figure*): The figure to update the layout for.

- **Returns**:

    - The updated Plotly figure with the new layout configuration.

.. _grafana_layout_3:

10.6) grafana_layout_3(fig, xtickvals, ytitle)
^^^^^^^^^^^^^^^^^^^^^^^^^

Customizes the layout of a Plotly figure for a Grafana dashboard with specific axis configurations.

- **Parameters**:

    - **fig** (*plotly.graph_objs.Figure*): The figure to update the layout for.
    - **xtickvals** (*list*): Values for the x-axis ticks.
    - **ytitle** (*str*): Title for the y-axis.

- **Returns**:

    - The updated Plotly figure with the new layout configuration.

11) roofline_dashboard.py
+++++++++++++++++++++++++

.. _generate_roofline_dashboard:

11.1) generate_roofline_dashboard(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates a complete Grafana dashboard for a given SuperTwin instance with roofline and benchmark panels.

- **Parameters**:

    - **SuperTwin**: The SuperTwin instance containing configuration and data sources.

- **Returns**:

    - The URL of the generated Grafana dashboard.

.. _generate_visibility_sequence:

11.2) generate_visibility_sequence(vis_dict)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a visibility sequence for Grafana panels based on a given visibility dictionary.

- **Parameters**:

    - **vis_dict** (*dict*): A dictionary specifying visibility for each panel.

- **Returns**:

    - List: A list representing visibility for each panel.

.. _generate_visibility_sequence_from_list:

11.3) generate_visibility_sequence_from_list(vis_list)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates a visibility sequence for Grafana panels from a given list of visibilities.

- **Parameters**:

    - **vis_list** (*list*): A list representing visibility for each panel.

- **Returns**:

    - List: A list representing visibility for each panel.

.. _get_next_color:

11.4) get_next_color()
^^^^^^^^^^^^^^^^^^^^^^^^^

Fetches the next color in the predefined color sequence for panel visualization.

- **Returns**:

    - String: The next color in the sequence.

.. _round_power_of_2:

11.5) round_power_of_2(number)
^^^^^^^^^^^^^^^^^^^^^^^^^

Rounds a given number to the nearest power of two.

- **Parameters**:

    - **number** (*int*): The number to round.

- **Returns**:

    - Int: The nearest power of two to the given number.

.. _carm_eq:

11.6) carm_eq(ai, bw, fp)
^^^^^^^^^^^^^^^^^^^^^^^^^

Calculates the minimum of AI times bandwidth and FP for the CARM benchmark.

- **Parameters**:

    - **ai** (*float*): Arithmetic intensity.
    - **bw** (*float*): Bandwidth.
    - **fp** (*float*): Floating point operations per second.

- **Returns**:

    - Float: The calculated minimum value for CARM.

.. _next_y:

11.7) next_y()
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates the next y-coordinate for placing panels in the Grafana dashboard.

- **Returns**:

    - Int: The next y-coordinate for a panel.

.. _next_panel_id:

11.8) next_panel_id()
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates the next unique panel ID for Grafana dashboard panels.

- **Returns**:

    - Int: The next unique panel ID.

.. _next_dash_id:

11.9) next_dash_id()
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates the next unique dashboard ID for Grafana dashboards.

- **Returns**:

    - Int: The next unique dashboard ID.

.. _return_line:

11.10) return_line(ai, eq, name, color, dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

Creates a line configuration for Plotly figures in Grafana panels.

- **Parameters**:

    - **ai** (*list*): List of arithmetic intensities.
    - **eq** (*list*): List of corresponding values.
    - **name** (*str*): Name of the line.
    - **color** (*str*): Color of the line.
    - **dash** (*str*): Dash style of the line.

- **Returns**:

    - Dict: A dictionary representing the line configuration.

.. _line_spec:

11.11) line_spec(color, dash)
^^^^^^^^^^^^^^^^^^^^^^^^^

Specifies the style of a line for Plotly figures in Grafana panels.

- **Parameters**:

    - **color** (*str*): Color of the line.
    - **dash** (*str*): Dash style of the line.

- **Returns**:

    - Dict: A dictionary representing the line style.

.. _return_subtraces:

11.12) return_subtraces(data, ai, thread, index)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates sub-traces for Plotly figures in Grafana panels.

- **Parameters**:

    - **data** (*dict*): Data used for generating the sub-traces.
    - **ai** (*list*): Arithmetic intensities.
    - **thread** (*str*): Thread count.
    - **index** (*int*): Index for data selection.

- **Returns**:

    - List: A list containing sub-trace data and configurations.

.. _thread_groups:

11.13) thread_groups(fig, thread, color, data, ai, ai_list)
^^^^^^^^^^^^^^^^^^^^^^^^^

Groups threads for Plotly figures in Grafana panels based on the given configuration.

- **Parameters**:

    - **fig** (*plotly.graph_objs.Figure*): The figure to update.
    - **thread** (*str*): Thread count.
    - **color** (*str*): Color for the group.
    - **data** (*dict*): Data used for the grouping.
    - **ai** (*list*): Arithmetic intensities.
    - **ai_list** (*list*): List of arithmetic intensities.

- **Returns**:

    - The updated Plotly figure with grouped threads.

.. _fill_carm_res_dict:

11.14) fill_carm_res_dict(carm_res, result)
^^^^^^^^^^^^^^^^^^^^^^^^^

Fills the CARM results dictionary with data from benchmark results.

- **Parameters**:

    - **carm_res** (*dict*): Dictionary to fill with CARM results.
    - **result** (*dict*): Benchmark result data.

- **Returns**:

    - Dict: The updated CARM results dictionary.

.. _get_carm_res_from_dt:

11.15) get_carm_res_from_dt(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Retrieves CARM results from a given SuperTwin instance.

- **Parameters**:

    - **SuperTwin**: The SuperTwin instance containing benchmark data.

- **Returns**:

    - Dict: A dictionary of CARM results.

.. _get_hpcg_marks:

11.16) get_hpcg_marks(hpcg_res)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates HPCG benchmark marks from given results.

- **Parameters**:

    - **hpcg_res** (*dict*): HPCG benchmark results.

- **Returns**:

    - Dict: A dictionary of HPCG benchmark marks.

.. _generate_carm_roofline:

11.17) generate_carm_roofline(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates a CARM roofline Plotly figure for a given SuperTwin instance.

- **Parameters**:

    - **SuperTwin**: The SuperTwin instance containing configuration and data sources.

- **Returns**:

    - plotly.graph_objs.Figure: The generated CARM roofline figure.

.. _get_indicator_fields:

11.18) get_indicator_fields(_string)
^^^^^^^^^^^^^^^^^^^^^^^^^

Extracts value, prefix, and suffix from a given string.

- **Parameters**:

    - **_string** (*str*): The string to parse.

- **Returns**:

    - Tuple: A tuple containing the extracted value, prefix, and suffix.

.. _get_indicator_fields_vector:

11.19) get_indicator_fields_vector(_array)
^^^^^^^^^^^^^^^^^^^^^^^^^

Extracts value, prefix, and suffix from a given array of strings.

- **Parameters**:

    - **_array** (*list*): The array of strings to parse.

- **Returns**:

    - Tuple: A tuple containing the extracted value, prefix, and suffix.

.. _generate_info_panel:

11.20) generate_info_panel(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates an information panel as a Plotly figure for a given SuperTwin instance.

- **Parameters**:

    - **SuperTwin**: The SuperTwin instance containing configuration and data sources.

- **Returns**:

    - plotly.graph_objs.Figure: The generated information panel figure.

.. _get_stream_bench_data:

11.21) get_stream_bench_data(td)
^^^^^^^^^^^^^^^^^^^^^^^^^

Retrieves STREAM benchmark data from twin description.

- **Parameters**:

    - **td** (*dict*): Twin description containing benchmark data.

- **Returns**:

    - Dict: A dictionary of STREAM benchmark results.

.. _generate_x:

11.22) generate_x(stream_res)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates x-axis data for a STREAM benchmark graph.

- **Parameters**:

    - **stream_res** (*dict*): STREAM benchmark results.

- **Returns**:

    - List: A list of x-axis data points.

.. _generate_y:

11.23) generate_y(stream_res_key)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates y-axis data for a STREAM benchmark graph based on a specific key.

- **Parameters**:

    - **stream_res_key** (*list*): Specific key in the STREAM benchmark results.

- **Returns**:

    - List: A list of y-axis data points.

.. _generate_stream_panel:

11.24) generate_stream_panel(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates a STREAM benchmark panel as a Plotly figure for a given SuperTwin instance.

- **Parameters**:

    - **SuperTwin**: The SuperTwin instance containing configuration and data sources.

- **Returns**:

    - plotly.graph_objs.Figure: The generated STREAM benchmark panel figure.

.. _get_hpcg_bench_data:

11.25) get_hpcg_bench_data(td)
^^^^^^^^^^^^^^^^^^^^^^^^^

Retrieves HPCG benchmark data from twin description.

- **Parameters**:

    - **td** (*dict*): Twin description containing benchmark data.

- **Returns**:

    - Dict: A dictionary of HPCG benchmark results.

.. _generate_hpcg_panel:

11.26) generate_hpcg_panel(SuperTwin)
^^^^^^^^^^^^^^^^^^^^^^^^^

Generates an HPCG benchmark panel as a Plotly figure for a given SuperTwin instance.

- **Parameters**:

    - **SuperTwin**: The SuperTwin instance containing configuration and data sources.

- **Returns**:

    - plotly.graph_objs.Figure: The generated HPCG benchmark panel figure.

.. _get_thread_set:

12) roofline_dashboard_old.py
+++++++++++++++++++++++++++++

This module contains utility functions for managing and processing data for Grafana dashboards.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: next_panel_id()

    Increments and returns a global panel ID.

.. function:: get_json_static_panel(h, w, x, y, title, emp, target)

    Generates a JSON representation of a static panel for Grafana dashboards.

    :param h: Height of the panel.
    :param w: Width of the panel.
    :param x: X-axis position of the panel.
    :param y: Y-axis position of the panel.
    :param title: Title of the panel.
    :param emp: Display mode of the panel (value or background).
    :param target: Data target for the panel.
    :return: A dictionary representing the JSON configuration of the panel.

.. function:: get_stream_bw(twin)

    Retrieves the maximum bandwidth from STREAM benchmark results.

    :param twin: The twin data containing benchmark results.
    :return: Maximum bandwidth in GB/s.

.. function:: peak_theoretical_flop(no_procs, core_per_proc, clock_speed, no_fma_units, max_vector_size)

    Calculates the peak theoretical floating-point operations per second.

    :param no_procs: Number of processors.
    :param core_per_proc: Number of cores per processor.
    :param clock_speed: Clock speed in GHz.
    :param no_fma_units: Number of FMA units.
    :param max_vector_size: Maximum vector size.
    :return: Peak theoretical GFLOP/s.

.. function:: get_ridge_point(bw, flop)

    Determines the ridge point in the roofline model.

    :param bw: Bandwidth in GB/s.
    :param flop: Floating-point operations per second in GFLOP/s.
    :return: Ridge point value.

.. function:: get_roof_values(max_bw, peak_g_flop, ridge_point)

    Computes the roof values for the roofline model.

    :param max_bw: Maximum bandwidth in GB/s.
    :param peak_g_flop: Peak GFLOP/s.
    :param ridge_point: Ridge point value.
    :return: A tuple of lists containing AI and corresponding performance values.

.. function:: get_flops_values(twin)

    Extracts FLOPS values from HPCG benchmark results.

    :param twin: The twin data containing benchmark results.
    :return: Tuple of FLOPS values for different HPCG operations.

.. function:: get_dram_roofline_panel(SuperTwin)

    Generates the DRAM roofline panel configuration.

    :param SuperTwin: The twin object with relevant data.
    :return: Dictionary representing the DRAM roofline panel configuration.

.. function:: get_stream_results(twin)

    Retrieves STREAM benchmark results.

    :param twin: The twin data containing benchmark results.
    :return: A tuple containing results and thread set.

.. function:: get_stream_scaling_panel(SuperTwin)

    Generates the STREAM scaling panel configuration.

    :param SuperTwin: The twin object with relevant data.
    :return: Dictionary representing the STREAM scaling panel configuration.

.. function:: get_hpcg_results(twin)

    Retrieves HPCG benchmark results.

    :param twin: The twin data containing benchmark results.
    :return: A tuple containing results and thread set.

.. function:: get_hpcg_scaling_panel(SuperTwin)

    Generates the HPCG scaling panel configuration.

    :param SuperTwin: The twin object with relevant data.
    :return: Dictionary representing the HPCG scaling panel configuration.

.. function:: generate_roofline_dashboard(SuperTwin)

    Creates a complete roofline dashboard based on the provided twin object.

    :param SuperTwin: The twin object with relevant data.
    :return: URL of the generated Grafana dashboard.



13) Flask Web Server with MongoDB Integration
+++++++++++++++++++++++++++++++++++++++++++++

This script creates a Flask-based web server with MongoDB integration. It handles HTTP requests and interacts with a MongoDB database to fetch and display data.

1. **Module Imports**:
   - `sys`: Used for Python runtime environment manipulations.
   - `utils`: Custom module, presumably for utility functions.
   - `Flask`: Main class for creating a Flask web application.
   - `request`, `jsonify`, `json`, `abort`: Flask modules for handling HTTP requests and responses.
   - `CORS`, `cross_origin`: Flask-CORS modules for handling Cross-Origin Resource Sharing (CORS).
   - `pprint`: Module for pretty-printing Python data structures.
   - `pymongo`, `MongoClient`: Modules for interacting with MongoDB.
   - `ObjectId`, `dumps`, `loads`: Modules from `bson` for handling BSON data.

2. **Flask App Configuration**:
   - `app`: Flask application instance.
   - `CORS(app)`: Enables CORS for the Flask app.
   - `app.config`: Configures CORS headers.

3. **Global Variables**:
   - `dummy_time`: Placeholder time value.
   - `data`: Dictionary to store data.

4. **Flask Routes**:
   - `@app.route('/')`: Root route, returns a simple 'OK' response.
   - `@app.route('/search')`: Search route, returns a JSON list of data.
   - `@app.route('/query')`: Query route, handles data queries and returns JSON-formatted data.

5. **main Function**:
   - Connects to a MongoDB database using the `utils` module.
   - Fills the `data` dictionary with data from MongoDB.
   - Runs the Flask app on the specified host and port.

6. **Execution**:
   - Checks if the script is the main program and calls the `main` function.

.. note:: Replace "dolap" and "10.36.54.195" with the appropriate arguments when calling the `main` function.

14) static_data.py
++++++++++++++++++

This module sets up a Flask server to handle data queries and integrates with a MongoDB database.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- The Flask module from Flask for creating the web server.
- The CORS and cross_origin modules from flask_cors for handling Cross-Origin Resource Sharing (CORS).
- The MongoClient from pymongo for MongoDB interactions.
- The ObjectId, dumps, and loads functions from bson for BSON to JSON conversion.
- The utils module for utility functions.

Flask App Configuration
^^^^^^^^^^^^^^^^^^^^^^^^^

The Flask app is configured with CORS to allow cross-origin requests. The app listens on all interfaces (0.0.0.0) at port 5052.

Endpoints
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: hello_world()

    A basic route that returns 'OK' when accessed. Used for health checks or basic verification.

.. function:: find_metrics()

    Endpoint to find and return available metrics in the data. Responds to both GET and POST requests.

.. function:: query_metrics()

    Endpoint to query specific metrics based on the request. The function extracts the target metric from the request and returns its value along with a dummy timestamp.

Initialization
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: main(SuperTwin)

    Initializes the Flask server and sets up database connections.

    :param SuperTwin: An object representing a specific configuration or environment.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To run the server, execute the script with Python. The main function takes a SuperTwin object as an argument, which contains configuration details like database address and name.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    if __name__ == '__main__':
        main("dolap", "10.36.54.195")

.. _observation:

Observation
-----------

15) Flask Web Server with InfluxDB Integration
++++++++++++++++++++++++++++++++++++++++++++++

This script creates a Flask-based web server integrated with InfluxDB for handling and processing time-series data.

1. **Module Imports**:
   - `influxdb.InfluxDBClient`: Used to connect to and interact with an InfluxDB database.
   - `influxdb.SeriesHelper`: Assists in the creation of data series for InfluxDB.
   - `pandas as pd`: Data manipulation and analysis library.
   - `datetime`: Module for manipulating dates and times.
   - `time`: Module for time-related tasks.
   - `sys`: System-specific parameters and functions.
   - `utils`: Custom module, presumably for utility functions.

2. **Functions**:
   - `query_string(metric, tagkey)`: Constructs a query string for InfluxDB.
   - `difference(to_normal, normal)`: Calculates the time difference between two timestamps.
   - `normalized(to_normal, difference)`: Adjusts a timestamp by a given time difference.
   - `normalize_tag(SuperTwin, _tag, no_subtags)`: Normalizes time tags for a given metric in InfluxDB.
   - `normalize_twin_tags(st1, st2, st3, st4)`: Normalizes time tags for multiple InfluxDB measurements.

3. **Flask App Configuration**:
   - `app`: Flask application instance.
   - `CORS(app)`: Enables CORS for the Flask app.
   - `app.config`: Configures CORS headers.

4. **Flask Routes**:
   - `@app.route('/')`: Root route, returns a simple 'OK' response.
   - `@app.route('/search')`: Handles search requests.
   - `@app.route('/query')`: Processes query requests and fetches data from InfluxDB.

5. **Main Function**:
   - Connects to InfluxDB and fetches data for specified tags.
   - Runs the Flask app on a specified host and port.

.. note:: The script uses utility functions from the `utils` module for database interactions and data processing. Ensure that the `utils` module is correctly configured and accessible.



16) Remote Command Execution and Monitoring Script
+++++++++++++++++++++++++++++++++++++++++++++++++

This Python script is designed to execute commands and scripts on remote systems (referred to as "SuperTwins") and observe their execution time. It uses SSH for remote execution and SCP for file transfer. Additionally, it integrates with Performance Co-Pilot (PCP) to monitor the performance metrics during the execution.

1. **Module Imports**:
   - Standard modules: `sys`, `subprocess`, `shlex`, `uuid`.
   - SSH and SCP related modules: `paramiko`, `SCPClient`.
   - Custom modules: `sampling`, `remote_probe`. These are assumed to be part of a larger framework for performance monitoring and analysis.
   - Time measurement: `timeit.default_timer`.

2. **Functions**:
   
   - `observe_wrap(SuperTwin, command)`: Executes a command on a remote system and observes its execution time. It sets up SSH and SCP connections, generates a unique observation ID, and runs the command while monitoring it with PCP.

   - `observe_script_wrap(SuperTwin, script)`: Similar to `observe_wrap` but for executing a script file on the remote system. It transfers the script to the remote system and then executes it, again observing the execution time.

   - `observe_single(SuperTwin, observation_id, command, obs_conf)`: A simplified version of `observe_wrap` which takes an existing observation ID and configuration to execute a single command.

   - `observe_single_parameters(SuperTwin, path, affinity, observation_id, command, obs_conf)`: An extension of `observe_single` that allows specifying a working directory (`path`) and processor affinity (`affinity`) for the command.

3. **Remote Execution and Monitoring Logic**:
   - The script is built to handle tasks on remote systems, identified as SuperTwins, by executing commands or scripts on them.
   - It uses SSH for remote command execution and SCP for file transfer.
   - Performance monitoring is done using Performance Co-Pilot, which is triggered alongside the remote commands/scripts.
   - Execution time is measured and returned for each task.

4. **Usage Notes**:
   - The script requires the SuperTwin objects to have specific attributes like SSH credentials and addresses.
   - It assumes the existence of specific directories on the remote systems for storing and running scripts.
   - The `sampling` and `remote_probe` modules are custom and need to be present for the script to function.

.. note:: This script is part of a larger system and relies on external custom modules and specific remote system configurations. Ensure all dependencies are correctly set up and the remote systems are configured to accept SSH and SCP connections from the host running this script.

.. _probing:

Probing
---------

17) benchmark.py
++++++++++++++++

This script is designed to calculate and analyze the roofline model for stream benchmark results.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- detect_utils: A utility module for detection tasks.
- subprocess: A module for running new applications or programs through Python.
- pprint: A data pretty printer.

Global Variables
^^^^^^^^^^^^^^^^^^^^^^^^^

- mt_scale: A dictionary to store scaling metrics for different operations like Copy, Scale, Add, and Triad.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: get_ridge_point(bw, flop)

    Calculates and returns the ridge point in the roofline model.

    :param bw: Bandwidth.
    :param flop: Floating point operations per second.
    :return: Ridge point value.

.. function:: peak_theoretical_flop(no_procs, core_per_proc, clock_speed, no_fma_units, max_vector_size)

    Computes the peak theoretical floating point operations per second.

    :param no_procs: Number of processors.
    :param core_per_proc: Number of cores per processor.
    :param clock_speed: Clock speed of the processor.
    :param no_fma_units: Number of FMA (Fused Multiply-Add) units.
    :param max_vector_size: Maximum vector size.
    :return: Peak GFLOP/s value.

.. function:: parse_one_stream_res(stream_res, threads)

    Parses one set of STREAM benchmark results.

    :param stream_res: Dictionary to store stream results.
    :param threads: Number of threads.
    :return: Updated stream_res dictionary.

.. function:: start_bench()

    Starts the STREAM benchmark.

.. function:: get_roof_values(max_bw, peak_g_flop, ridge_point)

    Generates roofline model values based on max bandwidth, peak GFLOPs, and ridge point.

    :param max_bw: Maximum bandwidth.
    :param peak_g_flop: Peak GFLOP/s value.
    :param ridge_point: Ridge point in the roofline model.

Main Execution
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: main()

    The main function to initiate the roofline model calculation process. It involves starting the benchmark, parsing results, and computing the roofline model.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To execute the script, run it with Python, ensuring all dependencies are satisfied.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    if __name__ == "__main__":
        main()

18) detect_utils.py
+++++++++++++++++++


This script is used for detecting and processing various hardware information on a system.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- contextlib: Utilities for common tasks involving the `with` statement.
- os: Miscellaneous operating system interfaces.
- re: Regular expression operations.
- subprocess: Subprocess management.
- sys: System-specific parameters and functions.
- uuid: UUID objects according to RFC 4122.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: cmd(cmdline)

    Executes a shell command and returns its output.

    :param cmdline: Command line to be executed.
    :return: Tuple (return code, output).

.. function:: output_lines(cmdline)

    Runs a shell command and returns its output split into lines.

    :param cmdline: Command line to be executed.
    :return: List of output lines.

.. function:: parse_lldtool(hw_lst, interface_name, lines)

    Parses the output from the `lldptool` command.

    :param hw_lst: Hardware list to update.
    :param interface_name: Network interface name.
    :param lines: Output lines from `lldptool`.
    :return: Updated hardware list.

.. function:: get_lld_status(hw_lst, interface_name)

    Retrieves LLDP status for a given network interface.

    :param hw_lst: Hardware list to update.
    :param interface_name: Network interface name.
    :return: Updated hardware list.

.. function:: parse_ethtool(hw_lst, interface_name, lines)

    Parses the output from the `ethtool` command.

    :param hw_lst: Hardware list to update.
    :param interface_name: Network interface name.
    :param lines: Output lines from `ethtool`.
    :return: Updated hardware list.

.. function:: get_ethtool_status(hw_lst, interface_name)

    Retrieves ethtool status for a given network interface.

    :param hw_lst: Hardware list to update.
    :param interface_name: Network interface name.
    :return: Updated hardware list.

.. function:: which(program)

    Searches for a given program in PATH and returns its full path.

    :param program: Program to search for.
    :return: Full path of the program or None.

.. function:: size_in_gb(size)

    Converts a size string to GB.

    :param size: Size string (e.g., '8 GB').
    :return: Size in GB.

.. function:: clean_str(val)

    Cleans a string from invalid UTF-8 characters.

    :param val: String to be cleaned.
    :return: Cleaned string.

.. function:: clean_tuples(lst)

    Cleans a list of tuples from invalid UTF-8 strings.

    :param lst: List of tuples.
    :return: Cleaned list of tuples.

.. function:: _get_uuid_x86_64()

    Retrieves UUID for x86_64 architecture.

    :return: UUID string.

.. function:: _get_uuid_ppc64le(hw_lst)

    Retrieves UUID for ppc64le architecture.

    :param hw_lst: Hardware list.
    :return: UUID string.

.. function:: get_uuid(hw_lst)

    Retrieves system UUID based on architecture.

    :param hw_lst: Hardware list.
    :return: UUID string.

.. function:: get_value(hw_lst, *vect)

    Gets a specific value from the hardware list.

    :param hw_lst: Hardware list.
    :param vect: Tuple of keys to search for.
    :return: Value or empty string if not found.

.. function:: get_cidr(netmask)

    Converts a netmask to CIDR notation.

    :param netmask: Netmask string (e.g., '255.255.255.0').
    :return: CIDR notation string.

.. function:: from_file(filename)

    Reads the first line of a file.

    :param filename: Name of the file.
    :return: First line of the file.

.. function:: fix_bad_serial(hw_lst, system_uuid, mobo_id, nic_id)

    Fixes bad serial numbers in the hardware list.

    :param hw_lst: Hardware list.
    :param system_uuid: System UUID.
    :param mobo_id: Motherboard ID.
    :param nic_id: NIC ID.

.. function:: get_cpus(hw_lst)

    Retrieves CPU information and updates the hardware list.

    :param hw_lst: Hardware list to update.

.. function:: modprobe(module)

    Loads a kernel module using `modprobe`.

    :param module: Name of the module to load.

.. function:: detect_auxv()

    Detects auxiliary vector information.

    :return: List of tuples with auxv information.

.. function:: parse_ahci(words)

    Parses AHCI information from a list of words.

    :param words: List of words to parse.
    :return: List of tuples with parsed AHCI information.

.. function:: parse_dmesg()

    Runs `dmesg` and parses its output.

    :return: List of tuples with parsed dmesg information.

.. function:: search_nested(keyword, node, default_return=None)

    Searches for a keyword in a nested dictionary or list.

    :param keyword: Keyword to search for.
    :param node: Nested dictionary or list.
    :param default_return: Default return value if keyword not found.
    :return: List of search results or default_return if not found.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use this script, ensure all dependencies are installed and import the script in your Python project. Functions can then be called with appropriate parameters to retrieve hardware information.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    hw_lst = []
    get_ethtool_status(hw_lst, "eth0")
    print(hw_lst)

19) diskinfo.py
+++++++++++++++


This script is used to detect and gather disk information on a system.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- os: Miscellaneous operating system interfaces.
- re: Regular expression operations.
- sys: System-specific parameters and functions.
- detect_utils: Custom utility module for detection.
- smart_utils: Custom utility module for SMART data handling.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: sizeingb(size)

    Converts size from bytes to gigabytes.

    :param size: Size in bytes.
    :return: Size in gigabytes.

.. function:: disksize(name)

    Retrieves the disk size.

    :param name: Disk name.
    :return: Disk size in gigabytes.

.. function:: disknames()

    Retrieves the names of all disks.

    :return: List of disk names.

.. function:: get_disk_info(name, sizes, hw_lst)

    Gathers various information about a disk.

    :param name: Disk name.
    :param sizes: Dictionary of disk sizes.
    :param hw_lst: Hardware list to update.

.. function:: get_disk_cache(name, hw_lst)

    Retrieves disk cache information.

    :param name: Disk name.
    :param hw_lst: Hardware list to update.

.. function:: get_disk_id(name, hw_lst)

    Retrieves disk identifiers.

    :param name: Disk name.
    :param hw_lst: Hardware list to update.

.. function:: parse_hdparm_output(output)

    Parses the output from the `hdparm` command.

    :param output: `hdparm` command output.
    :return: Parsed data.

.. function:: diskperfs(names)

    Retrieves disk performance data.

    :param names: List of disk names.
    :return: Dictionary of disk performances.

.. function:: disksizes(names)

    Retrieves sizes for a list of disks.

    :param names: List of disk names.
    :return: Dictionary of disk sizes.

.. function:: detect()

    Main function to detect disk information.

    :return: List of disk information tuples.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use this script, ensure all dependencies are installed and import the script in your Python project. The `detect` function can be called to retrieve disk information.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    detected_disks = detect()
    for disk in detected_disks:
        print(disk)

20) parse_cpuid.py
++++++++++++++++++


This script parses CPUID information to gather detailed characteristics of the CPU such as cache, monitoring capabilities, and frequency details.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- detect_utils: Custom utility module for executing and capturing output of shell commands.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: check_faulty_report(name)

    Checks if the CPU name corresponds to a known faulty CPUID report.

    :param name: The name of the CPU.
    :return: Boolean indicating whether the CPU has a known faulty report.

.. function:: fix_faulty_report(info, name)

    Fixes the faulty CPUID report for known issues.

    :param info: The parsed CPUID information.
    :param name: The name of the CPU.
    :return: Fixed CPUID information.

.. function:: gv_parentheses(cpuid_string)

    Extracts information enclosed in parentheses.

    :param cpuid_string: A string containing information in parentheses.
    :return: Extracted information.

.. function:: gv_parentheses_space(cpuid_string)

    Extracts information enclosed in parentheses, including an additional preceding word.

    :param cpuid_string: A string containing information in parentheses.
    :return: Extracted information with an additional word.

.. function:: parse_cpuid()

    Parses CPUID information to extract various CPU characteristics.

    :return: A dictionary containing parsed CPUID information.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use this script, ensure that `detect_utils` is correctly implemented and accessible. The `parse_cpuid` function can be called to retrieve CPUID information.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    cpu_info = parse_cpuid()
    print('CPU Info:', cpu_info)

21) parse_likwid_topology.py
++++++++++++++++++++++++++++


This script is designed to parse hardware affinity and topology using the Likwid tool, providing detailed information about sockets, domains, cache topology, and CPU-GPU affinity.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- detect_utils: Custom utility module for executing and capturing output of shell commands.
- re: Regular expression module for string searching and manipulation.
- pprint: Pretty-print module for formatted display of data structures.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: find_ind(to_find, str_list)

    Finds the index of the first occurrence of a string in a list.

    :param to_find: The string to find.
    :param str_list: The list to search.
    :return: The index of the found string or None.

.. function:: find_ind_multiple(to_find, str_list, occurrence)

    Finds the index of a specific occurrence of a string in a list.

    :param to_find: The string to find.
    :param str_list: The list to search.
    :param occurrence: The occurrence number to find (1-based).
    :return: The index of the found occurrence or None.

.. function:: parse_cache_topology(topol, ret_dict, name, level)

    Parses cache topology information from the Likwid output.

    :param topol: The topology data as a list of strings.
    :param ret_dict: The dictionary to store parsed data.
    :param name: The cache level name (e.g., 'L1D').
    :param level: The cache level.
    :return: The dictionary with added cache topology information.

.. function:: parse_likwid()

    Parses output from the Likwid tool to extract hardware topology.

    :return: A list containing socket groups, domains, cache topology, and GPU info.

.. function:: remove_whitespace(ls)

    Removes empty strings from a list.

    :param ls: The list to clean.
    :return: The cleaned list.

.. function:: parse_affinity()

    Parses CPU affinity information from the Likwid tool.

    :return: A dictionary containing parsed CPU affinity data.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use this script, ensure that Likwid is installed and accessible. Call the `parse_likwid` function to retrieve hardware topology information and `parse_affinity` for CPU affinity data.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    socket_groups, domains, cache_topology, gpu_info = parse_likwid()
    print('Socket groups:', socket_groups)
    print('Domains:', domains)
    print('Cache topology:', cache_topology)
    print('GPU info:', gpu_info)

    affinity = parse_affinity()
    pprint(affinity)

22) parse_lshw.py
+++++++++++++++++


This script utilizes the `lshw` tool to parse detailed hardware information of a system, including CPU, memory, disk, network, and kernel data.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- json: Module for JSON manipulation.
- detect_utils: Custom utility module for executing and capturing output of shell commands.
- pprint: Pretty-print module for formatted display of data structures.
- collections: Module for specialized container datatypes.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: generate_hardware_dict(to_gen, info_list)

    Generates a nested dictionary structure from a list of tuples.

    :param to_gen: The dictionary to be generated.
    :param info_list: The list of hardware information tuples.
    :return: The updated dictionary with hardware information.

.. function:: find_field_recursive(top_dict, _class, _description, found)

    Recursively searches for a hardware component in the nested dictionary.

    :param top_dict: The top-level dictionary.
    :param _class: The class of the hardware component.
    :param _description: The description of the hardware component.
    :param found: List to store the found components.
    :return: Updates the `found` list with matching components.

.. function:: find_field(top_dict, _class, _description, found)

    Wrapper function for `find_field_recursive`.

    :param top_dict: The top-level dictionary.
    :param _class: The class of the hardware component.
    :param _description: The description of the hardware component.
    :param found: List to store the found components.

.. function:: parse_lshw()

    Parses the output of the `lshw` command to extract hardware information.

    :return: Dictionary containing parsed hardware information.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use this script, ensure that `lshw` is installed on the system. The script will parse the hardware information and print it in a structured format.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    hardware_info = parse_lshw()
    pprint.pprint(hardware_info)

23) parse_showevtinfo.py
++++++++++++++++++++++++

This script uses the `pmu_event_query` tool to parse Performance Monitoring Unit (PMU) event information in a system.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- detect_utils: Custom utility module for executing and capturing output of shell commands.
- json: Module for JSON manipulation.
- pprint: Pretty-print module for formatted display of data structures.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: find_pmu(keys, name_line)

    Finds a PMU in the list of keys based on a name line.

    :param keys: List of PMU keys.
    :param name_line: Line containing the PMU name.
    :return: The PMU key if found, otherwise None.

.. function:: get_masks_modifiers(lines)

    Parses mask and modifier information from PMU event lines.

    :param lines: Lines containing PMU event details.
    :return: Dictionary with masks and modifiers.

.. function:: parse_event(pmus, event)

    Parses a PMU event and updates the PMU dictionary.

    :param pmus: Dictionary of PMUs.
    :param event: String containing the PMU event data.
    :return: Updated PMU dictionary.

.. function:: parse_evtinfo()

    Parses the output from the PMU event query tool.

    :return: Dictionary containing parsed PMU event information.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

Execute this script to parse PMU event information from the system. The results are printed in a structured format and saved to a JSON file.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    event_info = parse_evtinfo()
    pprint.pprint(event_info)

    # Save to JSON file
    with open("evtinfo.json", "w") as outfile:
        json.dump(event_info, outfile)

24) probe.py
++++++++++++

This script gathers detailed hardware information from a system, including CPU, memory, disk, network, and GPU details. It utilizes several custom modules to probe different hardware components.

Imports
^^^^^^^^^^^^^^^^^^^^^^^^^

- system, diskinfo, detect_utils: Custom modules for detecting various hardware components.
- parse_cpuid, parse_likwid_topology, parse_lshw, parse_evtinfo: Custom modules for parsing CPU, memory, and hardware topology information.
- json: Module for JSON manipulation.
- sys: System-specific parameters and functions.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. function:: choose_info(hostname, system, cache_info, socket_groups, domains, cache_topology, affinity, gpu_info, PMUs, pmprobe)

    Consolidates hardware information into a chosen format for further processing.

    :param hostname: System hostname.
    :param system: Dictionary containing system information.
    :param cache_info: CPU cache information.
    :param socket_groups: Information about CPU socket groups.
    :param domains: NUMA domain information.
    :param cache_topology: Cache topology information.
    :param affinity: CPU affinity information.
    :param gpu_info: GPU information.
    :param PMUs: Performance Monitoring Units information.
    :param pmprobe: Available metrics from PMU.
    :return: Dictionary with consolidated hardware information.

.. function:: generate_hardware_dict(to_gen, info_list)

    Generates a nested dictionary from a list of hardware information.

    :param to_gen: The initial dictionary to populate.
    :param info_list: List of hardware information tuples.
    :return: Nested dictionary of hardware information.

.. function:: print_hardware_dict(hw_dict)

    Prints the hardware dictionary in a structured format.

    :param hw_dict: Dictionary containing hardware information.

.. function:: get_pmprobe()

    Retrieves available metrics from the system's Performance Monitoring Units.

    :return: List of available metrics.

.. function:: main()

    Main function to execute the hardware probing. It gathers information from various sources and saves it to a JSON file.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

Run the script to probe the system's hardware and generate a JSON file with detailed information. This file can be used for further analysis or integration with other systems.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    info = main()
    # info now contains detailed hardware information about the system

25) smart_utils_info.py
+++++++++++++++++++++++

This documentation describes two Python dictionaries, `NVME_INFOS` and `SMART_FIELDS`, used for mapping NVMe drive and SMART attributes to more readable formats.

NVME_INFOS Dictionary
^^^^^^^^^^^^^^^^^^^^^^^^^

The `NVME_INFOS` dictionary maps NVMe drive attribute labels to their corresponding key names. This mapping is useful for processing and presenting NVMe drive information in a structured and comprehensible manner.

Attributes include:

- Model Number
- Serial Number
- Firmware Version
- Total NVM Capacity
- Warning and Critical Temperature Thresholds
- Critical Warning
- Temperature
- Power Cycles
- Power On Hours
- Unsafe Shutdowns
- Media and Data Integrity Errors
- Error Information Log Entries

SMART_FIELDS Dictionary
^^^^^^^^^^^^^^^^^^^^^^^^^

The `SMART_FIELDS` dictionary is designed to map attributes obtained from SMART (Self-Monitoring, Analysis, and Reporting Technology) diagnostics to user-friendly key names.

Attributes include:

- Serial Number
- SMART Health Status
- Specified Cycle Count Over Device Lifetime
- Accumulated Start-Stop Cycles
- Specified Load-Unload Count Over Device Lifetime
- Accumulated Load-Unload Cycles
- Power On Hours
- Blocks Sent to Initiator
- Blocks Received from Initiator
- Blocks Read from Cache and Sent to Initiator
- Non-Medium Error Count
- Current Drive Temperature
- Drive Trip Temperature
- Manufacture Date
- Rotation Rate

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

These dictionaries are primarily used in scripts or applications that interpret data from NVMe drives or SMART diagnostics. By using these dictionaries, data can be transformed from raw output to a more readable and meaningful format for analysis or display.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    nvme_info = parse_nvme_output(raw_nvme_output, NVME_INFOS)
    smart_info = parse_smart_output(raw_smart_output, SMART_FIELDS)

    # nvme_info and smart_info now contain structured and readable information

26) smart_utils.py
++++++++++++++++++

This documentation describes a set of Python functions used for retrieving S.M.A.R.T (Self-Monitoring, Analysis, and Reporting Technology) data from disks. These functions are designed to parse various attributes and logs from disks supporting both SCSI and ATA standards.

Functions Overview
^^^^^^^^^^^^^^^^^^^^^^^^^

- ``_parse_line(line)``: Strips and decodes the line, handling any errors in encoding.
- ``read_smart_field(hwlst, line, device_name, item, title)``: Reads a specific SMART field from a line and appends it to the hardware list (hwlst).
- ``read_smart_scsi_error_log(hwlst, line, device_name, error_log)``: Reads and processes SCSI error log entries.
- ``read_smart_scsi(hwlst, device, optional_flag="", mode="")``: Processes SMART information for SCSI devices.
- ``read_smart_ata(hwlst, device, optional_flag="", mode="")``: Processes SMART information for ATA devices.
- ``read_smart(hwlst, device, optional_flag="")``: Determines the device type (SCSI or ATA) and calls the appropriate function to read SMART data.
- ``read_smart_nvme(hwlst, device_name)``: Reads SMART information specific to NVMe devices.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

These functions are typically called with the following parameters:

- ``hwlst``: A list that the function will append hardware information to.
- ``line``: A line of text (usually from smartctl output) to be processed.
- ``device``: The device name (e.g., /dev/sda).
- ``device_name``: The basename of the device.
- ``item`` and ``title``: Used to identify and label the SMART field.
- ``optional_flag`` and ``mode``: Additional flags or modes for smartctl commands.

Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    hwlst = []
    device = "/dev/sda"
    read_smart(hwlst, device)

After execution, ``hwlst`` will contain a list of tuples representing various SMART attributes of the device.

27) system.py
+++++++++++++

The `detect` function is designed to gather various system characteristics by analyzing the output of the `lshw` command. It parses the XML output from `lshw` and populates a list with hardware information.

Function Overview
^^^^^^^^^^^^^^^^^^^^^^^^^

- ``detect(output=None)``: Main function to detect system characteristics.

Parameters
^^^^^^^^^^^^^^^^^^^^^^^^^
- ``output``: (Optional) The output of the `lshw -xml` command. If not provided, the function will execute `lshw -xml` internally.

Returns
^^^^^^^^^^^^^^^^^^^^^^^^^
- A list of tuples, where each tuple represents a piece of hardware information.

Description
^^^^^^^^^^^^^^^^^^^^^^^^^

The function uses various helper methods to parse the `lshw` XML output:

- ``_find_element``: Searches for specific elements in the XML and populates the hardware list.
- Other helper functions are used to handle the parsing of different system components, such as motherboard, BIOS, memory, and network interfaces.

The function also utilizes external utility functions from the `detect_utils` module to gather additional information, including CPU details, operating system version, kernel version, and architecture.

Usage Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    hardware_info = detect()

After execution, `hardware_info` will contain a list of tuples representing various system attributes like CPU, motherboard, network interfaces, and more.

Note
^^^^^^^^^^^^^^^^^^^^^^^^^

This function is designed to work on systems where `lshw` is available and provides XML output. It may need modifications to work correctly on different system configurations or in environments where `lshw` is not available.

28) detect_utils.py
+++++++++++++++++++

This Python module provides functions for detecting various system hardware and configuration details, primarily using system commands and parsing their output.

Functions Overview
^^^^^^^^^^^^^^^^^^^^^^^^^

- ``cmd(cmdline)``: Executes a shell command and returns its exit status and output.
- ``output_lines(cmdline)``: Runs a shell command and returns the output as lines.
- ``parse_lldtool(hw_lst, interface_name, lines)``: Parses LLDP tool output and adds parsed data to the hardware list.
- ``get_lld_status(hw_lst, interface_name)``: Gets LLDP status for a given network interface.
- ``parse_ethtool(hw_lst, interface_name, lines)``: Parses ethtool output for various network interface properties.
- ``get_ethtool_status(hw_lst, interface_name)``: Retrieves ethtool status for a network interface.
- ``which(program)``: Checks if a program is executable and returns its path.
- ``size_in_gb(size)``: Converts size to GB format.
- ``clean_str(val)``: Cleans up strings with invalid UTF-8 encoding.
- ``clean_tuples(lst)``: Cleans a list of tuples from bad UTF-8 strings.
- ``get_uuid(hw_lst)``: Retrieves the UUID of the system.
- ``get_value(hw_lst, *vect)``: Retrieves a value from the hardware list.
- ``get_cidr(netmask)``: Converts a netmask to CIDR format.
- ``from_file(filename)``: Reads the first line of a file.
- ``fix_bad_serial(hw_lst, system_uuid, mobo_id, nic_id)``: Fixes bad serial numbers known for certain vendors.
- ``get_cpus(hw_lst)``: Retrieves CPU information and adds it to the hardware list.
- ``modprobe(module)``: Loads a kernel module using modprobe.
- ``detect_auxv()``: Detects auxiliary vector (AUXV) information.
- ``parse_ahci(words)``: Parses AHCI information from dmesg output.
- ``parse_dmesg()``: Runs and parses dmesg output.

Description
^^^^^^^^^^^^^^^^^^^^^^^^^

These functions are utility tools designed to extract and parse hardware information from a Linux-based system. They use various system tools like `lshw`, `ethtool`, `dmidecode`, and system files to gather information such as CPU details, network interface configurations, system UUID, and more.

The functions primarily operate by executing system commands and parsing their output to collect detailed information about different components of the system.

Usage Example
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python

    hw_lst = []
    get_cpus(hw_lst)
    print(hw_lst)

This example populates `hw_lst` with CPU-related information. The module functions can be used similarly to gather other types of system information.

Note
^^^^^^^^^^^^^^^^^^^^^^^^^

The module is designed for use on Linux-based systems. It may require adjustments or may not function as intended on non-Linux systems or in environments where certain system tools are unavailable or restricted.

29) remote_probe.py
+++++++++++++++++++

This module is designed to remotely probe a system for hardware and configuration information using SSH and SCP.

Overview
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script connects to a remote host via SSH, executes various commands to gather system information, and then uses SCP to transfer the data back to the local machine.
- The remote probing involves executing scripts located in specified paths (`system_query_path`, `pmu_query_path`) on the remote host.
- The script requires `paramiko` and `scp` Python modules for SSH and SCP functionalities, respectively.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

- ``progress4(filename, size, sent, peername)``: Callback function for SCP progress.
- ``run_sudo_command(ssh_client, SSHkey, name, command)``: Executes a command with sudo on the remote system.
- ``run_sudo_command_perfevent(ssh_client, SSHkey, name, command)``: Specialized function for executing performance-related commands.
- ``run_command(ssh_client, name, command)``: Executes a regular command on the remote system.
- ``main(*args)``: Main function to handle remote system probing.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

The script can be executed directly from the command line or imported as a module. It supports passing the remote host's SSH credentials (host, username, password) as arguments. If credentials are not provided, it prompts the user for them.

Example Command
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

    python remote_system_probing.py <remote_host> <username> <password>

This command would initiate the probing process on the specified remote host using the provided SSH credentials.

Note
^^^^^^^^^^^^^^^^^^^^^^^^^

- Ensure that the paths to the `system_query` and `pmu_event_query` directories are correctly set and accessible.
- The script requires appropriate permissions on the remote system to execute commands and access system information.
- The script is designed for Linux-based systems and might need adjustments for other operating systems.

.. _sampling:

Sampling
---------

30) initiate.py
+++++++++++++++

This script is designed for system monitoring and dashboard generation using a combination of tools and databases like InfluxDB and MongoDB.

Overview
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script facilitates the collection of system metrics, their storage in InfluxDB, and the creation of visual dashboards for monitoring.
- It utilizes a Digital Twin representation of the system for detailed monitoring.
- The script relies on various external libraries and assumes certain directory structures and file locations.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

- ``get_date_tag()``: Generates a unique date-based tag for each run.
- ``generate_pcp2influxdb_config(config_file, tag, sourceIP, source_name)``: Generates a configuration file for Performance Co-Pilot (PCP) to InfluxDB data transfer.
- ``get_mongo_database(mongodb_name)``: Establishes a connection to a MongoDB database.
- ``get_influx_database(influxdb_name)``: Creates and connects to an InfluxDB database.
- ``run_single(hostname, date, config_file, dt_pruned, command)``: Executes a single command for system monitoring and logs the data.
- ``run_commands(hostname, date, config_file, dt_pruned, commands)``: Executes multiple system monitoring commands.
- ``system_dashboard_prepare(hostname, twin_id)``: Prepares the system dashboard for the specified host.
- ``system_dashboard_launch(comp_dashes)``: Launches the system dashboard.
- ``read_commands(commands_file)``: Reads monitoring commands from a file.
- ``main(hostname, hostIP, hostProbFile, monitoringMetricsConf)``: Main function that orchestrates the monitoring and dashboard generation.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use the script, ensure the required MongoDB and InfluxDB instances are running and accessible. The script should be executed with the hostname, IP address of the host, a JSON file containing system information, and a configuration file for monitoring metrics.

Example Command
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

    python system_monitoring.py <hostname> <hostIP> <hostProbFile> <monitoringMetricsConf>

Dependencies
^^^^^^^^^^^^^^^^^^^^^^^^^

- Python libraries: `datetime`, `subprocess`, `influxdb`, `pymongo`, `paramiko`, `scp`.
- External tools: InfluxDB, MongoDB, Performance Co-Pilot (PCP).

Note
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script is designed for Linux-based systems and might require adjustments for other operating systems.
- Proper permissions and network accessibility are necessary for the script to function correctly.
- The script assumes that the required external tools and databases are already installed and configured.



31) sampling.py
+++++++++++++++

This script facilitates the setup of Performance Co-Pilot (PCP) to InfluxDB configurations for system performance monitoring.

Overview
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script helps in setting up and managing the configuration for PCP to monitor system metrics and store them in InfluxDB.
- It supports remote configuration and execution of performance monitoring daemons.
- The script is part of a larger framework that involves remote system monitoring and data analysis.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

- ``get_date_tag()``: Generates a unique timestamp tag.
- ``add_pcp(SuperTwin, config_lines)``: Adds PCP specific configuration lines.
- ``generate_pcp2influxdb_config(SuperTwin)``: Generates a PCP to InfluxDB configuration file based on the provided `SuperTwin` object.
- ``generate_pcp2influxdb_config_observation(SuperTwin, observation_id)``: Generates a PCP to InfluxDB configuration for a specific observation.
- ``generate_perfevent_conf(SuperTwin)``: Creates a configuration file for performance events based on the `SuperTwin` object.
- ``reconfigure_perfevent(SuperTwin)``: Reconfigures the remote performance event monitoring daemon.
- ``main(SuperTwin)``: Main function that orchestrates the configuration generation and starts the monitoring process.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use this script, an instance of `SuperTwin` (a custom object representing the system to be monitored) should be provided. This object contains details like system name, metrics to be monitored, and other necessary configurations.

Example Command
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

    python performance_monitoring.py <SuperTwin_Object>

Dependencies
^^^^^^^^^^^^^^^^^^^^^^^^^

- Python libraries: `datetime`, `subprocess`, `shlex`, `paramiko`, `scp`.
- External tools: InfluxDB, PCP (Performance Co-Pilot).

Note
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script is designed to work in a system where InfluxDB and PCP are installed and configured.
- It requires network accessibility to the system being monitored.
- The script is part of a larger monitoring and analysis framework, and its functionality is dependent on the correct setup of this framework.


.. _twin_description:

twin_description
---------

32) generate_date.py
++++++++++++++++++++

This script generates a digital twin of a system for monitoring purposes, using Performance Co-Pilot (PCP) and other system metrics.

Overview
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script constructs a digital twin, a virtual model of a physical system, to facilitate monitoring and analysis.
- It leverages system metrics, including those provided by PCP, to build a comprehensive representation of the system's state.
- The digital twin is constructed as a set of interfaces, each representing different system components like CPU, memory, disk, network, and others.

Functions
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script includes various functions to add components (CPU, memory, etc.), properties, and relationships to the digital twin.
- Functions like `get_interface`, `get_relationship`, and `get_property` help in building the structure of the digital twin.
- Specialized functions like `add_cpus`, `add_memory`, `add_disk`, and `add_network` are used to add specific system components to the twin.
- The `main` function orchestrates the process, using system information to generate the complete digital twin.

Usage
^^^^^^^^^^^^^^^^^^^^^^^^^

To use this script, system information needs to be provided. This can include details about CPUs, memory, storage, network interfaces, and performance metrics.

Example Command
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

    python digital_twin_generator.py <System_Info>

Dependencies
^^^^^^^^^^^^^^^^^^^^^^^^^

- Python libraries: `json`, `datetime`, `subprocess`, `shlex`.
- External tools and libraries: Performance Co-Pilot (PCP), Paramiko for SSH communication.

Note
^^^^^^^^^^^^^^^^^^^^^^^^^

- The script is designed for advanced system monitoring and analysis tasks.
- It requires an understanding of system architecture and performance metrics.
- The generated digital twin can be used in various monitoring and analysis applications, like predictive maintenance, system optimization, and troubleshooting.

