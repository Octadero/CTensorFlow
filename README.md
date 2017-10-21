# CTensorFlow
TensorFlow C Bindings for Swift

## Using CTensorFlow
Add that dependency to your Package.swift file.
That module makes bridge to libtensorflow library.
```
let package = Package(
	name: "YourProject",
	dependencies: [
		.package(url: "git@github.com:Octadero/CTensorFlow.git", from: "0.1.6")
	]
)
```

### Linux 
On Linux OS you could install library from [sources](https://www.tensorflow.org/install/install_c) or using apt package manager.

### mac OS
On mac OS you could install library from [sources](https://www.tensorflow.org/install/install_c) or using [brew](https://brew.sh) package manager.

### PkgConfig
*In case, installing from sources:*
To make interaction more easy, copy `tensorflow.pc` file to your pkgconfig folder. That is way to avoid setting all compile flags at build phase.  

Before that, set *tensorflow_path* property in `tensorflow.pc` file to your tensorflow library path.

```
sudo copy tensorflow.pc /usr/local/lib/pkgconfig/
```

### Troubleshooting
If you use apt or brew package manager, make shure that your `tensorflow.pc` file contains only [whitelisted flags](https://github.com/apple/swift-package-manager/blob/740b6667d8dfbea579927045c038d2d885543316/Sources/PackageLoading/Module%2BPkgConfig.swift#L159).
