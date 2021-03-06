<!-- Code generated from the comments of the ToolsConfig struct in builder/parallels/common/tools_config.go; DO NOT EDIT MANUALLY -->

-   `parallels_tools_guest_path` (string) - The path in the virtual machine to
    upload Parallels Tools. This only takes effect if parallels_tools_mode
    is "upload". This is a configuration
    template that has a single
    valid variable: Flavor, which will be the value of
    parallels_tools_flavor. By default this is "prl-tools-{{.Flavor}}.iso"
    which should upload into the login directory of the user.
    
-   `parallels_tools_mode` (string) - The method by which Parallels Tools are
    made available to the guest for installation. Valid options are "upload",
    "attach", or "disable". If the mode is "attach" the Parallels Tools ISO will
    be attached as a CD device to the virtual machine. If the mode is "upload"
    the Parallels Tools ISO will be uploaded to the path specified by
    parallels_tools_guest_path. The default value is "upload".
    