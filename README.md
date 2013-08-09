Magic cURL
==========

Magic cURL is a simple caching wrapper around the `curl` command. 
It can be placed before the real `curl` command in the $PATH to cache downloaded files so they can be subsequently downloaded faster.

Usage
-----

To use Magic cURL, place its `/bin` dir before the real `curl` command in your $PATH. For example:

    export PATH=/usr/bin/local/magic_cache/bin:$PATH

Once this is set, use the `curl` command like you normally would. Magic cURL will automatically forward all arguments to the real `curl` command if a local copy is not found in the cache.

The cache location defaults to `/tmp/magic_curl_cache`, but can be changed by setting the `MAGIC_CURL_CACHE` env var.

Run `magic-curl-cache-clear` to clear the cache. 
