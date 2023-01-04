---
tags: a/note
---
in:: [[technology]]

# Notes
QNAP NAS
* [QNAP (US)](https://www.qnap.com/en-us)

## TBS-464 review
* [TBS-464 | QNAP (US)](https://www.qnap.com/en-us/product/tbs-464)
* [TBS-464 manuals](https://www.qnap.com/en-us/download?model=tbs-464&category=documents)
* 4-drive NAS using M.2 2280 SSD drives
* Small and quiet while still as powerful as larger units
* Note: M.2 2280 drives have at least two different connectors. See [M.2 Drives](https://github.com/digitalreplica/technology/blob/main/computer_hardware.md#m2-drives).

## Migrating shared folders between two NAS devices
This assumes copying data between old and new NAS, not physically moving drives.
* Setup new NAS. Configure storage.
* Create the shared folders on the new NAS that you want to migrate
* On the new NAS, install "HBS 3 Hybrid Backup Sync" app
  * Enable RTRR server and set password
* On the old NAS, install Hybrid Backup Sync app
  * Create one-way sync job, "Sync Local to Remote"
