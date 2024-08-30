# Segment-Routing-using-DRL

## Introduction

In today's increasingly complex and interconnected world, the efficient management of network traffic is crucial for ensuring optimal performance and reliability. As networks grow in size and complexity, traditional methods of routing and traffic management often fall short, necessitating the development of more advanced and intelligent solutions. This project presents a comprehensive approach to network optimization using advanced techniques, including Network Simulation, Deep Reinforcement Learning (DRL), and Machine Learning (ML) algorithms.

The primary objective of this project is to develop a tool that optimizes network traffic routing by selecting the most efficient paths through a network. This involves training models to predict the optimal number of middle points in Segment Routing (SR) and testing these predictions in various network configurations. The project leverages the power of Python libraries like NetworkX for network simulation, and PyTorch for implementing DRL models, ensuring a robust and scalable solution.

This documentation provides an in-depth exploration of the tool's functionality, the methodologies employed, and the results achieved. From loading and analyzing network topologies to training and evaluating machine learning models, the document serves as a comprehensive guide for users and developers alike. Whether you're a researcher, network engineer, or data scientist, this guide aims to equip you with the knowledge and tools needed to optimize network traffic effectively.

## Getting Started

### Prerequisites

Before you begin, ensure you have met the following requirements:

- **Python 3.8.10**: This project requires Python version 3.8.10. You can download and install it from the official [Python website](https://www.python.org/downloads/release/python-3810/).
- **pip**: Python package installer, usually included with Python.

### Setting Up the Environment

1. **Clone the Repository**

   First, clone the project repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/Segment-Routing-using-DRL.git
   cd Segment-Routing-using-DRL

   python3.8 -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`

   pip install -r requirements.txt

   pip install jupyter notebook
   pip install networkx
   pip install torch  # Or `pip install torch==version_number` for a specific version
   pip install numpy
   pip install matplotlib

## System Architecture
The system is composed of several key modules, each designed to perform specific tasks in the network optimization process. The main components include:

**Data Extraction: This module handles the efficient extraction of relevant data from specified datasets, ensuring flexibility in data handling by employing robust algorithms.
**Network Topology Creation: Using Python-based network simulation techniques, this module constructs network topologies from the extracted data, defining the structural framework of the network.
**Flow Demand Routing: This module focuses on routing flows through the network efficiently, integrating middle points within the network to enhance flow routing efficiency.
**Performance Evaluation: This module assesses the performance of routing algorithms and the impact of middle point selections on network efficiency.
**Deep Reinforcement Learning (DRL) Integration: The core of the system, this module leverages PyTorch to implement DRL models that predict and optimize flow placements within the network.

## Deep Reinforcement Learning (DRL) Overview
The DRL module plays a critical role in optimizing network routing by dynamically selecting the most efficient paths. Here's an overview of how DRL is implemented:

** DRL Model: The project employs a Deep Reinforcement Learning model designed using PyTorch. The model is trained to optimize the selection of middle points in the network based on traffic flow data.
** Training Process: The model is trained on historical network data to predict the optimal number of middle points that should be used in different network configurations. The training process involves preprocessing input data, defining the DRL model architecture, and using optimization algorithms such as Adam to update model parameters.
** Testing and Evaluation: After training, the model is tested on new network configurations to evaluate its performance. The evaluation process includes testing with and without middle points to compare the effectiveness of the DRL model in optimizing network flow.

## Implementation Details
** Programming Language: Python was used for the implementation, leveraging its extensive libraries for network simulation (NetworkX), data visualization (Matplotlib), and machine learning (PyTorch).
** Code Structure: The project is organized into modules for network simulation, machine learning simulation, and DRL model training and testing. The code is modular, allowing for easy extension and maintenance.

## Use Cases and Limitations
The tool is designed to address specific use cases such as congestion control and optimal resource utilization. While the DRL model shows promising results, there are limitations that need to be addressed, such as improving the accuracy of predictions in dynamic network environments.
## Loading Topologies
The tool allows users to work with predefined network topologies stored in text files. These files contain information about nodes, edges, and their respective weights, which are loaded into the tool for analysis. Ensure that your topology files adhere to the specified format: nodes are listed first, followed by edges and their weights.

## Setting Flow Demands
Once a topology is loaded, you can set up flow demands, which represent the volume of traffic between specific source and destination nodes. These can be configured manually or generated randomly within the tool, allowing for the simulation of various network scenarios.

## Running Optimization
The core of the tool is its optimization engine, which uses a sequential routing algorithm to determine the most efficient paths through the network. The algorithm dynamically selects middle points based on their betweenness centrality and tests routing configurations with increasing numbers of middle points. Results include success counts for various configurations and the corresponding routing paths.

## Advanced Features
Advanced users can access additional features to customize the optimization process. These include adjusting parameters for the routing algorithms, convergence criteria, and optimization strategies. The tool also offers a command-line interface (CLI) for automated batch processing, making it suitable for integration into larger workflows.

## Troubleshooting and Support
If you encounter issues while using the tool, refer to the troubleshooting section for solutions to common problems. For further assistance, you can engage with the community on the project's forum or contact the development team directly via email.

## Contributing
Contributions to this project are welcome! If you'd like to contribute, please fork the repository and submit a pull request with your changes. Ensure that your code follows the project's coding standards and includes appropriate tests.


