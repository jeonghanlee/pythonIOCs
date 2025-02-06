# pythonIOCs


## Python Local Virtual Environment

```
$ python -m venv ~/penv
source ~/penv/bin/activate
(penv) jeonglee@Neutron: pythonIOCs (master)$
(penv) jeonglee@Neutron: pythonIOCs (master)$ pip install softioc cothread
(penv) jeonglee@Neutron: pythonIOCs (master)$ python dls_ioc_example.py 
INFO: PVXS QSRV2 is loaded, permitted, and ENABLED.
Starting iocInit
############################################################################
## EPICS 7.0.7.1-DEV
## Rev. 7.0.7.99.1.1
## Rev. Date 7.0.7.99.1.1
############################################################################
iocRun: All initialization complete
Python 3.11.2 (main, Nov 30 2024, 21:22:50) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> dbl
<function ExportTest.<locals>.call_f at 0x7fc0ac60bba0>
>>> dbl()
MY-DEVICE-PREFIX:AI
MY-DEVICE-PREFIX:AO

```

```
(penv) pythonIOCs (master)$ export EPICS_CA_ADDR_LIST=localhost
(penv) pythonIOCs (master)$ export EPICS_PVA_ADDR_LIST=localhost
(penv) pythonIOCs (master)$ camonitor MY-DEVICE-PREFIX:AI
MY-DEVICE-PREFIX:AI            2025-02-06 00:49:49.136633 182
MY-DEVICE-PREFIX:AI            2025-02-06 00:49:50.138049 183
MY-DEVICE-PREFIX:AI            2025-02-06 00:49:51.139423 184

```
