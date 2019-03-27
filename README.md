### using jenkinsfilext command

```
Usage:
  jenkinsfilext [command]

Available Commands:
  help        Help about any command
  validate    validate some resources
  version     Print the version number of jenkinsfilext

Flags:
  -h, --help   help for jenkinsfilext
```

validate template definition
```
validate some resources

Usage:
  jenkinsfilext validate [command]

Available Commands:
  definition  validate resource definition

Flags:
  -h, --help   help for validate
```

```
Usage:
  jenkinsfilext validate definition [flags]

Flags:
  -d, --dir string         provider the pipeline template repository directory that want to be validate
  -f, --file stringArray   provider the file path that want to be validate
  -h, --help               help for definition
```


#### Examples
validate template repository

```
jenkinsfilext validate definition  -d ./pipeline-templates

// OutPut -----
// √        pipeline-templates/definition/pipelines/alaudaBuildImage/pipeline.yaml
// √        pipeline-templates/definition/pipelines/alaudaBuildImage&DeployService/pipeline.yaml
// √        pipeline-templates/definition/pipelines/alaudaDeployService/pipeline.yaml
// √        pipeline-templates/definition/tasks/alaudaBuildImage/task.yaml
// √        pipeline-templates/definition/tasks/alaudaDeployService/task.yaml
// √        pipeline-templates/definition/tasks/clone/task.yaml
```

validate template file
```
jenkinsfilext validate definition  -f ./pipeline-templates/definition/pipeline/alaudaBuild/alaudaBuild.yaml

// OutPut ----
// √        ./pipeline-templates/definition/pipelines/alaudaBuildImage&DeployService/pipeline.yaml
```
