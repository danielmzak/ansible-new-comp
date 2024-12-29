# Running the Playbook

- Install Ansible: `sudo apt update && sudo apt install ansible`
- Navigate to your project directory: `cd ubuntu-laptop-setup`
- Run: `ansible-playbook -i inventory.ini playbook.yml -K -vvv`
- `-K` will prompt for the sudo password.
- `-vvv` verbose mode, useful for debug

---

## Key Considerations

- Idempotency: Ansible roles and tasks are designed to be idempotent. This means you can run the playbook multiple times, and it will only make changes if needed.
- Error Handling: Add failed_when conditions to tasks to handle potential errors gracefully.
- Testing: Consider using a virtual machine to test your playbook before running it on your actual laptop.
- Version Control: Store your Ansible code in a Git repository to track changes and collaborate effectively.

### Security:

- Avoid hardcoding sensitive information (passwords, API keys) directly in your playbooks. Use Ansible Vault or environment variables.
- Regularly update your system and Ansible to patch security vulnerabilities.
- Modularity: As your setup grows, break down roles into smaller, more manageable tasks.
- This comprehensive structure provides a solid foundation for automating your Ubuntu laptop installation with Ansible. Remember to customize the vars files with your specific applications and preferences. Good luck!