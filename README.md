# yb-firedrill

## Let's break and learn

### Installation

Just download latest appropriate binary from releases

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

#### Usage

        usage: firedrill [-h] [--exercise EXERCISE] [--type TYPE] [--list-types]
        Run a random exercise
        optional arguments:
          -h, --help           show this help message and exit
          --exercise EXERCISE  Run a specific exercise, This will override the random exercise selection. This designed to used developers of firedrill for testing.
          --type TYPE          Run a specific type of exercise
          --list-types         List the types of exercises

#### Requirements

- 3 Node universe with `systemd-enabled`
- config file name should be config.ini

#### Feedback and issues

If you have any feedback or facing any issues, You can reach us out at `#firedrill` slack channel.
