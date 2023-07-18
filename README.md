## Installation 
 1. Clone this repository, cd into scripts folder. Modify chmode and move kubeplugin with this commands:
 ```bash
    sudo chmod +x ./kubectl-kubeplugin
    sudo mv ./kubectl-kubeplugin /usr/local/bin
   ```
## Usage
- The script expects the namespace as the first argument and the resource type as the second argument when invoking the script. For example: $ kubectl kubeplugin <namespace> <resource-type>.

- The kubectl command uses the get subcommand to retrieve the resource usage statistics.

- The namespace is passed as an argument using the -n flag to filter resources from the specified namespace.

- The output is processed using the tail command to skip the header line.

- The while loop reads each line of output and extracts the name, CPU, and memory information using awk.

 -The extracted statistics are then printed to the console.
