# libc Wishlist

1. A variant of `asprintf` that also takes a buffer size, so can reuse/`realloc` an existing buffer, like `getline` can do
2. `open_memstream` to be backed by `memfd_create` when available, so that `fileno` will work on it
