# Java Accelerator - Function Buildpacks for Knative

This accelerator generates template files, which enable developers to work with Function Buildpacks
and deploy a FaaS experience easily.

These template files are generated from VMware's open-source [Function Buildpacks for Knative](https://github.com/vmware-tanzu/function-buildpacks-for-knative) project. 

## Getting Started

To begin editing your function, refer to the tree diagram below of the file to modify:
```
functions-java
└── src/main/java/functions
    └── Handler.java // EDIT THIS FILE
```

Inside this file, you will find a function that is invoked by default. For example:
```
@Bean
public Function<String, String> hello() {
	return in -> "Hello " + in; // YOUR CODE HERE
}
```

You may replace the code inside this default function with your logic.

To see samples of code deployable as a Function (FaaS) experience, visit the [samples folder](https://github.com/vmware-tanzu/function-buildpacks-for-knative/tree/main/samples/java).

### Implementation Details (FAQ)
To add/remove dependencies, you may use Maven or Gradle for dependency management as with any normal Java / Spring development.

If you would prefer to use Spring's CloudEvent package, you may use the `org.springframework.cloud.function.cloudevent.CloudEventMessageBuilder` instead of the default `io.cloudevents.core.builder.CloudEventBuilder` import.

Instead of arguments in the function definition, the `in` object has attributes that can be populated and accessed.

## Deploying
Please see [DEPLOYING.md](DEPLOYING.md) on how to build, deploy, and test your newly built function.

## Links

### Contributing
* [Contributing Guide](https://github.com/vmware-tanzu/function-buildpacks-for-knative/blob/main/CONTRIBUTING.md)

### License
* [BSD-2 License](https://github.com/vmware-tanzu/function-buildpacks-for-knative/blob/main/LICENSE)

### Reporting Bugs or Vulnerabilities
* [Bugs, Issues, Missing Features](https://github.com/vmware-tanzu/function-buildpacks-for-knative/issues/)
* [Only Vulnerabilities](https://github.com/vmware-tanzu/function-buildpacks-for-knative/blob/main/SECURITY.md)
