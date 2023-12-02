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

- **next_color**: A global variable that keeps track of the current position in the **colors** list.
- **colors**: A global list containing the hexadecimal color codes to be cycled through.

.. rubric:: ↩ Returns

- **Return Type:**: **string**
- **Description:** Returns a hexadecimal color code (e.g., ``#4A90E2``). This is the next color in the ``colors`` list.

