# 06 – Python Monitoring and Automation Scripts

## 1. Objective

Python scripts were developed to add lightweight monitoring capabilities to the infrastructure and Restic backup environment.

The objective is to automate basic checks and make monitoring information easier to consult.

## 2. Python Environment

The scripts use Python 3 and the `psutil` library.

Dependencies are listed in `requirements.txt`.

Installation:

```bash
python3 -m venv venv
source venv/bin/activate
python -m pip install -r requirements.txt
```

## 3. System Resource Monitoring

`system_monitor.py` uses `psutil` to collect:

- CPU utilization.
- RAM utilization.
- Disk utilization.

The script compares the collected values against predefined thresholds:

| Resource | Threshold |
|---|---:|
| CPU | 80% |
| RAM | 85% |
| Disk | 85% |

It displays the monitoring status and returns a non-zero exit code when a threshold is reached.

## 4. Restic Snapshot Monitoring

`backup_monitor.py` checks access to the Restic repository and retrieves the available snapshots in JSON format.

It displays:

- Total number of snapshots.
- Latest snapshot identifier.
- Latest backup date.
- Associated hostname.

This script checks snapshot availability. It does not replace the Restic integrity check or restoration test.

## 5. Project Files

- [`system_monitor.py`](../../scripts/python/system_monitor.py)
- [`backup_monitor.py`](../../scripts/python/backup_monitor.py)
- [`requirements.txt`](../../scripts/python/requirements.txt)

## 6. Evidence

The following screenshots document the Python environment, dependency installation and script execution:

- [Python environment](../../scripts/python/01-python-environnement.png)
- [psutil installation](../../scripts/python/02-psutil-installation.png)
- [System monitor execution](../../scripts/python/03-system-monitor.png)
- [Backup monitor execution](../../scripts/python/04-backup-monitor.png)
- [Python project files](../../scripts/python/05-python-project-files.png)
- [Backup monitor script](../../scripts/python/Script-backup-monitor.png)

## 7. Conclusion

These scripts provide additional monitoring functions to the lab. They complement Zabbix and Restic by offering simple command-line checks for system resources and backup snapshot availability.
