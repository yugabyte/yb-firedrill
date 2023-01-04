# yb-firedrill

## Let's break and learn

### Requirements

- Yugabyte Version 2.16 +
- Yugabyte Anywhere instance running on [Certified Image](https://console.cloud.google.com/compute/imagesDetail/projects/debian-cloud/global/images/debian-11-bullseye-v202212060)
    - Debian GNU/Linux, 11 (bullseye) - v20221206
    - Architecture x86/64
    - Family debian-11
- User `yugabyte` with sudo privileges.
- 3 Node universe with `systemd-enabled`
- config file name should be `config.ini` and in a working directory.

### Installation

- Just clone this repo and give execute permissions to `yb-firedrill` binary

```
git clone https://github.com/yugabyte/yb-firedrill.git
cd yb-firedrill/
chmod +x yb-firedrill
```

#### Config file

- Update the config file as per your environment and keep it in your current working directory.
- Sample config file:

        [global]
        server1_ip = 10.212.0.90
        server2_ip = 10.212.0.91
        server3_ip = 10.212.0.92
        key_path = /opt/yugabyte/yugaware/data/keys/26183b50-dec2-458a-ac03-27f8a9b2d95f/yb-dev-gcp_26183b50-dec2-458a-ac03-27f8a9b2d95f-key.pem 
        ssh_port = 54422
        tls_path = /home/yugabyte/yugabyte-tls-config/
        master_bin_path = /home/yugabyte/master/bin/
        tserver_bin_path = /home/yugabyte/tserver/bin/
        postgres_bin_path = /home/yugabyte/tserver/postgres/bin/
        pg_password = <password>

#### Usage

        usage: firedrill [-h] [--exercise EXERCISE] [--type TYPE] [--list-types]
        Run a random exercise
        optional arguments:
          -h, --help           show this help message and exit
          --exercise EXERCISE  Run a specific exercise, This will override the random exercise selection. This designed to used developers of firedrill for testing.
          --type TYPE          Run a specific type of exercise
          --list-types         List the types of exercises


#### Feedback and issues

If you have any feedback or facing any issues, You can reach us out at `#firedrill` slack channel.
