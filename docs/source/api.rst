API
===

.. autosummary::
   :toctree: generated

   lumache

1) generate_plotly_panels_dd_go.py
++++++++++++++++++++++++++++++++++

This section documents the functions defined in the ``generate_plotly_panels_dd_go.py`` file.

.. _get_next_color:

1.1) get_next_color()
---------------------

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
------------------------------

.. rubric:: ➤ Functionality

The ``_round_power_of_2(number)`` function rounds a given number to the nearest higher power of two. 

.. rubric:: ⚙ Parameters

- `number`: The number to be rounded.

.. rubric:: ↩ Returns

- `Return Type:` `int`
- `Description:` The nearest higher power of two to the given number.

.. _carm_eq:

1.3) carm_eq(ai, bw, fp)
------------------------

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
-----------------------------------------------------

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
------------------------------------------------------

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
--------------------

.. rubric:: ➤ Functionality

Creates a template dictionary with default settings for a Grafana dashboard.

.. rubric:: ⚙ Parameters

None.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary template for a Grafana dashboard with default settings.

.. _return_line:

1.7) return_line(ai, eq, name, color, dash)
-------------------------------------------

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
---------------------------

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
------------------------------------

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
---------------------------------------------------------

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
-------------------------------------

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
-----------------------------------------------

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
---------------------------------------------------------

.. rubric:: ➤ Functionality

Adds multiple traces to a Plotly figure for a specific thread count.

.. rubric:: ⚙ Parameters

- `fig`: The Plotly figure object.
- `thread`: Thread count.
- `color`: Color code

.. _thread_groups:

1.14) thread_groups(fig, thread, color, data, ai, ai_list)
----------------------------------------------------------

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
-------------------------

.. rubric:: ➤ Functionality

Adjusts the layout of a Plotly figure to fit well within a Grafana dashboard.

.. rubric:: ⚙ Parameters

- `fig`: The Plotly figure object to be adjusted.

.. rubric:: ↩ Returns

- **Return Type:** `object`
- **Description:** The Plotly figure object with an adjusted layout for Grafana integration.

.. _main:

1.16) main(SuperTwin)
---------------------

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
------------------

.. rubric:: ➤ Functionality

Generates and returns a unique identifier by incrementing a global counter.

.. rubric:: ↩ Returns

- **Return Type:** `int`
- **Description:** The next unique identifier.


.. _get_params:

2.2) get_params(td, measurement)
--------------------------------

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
-----------------------------------------------------------

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
---------------------

.. rubric:: ➤ Functionality

Analyzes and returns the system topology from its digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** The topology of the system.


.. _stat_panel:

2.5) stat_panel(SuperTwin, h, w, x, y, color_scheme, metric, empty_dash)
------------------------------------------------------------------------

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
--------------------------------------

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
---------------------------------------

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
-----------------------------------------------------------------

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
--------------------------------------------------------

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
------------------

.. rubric:: ➤ Functionality

Generates and returns a unique identifier by incrementing a global counter.

.. rubric:: ↩ Returns

- **Return Type:** `int`
- **Description:** The next unique identifier.


.. _get_params:

3.2) get_params(td, measurement)
--------------------------------

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
-----------------------------------------------------------

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
---------------------

.. rubric:: ➤ Functionality

Analyzes and returns the system topology from its digital twin description.

.. rubric:: ⚙ Parameters

- `td`: Digital twin description.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** The topology of the system.


.. _generate_monitoring_dashboard:

3.5) generate_monitoring_dashboard(SuperTwin)
---------------------------------------------

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
------------------

.. rubric:: ➤ Functionality

Increments and returns the next unique identifier from a global counter.

.. rubric:: ↩ Returns

- **Return Type:** `int`
- **Description:** The next unique identifier in the sequence.


.. _get_params:

4.2) get_params(td, measurement)
--------------------------------

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
-----------------------------------------------------------

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
---------------------

.. rubric:: ➤ Functionality

Analyzes a digital twin description to determine the system topology, specifically mapping sockets to their corresponding cores and threads.

.. rubric:: ⚙ Parameters

- `td`: The digital twin description.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary representing the system topology.


.. _generate_monitoring_dashboard:

4.5) generate_monitoring_dashboard(SuperTwin)
---------------------------------------------

.. rubric:: ➤ Functionality

Generates a Grafana monitoring dashboard for the given digital twin, configuring panels and metrics based on the twin's description.

.. rubric:: ⚙ Parameters

- `SuperTwin`: The digital twin object for which the monitoring dashboard is being created.

.. rubric:: ↩ Returns

- **Return Type:** `string`
- **Description:** The URL of the newly generated Grafana dashboard.