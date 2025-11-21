# NPM Dependency Visualizer

An interactive, single-file web application designed to visualize the dependency tree of any Node.js project. It utilizes the output of `npm ls --json` to render a dynamic, force-directed graph powered by D3.js, allowing for intuitive exploration, searching, and filtering of package relationships.

## ✨ Features

  * **Interactive Force-Directed Graph:** Uses D3.js to render a stable and visually appealing graph where nodes represent packages and links represent dependencies.
  * **Highlighting:** Hover or click on any node to highlight its direct dependencies and dependents. Clicking a node focuses the view and traces its full ancestry path to the root.
  * **Search Functionality:** Quickly find specific packages within the graph.
  * **Responsive UI:** A clean, modern interface styled with Tailwind CSS, ensuring usability on all screen sizes.
  * **Lock Mode:** Toggle the layout lock to prevent accidental dragging of nodes, allowing for smooth panning across the entire visualization.
  * **Node Coloring:** Nodes are color-coded by depth (Root, Direct Dependency, Transitive Dependency).

## 🚀 How to Use

Since this is a client-side visualization, you need to first generate the dependency data from your target Node.js project.

### 1\. Generate the JSON Data

Open your terminal in the root directory of the Node.js project you wish to visualize and run the following command:

```bash
npm ls --all --json > dependency-tree.json
