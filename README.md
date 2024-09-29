# Execute commands inside the sandbox

The package only creates a link to "root", to access another utility within 
the package as long as it is in the PATH environment variable, it can be executed,

- flatpak run --command=utility cern.root.ROOT

or open a shell session by passing "sh",

- flatpak run --command=sh cern.root.ROOT

If the permissions granted to the package do not meet your needs (such as file system
access), you can always modify them to your liking.

# Install Jupyter notebooks

To install Jupyter in the isolated environment, you have to enter the container,

- flatpak run --devel --command=sh cern.root.ROOT

At this point you cannot alter the contents of the package located in /app, so the installation is done for the user,

- pip install --user jupyter
- pip install --user metakernel

and to run inside the container,

- root --notebook

or from outside,

- flatpak run cern.root.ROOT --notebook
