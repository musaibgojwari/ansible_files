# Ansible Playbook: Install Pip and Boto3

This Ansible playbook automates the installation of Python's Pip package manager and the Boto3 library on target hosts. Boto3 is the Amazon Web Services (AWS) Software Development Kit (SDK) for Python, allowing seamless interaction with AWS services.

## Prerequisites

- Ansible installed on the control machine.
- SSH access to the target hosts.
- The target hosts should be running an apt-compatible Linux distribution (e.g., Ubuntu).

## Usage

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/your-username/ansible_files.git
    ```

2. Navigate to the project directory:

    ```bash
    cd ansible_files
    ```

3. Open the `inventory` file and replace the `hosts` value with your target hosts or group ip address.

4. Execute the Ansible playbook:

    ```bash
    ansible-playbook -i inventory ansible_file.yml
    ```

    This will install Python3 Pip on the target hosts and then install the Boto3 library using Pip.

## Customization

- Adjust the `ansible_distribution` condition in the playbook to match the target Linux distribution if it's not Ubuntu.
  
- Modify the playbook to suit your specific requirements.

## Notes

- The `become: yes` statement is used to run tasks with elevated privileges.

- Ensure that SSH access is properly configured for the target hosts.

- The playbook assumes Python3 is available on the target hosts.

**Happy automating!**
