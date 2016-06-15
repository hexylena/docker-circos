# Circos Docker Container

This is a containerized circos. For more information on circos please visit the [Circos website] (http://circos.ca). The website has an easy to use and excellent interface for quick entry of data in tabular form and automated generation of very simple, elegant circos graphs. For many applications however, the installation can be fairly involved, even for linux users. Therefore having a preconfigured container with circos installed is very convenient.

To use this container, I recommend mounting a local data volume at runtime and interactively running your circos config script. As an example, at the docker prompt, run:

    docker run -it -v $(pwd)/example:/input circos -conf /input/circos.conf

In this case, the example directory contains **_all_** files necessary to compile your circos image, including data and configuration.
