# Debug Examples

- Set handlign error and trap error:

    ```bash
    #!/usr/bin/env bash
    set -e # This instructs bash to stop the execution of this script as soon as it encounters an error

    error_report() {
        echo -e "\nERROR ($(date)): Command execution error found on line $1"
    }

    trap 'error_report $LINENO' ERR

    echo all is good
    echot "This command is incorrect and won't run"
    ```
