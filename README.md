# Home Assistant Device Updates Automation Generator

This project generates the automation YAML content for updating all devices listed in the `vars.yml` file automatically at a specific time. The generated automation handles checking for available updates and performs the updates based on the schedule set by a helper.

### What it does:
- Generates the automation YAML content for updating all devices from the `vars.yml` file automatically at a specific time.
- The time is set via a schedule helper, which must be created in Home Assistant before running the playbook.

### Quickstart:

1. **Create a schedule helper** in Home Assistant, which will control when the updates are triggered.
   
2. **Create the `vars.yml` file**:
   - Copy the `vars.yml.template` file to `vars.yml`.
   - Populate `vars.yml` with your devices (lights, thermostats, plugs, etc.).

3. **Run the Ansible playbook** to generate the automation:
   ```bash
   ansible-playbook playbook.yml
   ```

4. **Copy the generated automation**:
   - After the playbook runs, a file called `generated_update_automation.yaml` will be created.
   - Copy the content of this file into the **YAML view** of a new automation in the Home Assistant UI.


