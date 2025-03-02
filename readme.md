# Portainer Agent Automation

This repository contains an Ansible playbook to install and configure the Portainer Agent locally on a Raspberry Pi.

## Prerequisites

- A Raspberry Pi running a Debian-based OS (e.g., Raspbian)
- Ansible installed on your local machine
- Sudo privileges on the Raspberry Pi

## Setup

1. Clone this repository to your local machine:

    ```sh
    git clone https://github.com/18visions/portainer_agent_automation.git
    cd portainer_agent_automation
    ```

2. Run the Ansible playbook to install and configure the Portainer Agent:

    ```sh
    ansible-playbook ansible/setup_portainer_agent.yaml
    ```

## Playbook Details

The Ansible playbook [setup_portainer_agent.yaml](https://github.com/18visions/portainer_agent_automation/blob/main/ansible/setup_portainer_agent.yaml) performs the following tasks:

1. Updates and installs necessary dependencies.
2. Adds the Docker GPG key.
3. Adds the Docker repository.
4. Installs Docker and its dependencies.
5. Enables and starts the Docker service.
6. Ensures the Python Docker SDK is installed via PIP.
7. Deploys the Portainer Agent container.
8. Verifies that the Portainer Agent is running.
9. Displays the Portainer Agent status.

## Usage

After running the playbook, the Portainer Agent should be running on your Raspberry Pi. You can add this node to your Portainer instance using the IP address and port `9001`:
