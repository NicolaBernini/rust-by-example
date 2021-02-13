# Rust By Example

[![Build Status][travis-badge]][travis-repo]

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/NicolaBernini/rust-by-example/HEAD)

[travis-badge]: https://travis-ci.com/rust-lang/rust-by-example.svg?branch=master
[travis-repo]: https://travis-ci.com/rust-lang/rust-by-example

Learn Rust with examples (Live code editor included)

## Quick Rust Installation 

```bash
curl https://sh.rustup.rs -sSf | sh
```

## Using

If you'd like to read Rust by Example, you can visit <https://doc.rust-lang.org/rust-by-example/>
to read it online.

If you'd like to read it locally, [install Rust], and then:

```bash
$ git clone https://github.com/rust-lang/rust-by-example
$ cd rust-by-example
$ cargo install mdbook
$ mdbook build
$ mdbook serve
```

[install Rust]: https://www.rust-lang.org/tools/install

To be able to run the examples, you must be connected to the internet; you can
read all content offline, however!



## Run it on Binder 

Before starting, I am assuming you have an [Ngrok](https://ngrok.com/) token 

1. Go to [MyBinder](https://mybinder.org/)
2. Launch MyBinder with this repo 
3. Open a console 
4. Install Rust 

```bash
curl https://sh.rustup.rs -sSf | sh
```


5. Install ngrok

```bash
pip install pyngrok
ngrok help
```


6. Build the book 

```bash
mdbook build
```


7. Serve the book 

```bash
mdbook serve & 
```

This should serve the book at http://localhost:3000/ but since it is localhost you can't access it directly, you need to build a tunnel to a public IP and for this we use ngrok 


8. Run the ngrok tunneling 

```bash
ngrok http 3000
```

You should see something like 

```bash
ngrok by @inconshreveable                                                                                  (Ctrl+C to quit)

Session Status                online
Account                       Nicola Bernini (Plan: Free)
Version                       2.3.35
Region                        United States (us)
Web Interface                 http://127.0.0.1:4040
Forwarding                    http://9f3348fc6ce7.ngrok.io -> http://localhost:3000
Forwarding                    https://9f3348fc6ce7.ngrok.io -> http://localhost:3000

Connections                   ttl     opn     rt1     rt5     p50     p90
                              38      0       0.00    0.01    1.61    17.29
```



9. Access the book by connecting to the link 

For example 

http://9f3348fc6ce7.ngrok.io/variable_bindings/scope.html

and in the ngrok logs you should see something like 


```bash
HTTP Requests
-------------

GET /favicon.svg                                   200 OK
GET /favicon.png                                   200 OK
GET /fonts/open-sans-v17-all-charsets-italic.woff2 200 OK
```


## Contributing

Please see the [CONTRIBUTING.md] file for more details.

[CONTRIBUTING.md]: https://github.com/rust-lang/rust-by-example/blob/master/CONTRIBUTING.md

## Translations to other languages

* [Chinese](https://github.com/rust-lang-cn/rust-by-example-cn)
* [Japanese](https://github.com/rust-lang-ja/rust-by-example-ja)
* [French](https://github.com/Songbird0/FR_RBE)
* [Russian](https://github.com/ruRust/rust-by-example)

## License

Rust by Example is licensed under either of

* Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
  <http://www.apache.org/licenses/LICENSE-2.0>)
* MIT license ([LICENSE-MIT](LICENSE-MIT) or
  <http://opensource.org/licenses/MIT>)

at your option.

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in Rust by Example by you, as defined in the Apache-2.0 license, shall be
dually licensed as above, without any additional terms or conditions.
