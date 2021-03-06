# quartus-lite

Quartus Lite Docker for MiSTer core development.

Since MiSTer has standardized on Quartus 17.0, this installs that version with support for the Cyclone V FPGA on the DE10-Nano board used by the MiSTer project.

For Mac OS X users, I included a `quartus` shell script, which allows execution of e.g. `quartus_sh` inside the docker container. The current working directory is mounted to `/build`. 

Example:
```
quartus quartus_sh --flow compile my.qpf
```
`quartus_sh` command is executed in the current working directory. 
Just copy `quartus_sh` to a directory in your `PATH`.

Environment variables:
- `JTAG_SERVER`: allows setting a server for remote programming
- `JTAG_PASSWD`: allows setting a server password for remote programming
