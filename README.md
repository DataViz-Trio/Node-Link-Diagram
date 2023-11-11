# Node-Link-Diagram

## Project Structure

- **Graph Files:** Contains Gephi graph files for positive and negative edges.
  - [positive_edges.gephi](Graph%20Files/Positive_edges.gephi): Gephi graph file for positive edges.
  - [negative_edges.gephi](Graph%20Files/Negative_edges.gephi): Gephi graph file for negative edges.

- **Screenshots:** Contains screenshots of node-link diagrams for both positive and negative edges.
  - **Positive:**
    - [Fruchterman Reingold.png](Screenshots/Positive/Fruchterman%20Reingold.png)
    - [OpenOrd.png](Screenshots/Positive/OpenOrd.png)
    - [Yifan Hu.png](Screenshots/Positive/Yifan%20Hu.png)
  - **Negative:**
    - [Fruchterman Reingold.png](Screenshots/Negative/Fruchterman%20Reingold.png)
    - [Force Atlas2.png](Screenshots/Negative/Force%20Atlas2.png)
    - [Yifan Hu.png](Screenshots/Negative/Yifan%20Hu.png)
    - [Yifan Hu Proportional.png](Screenshots/Negative/Yifan%20Hu%20Proportional.png)

- **Data:** Contains pre-processed CSV files.
  - [positive_edges.csv](Data/positive_edges.csv): CSV file for positive edges.
  - [negative_edges.csv](Data/negative_edges.csv): CSV file for negative edges.
  - [nodes.csv](Data/nodes.csv): CSV file containing node information.

- IPython Notebook for data preprocessing:
  - [preprocessing.ipynb](preprocessing.ipynb)

## Dataset Description

This dataset represents a network of politicians speaking in the United States Congress. Nodes are politicians, and directed edges denote one politician mentioning another. Edge weights represent whether the mention is in support (positive weight) or opposition (negative weight). Parallel edges and self-loops are allowed.

## Data Analysis and Preprocessing

1. **Loading Data:**
   - Load the dataset from `data.convote`.
   - Extract tuples of (Source, Target, Weight).

2. **Separating Positive and Negative Edges:**
   - Create separate DataFrames for positive and negative edges.

3. **Grouping and Summing:**
   - Group positive edges by source and target nodes, summing weights.
   - Group negative edges similarly, negating the weights.

4. **CSV Export:**
   - Export positive and negative edge DataFrames to CSV files.
   - Export node information to a CSV file.

5. **Creating Node-Link Diagrams:**
   - Two node-link diagrams are created to visually represent the network based on the nature of interactions between politicians.
     - **Positive Edges Diagram:**
       - Represents instances where a speaker is mentioned in support of another.
       - Positive edge weight implies support.
     - **Negative Edges Diagram:**
       - Represents instances where a speaker is mentioned in opposition to another.
       - Negative edge weight implies opposition.

## Importing Graph Files to Gephi

1. **Install Gephi:**
   - Download and install Gephi from [Gephi's official website](https://gephi.org/).

2. **Importing Positive Edges:**
   - Open Gephi.
   - File > Open Project > Select `positive_edges.gephi`.
   - Explore and visualize positive edges using various layout algorithms.

3. **Importing Negative Edges:**
   - Open Gephi.
   - File > Open Project > Select `negative_edges.gephi`.
   - Explore and visualize negative edges using various layout algorithms.

Feel free to explore different layout algorithms in Gephi to understand the network structure better.

