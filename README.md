# Recipe Builder Solution

This project is a Recipe Builder solution that leverages Semantic Kernel and agentic AI. It includes multiple agents: the Recipe Builder Agent, the Vegan Substitution Agent, and the Gluten-Free Substitution Agent.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Agents](#agents)
  - [Recipe Builder Agent](#recipe-builder-agent)
  - [Vegan Substitution Agent](#vegan-substitution-agent)
  - [Gluten-Free Substitution Agent](#gluten-free-substitution-agent)
- [OTEL Endpoint](#otel-endpoint)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Installation

Follow these steps to get your development environment set up:

```bash
# Clone the repository
git clone https://github.com/swigerb/recipe-chat.git

# Go into the repository
cd recipe-chat

# Restore dependencies
dotnet restore
```

## Usage

To run the Recipe Builder solution:

```bash
# Run the project
dotnet run
```

## Agents

### Recipe Builder Agent

The Recipe Builder Agent assists in creating custom recipes based on user input.

### Vegan Substitution Agent

The Vegan Substitution Agent provides vegan alternatives for ingredients in recipes.

### Gluten-Free Substitution Agent

The Gluten-Free Substitution Agent suggests gluten-free substitutions for recipe ingredients.

## OTEL Endpoint

I highly recommend the .NET Aspire dashboard to create an OTEL endpoint that you can use for this solution and capture/visual monitoring.


## Running the Aspire Dashboard Locally

To run the Aspire dashboard locally, follow these steps:

1. Start the Dashboard:
   - Use the Docker command line to start the dashboard. Open your terminal and run the following command:
     ```bash
     docker run --rm -it -d -p 18888:18888 -p 4317:18889 --name aspire-dashboard mcr.microsoft.com/dotnet/aspire-dashboard:9.0
     ```
   - This command will start a container from the Aspire dashboard image and map the necessary ports.

2. Access the Dashboard:
   - Once the container is running, open your web browser and navigate to http://localhost:18888 to view the dashboard UI.

3. Login to the Dashboard:
   - The dashboard requires a token for authentication. The token is printed in the container logs. You can retrieve it by running:
     ```bash
     docker logs aspire-dashboard
     ```
   - Copy the token and use it to log in to the dashboard.

4. Send Telemetry to the Dashboard:
   - Configure your applications to send telemetry data to the dashboard using the OpenTelemetry Protocol (OTLP). The endpoint for receiving data is http://localhost:4317.

For more detailed configuration options, refer to the official documentation. https://learn.microsoft.com/en-us/dotnet/aspire/fundamentals/dashboard/standalone?tabs=bash

## Contributing

We welcome contributions from the community! To contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/feature-name`)
3. Commit your changes (`git commit -m 'Add feature'`)
4. Push to the branch (`git push origin feature/feature-name`)
5. Open a Pull Request

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact

If you have any questions or suggestions, feel free to reach out!

Author: Brian Swiger - brian@mightybs.com

Project Link: [https://github.com/swigerb/recipe-chat](https://github.com/swigerb/recipe-chat)
