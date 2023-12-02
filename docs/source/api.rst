API
===

.. autosummary::
   :toctree: generated

   lumache


.. _get_next_color:

get_next_color()
----------------

.. rubric:: ➤ Functionality

The ``get_next_color()`` function cycles through a predefined list of color codes, 

.. rubric:: ⚙ Parameters

- `next_color`: A global variable that keeps track of the current position in the **colors** list.
- `colors`: A global list containing the hexadecimal color codes to be cycled through.

.. rubric:: ↩ Returns

- `Return Type:` `string`
- `Description:` Returns a hexadecimal color code (e.g., `#4A90E2`). This is the next color in the `colors` list.

.. _round_power_of_2(number):

_round_power_of_2(number)
-------------------------

.. rubric:: ➤ Functionality

The ``_round_power_of_2(number)`` function rounds a given number to the nearest higher power of two. 

.. rubric:: ⚙ Parameters

- `number`: The number to be rounded.

.. rubric:: ↩ Returns

- `Return Type:` `int`
- `Description:` The nearest higher power of two to the given number.

.. _carm_eq:

carm_eq(ai, bw, fp)
--------------------

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

upload_to_grafana(json, server, api_key, verify)
------------------------------------------------

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

get_dashboard_json(dashboard, overwrite, message)
--------------------------------------------------

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

template_dict()
---------------

.. rubric:: ➤ Functionality

Creates a template dictionary with default settings for a Grafana dashboard.

.. rubric:: ⚙ Parameters

None.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary template for a Grafana dashboard with default settings.

.. _return_line:

return_line(ai, eq, name, color, dash)
---------------------------------------

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

line_spec(color, dash)
-----------------------

.. rubric:: ➤ Functionality

Generates a specification for the style of a line in a Plotly graph.

.. rubric:: ⚙ Parameters

- `color`: The color of the line.
- `dash`: The dash style of the line.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A dictionary specifying the line's style.

.. _two_templates_one:

two_templates_one(data, layout)
--------------------------------

.. rubric:: ➤ Functionality

Creates a Grafana panel with specific data and layout settings for displaying a Plotly graph.

.. rubric:: ⚙ Parameters

- `data`: Data to be displayed in the panel.
- `layout`: Layout configuration for the panel.

.. rubric:: ↩ Returns

- **Return Type:** `dict`
- **Description:** A Grafana panel template with data and layout.

.. _all_these_lines:

all_these_lines(datalines, data, ai, thread, color)
---------------------------------------------------

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

return_traces(data, ai, thread)
--------------------------------

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

return_subtraces(data, ai, thread, index)
-----------------------------------------

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

thread_group(fig, thread, color, data, ai, ai_list)
---------------------------------------------------

.. rubric:: ➤ Functionality

Adds multiple traces to a Plotly figure for a specific thread count.

.. rubric:: ⚙ Parameters

- `fig`: The Plotly figure object.
- `thread`: Thread count.
- `color`: Color code

.. _thread_groups:

thread_groups(fig, thread, color, data, ai, ai_list)
-----------------------------------------------------

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

grafana_layout(fig)
--------------------

.. rubric:: ➤ Functionality

Adjusts the layout of a Plotly figure to fit well within a Grafana dashboard.

.. rubric:: ⚙ Parameters

- `fig`: The Plotly figure object to be adjusted.

.. rubric:: ↩ Returns

- **Return Type:** `object`
- **Description:** The Plotly figure object with an adjusted layout for Grafana integration.

.. _main:

main(SuperTwin)
---------------

.. rubric:: ➤ Functionality

Main function orchestrating the creation of a performance analysis dashboard.

.. rubric:: ⚙ Parameters

- `SuperTwin`: Object or data structure representing the context or data for the dashboard.

.. rubric:: ↩ Returns

- **Return Type:** `string` or `dict`
- **Description:** URL or data structure representing the generated Grafana dashboard.





