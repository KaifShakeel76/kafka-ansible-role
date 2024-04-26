# Ansible Role: Kafka

An Ansible role for installing and configuring Apache Kafka.

## Requirements

This role requires Ansible installed on the control node and the target machines must have access to the internet to download Kafka.

## Role Variables

Available variables are listed below, along with their default values (see `defaults/main.yml`):

- `kafka_group`: The group name for the Kafka user. Default is `kafka`.
- `kafka_user`: The Kafka user name. Default is `kafka`.
- `kafka_create_user_group`: Boolean flag indicating whether to create the Kafka user and group. Default is `true`.
- `kafka_version`: The version of Kafka to install. Default is `2.8.0`.
- `kafka_scala_version`: The Scala version for Kafka. Default is `2.13`.
- `kafka_download_base_url`: The base URL for downloading Kafka. Default is `https://downloads.apache.org/kafka`.
- `kafka_download_validate_certs`: Boolean flag indicating whether to validate SSL certificates when downloading Kafka. Default is `yes`.
- `kafka_root_dir`: The root directory where Kafka will be installed. Default is `/opt`.
- `kafka_dir`: The directory where Kafka will be installed. Default is `{{ kafka_root_dir }}/kafka`.
- `kafka_data_log_dirs`: Comma-separated list of directories for Kafka data log files. Default is `/var/lib/kafka/data`.
- `kafka_log_dir`: The directory for Kafka application logs. Default is `/var/log/kafka`.
- `kafka_unit_path`: The path for Kafka systemd service unit file. Default is `/etc/systemd/system/kafka.service`.
- `kafka_start`: Boolean flag indicating whether to start Kafka service. Default is `true`.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: ansible-kafka
```

## License

MIT

## Author Information

This role was created by [Your Name] for personal use.

Feel free to contribute or improve upon it!
