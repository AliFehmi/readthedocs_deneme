API
===

.. autosummary::
   :toctree: generated

   lumache

## `get_next_color()`

### Functionality

- The `get_next_color()` function is designed to iterate through a predefined list of color codes, `colors`.
- Each time the function is called, it returns the next color in the sequence.
- Once the end of the list is reached, it continues again from the beginning, ensuring a continuous supply of colors.
- This function is particularly useful in data visualization contexts where different data series need to be distinguished by unique colors.

### Parameters

- The function does not take any external parameters.
- It relies on a global variable `next_color` which tracks the current index in the `colors` list.
- The `colors` list is also a global variable, containing the color codes to cycle through.

### Returns

- **Return Type:** `string`
- **Description:** The function returns a string representing the color code in hexadecimal format (e.g., `#FF5733`). This color code corresponds to the next color in the `colors` list.

