

Tenets of Go from https://go.dev/talks/2013/bestpractices.slide
- simple
- readable
- maintainable


Write everything or nothing



- Check for errors before calling defer something.Close() because something will be nil if there is an error, resulting in a segfault

