# Example Distributed Argo Workflow
## About

This is an example config for an Argo workflow that takes the contents of a mounted volume as input parameters to a dynamically generated set of jobs.  There is a parameters.json file which needs the keys of "cmd" and "file_extension" to represent the command to execute in the generated jobs and the file extension to filter for on the mounted volume.


```
argo submit -f parameters.json run_distributed_command.yaml
```

## Example parameters.json

```json
{
    "cmd": "/bin/some_bin \
            --somearg1=someval1 \
            --somearg2=someval2",
    "file_extension": ".txt"
}
```
