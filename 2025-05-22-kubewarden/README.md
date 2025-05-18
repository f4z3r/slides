# Kubewarden Brown Bag Lunch

In order to build this presentation, you will need to initialise submodules first:

```sh
git submodule init
git submodule update
```

Once this is done, you can build the slides with `pandoc` and serve them with `miniserve`. Note that
`miniserve` needs to be able to serve files within the `/assets/` directory, and should thus be
started in the root of the repository. The simplest way to achive this is to run `devbox run serve`.
