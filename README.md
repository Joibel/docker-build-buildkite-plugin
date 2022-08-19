# Docker Build

Builds one docker image and pushes it to a repository, using docker.

`key`: The Buildkite pipeline key for the generated step. Defaults to build. Must be set if this plugin is used multiple times in a single pipeline.
`label`: Label for generated step. Defaults to Build.
`arn_role`: Full role to run this operation with. Must be able to read the old tag's manifest and create a new image with that manifest.
`ecr_url`: DNS entry of ECR
`repository`: ECR repository name
`tag`: The tag you'd like to use for this image.
`path`: The path to the Dockerfile you'd like to use. Defaults to .
`docker_extra_args`: (Optional). Extra arguments to pass to docker.

This plugin injects a new step into your pipeline immediately after it has executed to perform this operation.
