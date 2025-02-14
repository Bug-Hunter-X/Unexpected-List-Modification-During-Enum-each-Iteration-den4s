# Elixir List Modification Bug

This repository demonstrates a common issue in Elixir when attempting to modify a list while iterating over it using `Enum.each`. The code intends to remove the element `3` from the list, but due to the immutable nature of Elixir lists, it fails to do so. The example showcases this behavior and provides a corrected solution using `Enum.filter`.

## Bug Description
The original code attempts to remove an element from a list during iteration using `Enum.each`. However, this approach does not modify the list in place because Elixir lists are immutable. The attempt to update the `list` variable within the anonymous function creates a new list, which is discarded after each iteration. Therefore, the original `list` remains unchanged.