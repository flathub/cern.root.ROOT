The package only creates a link to "root", to access another utility within 
the package as long as it is in the PATH environment variable, it can be executed,

flatpak run --command=utility cern.root.ROOT

or open a shell session by passing "sh",

flatpak run --command=sh cern.root.ROOT

If the permissions granted to the package do not meet your needs (such as file system
access), you can always modify them to your liking.
