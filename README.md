The flame projects are set up as separate, individual projects. This 
means you can check out a single project, build it and work on it.

If you want to work on multiple dependent projects at the same time, put all of
them in the same project root and copy the "settings.gradle" and "build.gradle"
files to the root of your project tree, like this:

project-root/
- build.gradle
- settings.gradle
- flame-compiler/
- treemarker/

You can now build all projects at once by going to the project root and typing
```
gradle build
```

Since the project root already contains other git repositories, make sure you 
COPY build.gradle and settings.gradle into your project root, instead of 
checking out the whole flame-parent git repository. The latter would cause the
other git repositories to be nested inside the flame-parent git repository,
which wouldn't work well.
