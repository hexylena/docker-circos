This is a containerized circos. For more information on circos please visit the [Circos website] (http://circos.ca). The website has an easy to use and excellent interface for quick entry of data in tabular form and automated generation of very simple, elegant circos graphs. For many applications however, the installation can be fairly involved, even for linux users. Therefore having a preconfigured container with circos installed is very convenient.

To use this container, I recommend mounting a local data volume at runtime and interactively running your circos config script. As an example, at the docker prompt, run:

    docker run -it -v /home/myname/projects/circos_example:/root/circos_example dennishazelett/circos


In this case, the circos_example directory contains **_all_** files necessary to compile your circos image, including data and configuration. From the bash interpreter, you would change directories to the subdirectory containing your main configuration file and run

    circos -conf circos_example.conf


A working example is included with the base image.
