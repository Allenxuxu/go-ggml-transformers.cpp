# [![Go Reference](https://pkg.go.dev/badge/github.com/go-skynet/go-ggml-transformers.cpp.svg)](https://pkg.go.dev/github.com/go-skynet/go-ggml-transformers.cpp) go-ggml-transformers.cpp

[ggml](https://github.com/ggerganov/ggml) golang bindings to run transformers.

The go-llama.cpp bindings are high level, as such most of the work is kept into the C/C++ code to avoid any extra computational cost, be more performant and lastly ease out maintenance, while keeping the usage as simple as possible. 

Check out [this](https://about.sourcegraph.com/blog/go/gophercon-2018-adventures-in-cgo-performance) and [this](https://www.cockroachlabs.com/blog/the-cost-and-complexity-of-cgo/) write-ups which summarize the impact of a low-level interface which calls C functions from Go.

If you are looking for an high-level OpenAI compatible API, check out [here](https://github.com/go-skynet/LocalAI).

## Usage

Note: This repository uses git submodules

Clone the repository locally:

```bash
git clone --recurse-submodules https://github.com/go-skynet/go-ggml-transformers.cpp
```

To build the bindings locally, run:

```
cd go-ggml-transformers.cpp
make libtransformers.a
```

Now you can run the example with:

```
LIBRARY_PATH=$PWD C_INCLUDE_PATH=$PWD go run ./examples -m "/model/path/here" -t 14
```

Enjoy!

The documentation is available [here](https://pkg.go.dev/github.com/go-skynet/go-ggml-transformers.cpp) and the full example code is [here](https://github.com/go-skynet/go-ggml-transformers.cpp/blob/master/examples/main.go).

## License

MIT
