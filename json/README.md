# JSON files for tested component libraries
- This directory contains a `template.json` with an example JSON file that can be used to fill in test results for different component libraries.
- Each component library has its own directory which in turn contains the JSON file specific to that framework. Any other relevant files or data (e.g. test results) can be committed to the specific directory as needed.

## How to add a new component library
- Create a directory with the name of the component library
- Copy the `template.json` into that directory and rename it to match the name of the component library.
- Fill in the test results (e.g. from [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview) tests), errors and any other useful data.
