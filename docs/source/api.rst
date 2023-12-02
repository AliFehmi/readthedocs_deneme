API
===

.. autosummary::
   :toctree: generated

   lumache


.. _get_next_color:

get_next_color()
----------------

.. rubric:: Functionality

The ``get_next_color()`` function cycles through a predefined list of color codes, ``color_palette``.
It returns the next color in the sequence with each call.
Upon reaching the end of the color list, it starts over from the beginning, providing a continuous cycle of colors.
This function is ideal for use in data visualization to differentiate between various data series with distinct colors.

.. rubric:: Parameters

- ``color_index``: A global variable that keeps track of the current position in the ``color_palette`` list.
- ``color_palette``: A global list containing the hexadecimal color codes to be cycled through.

.. rubric:: Returns

- **Return Type:** ``string``
- **Description:** Returns a hexadecimal color code (e.g., ``#4A90E2``). This is the next color in the ``color_palette`` list.

