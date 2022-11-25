# Book Searcher

[![GitHub stars](https://img.shields.io/github/stars/zu1k/book-searcher)](https://github.com/zu1k/book-searcher/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/zu1k/book-searcher)](https://github.com/zu1k/book-searcher/network)
[![Release](https://img.shields.io/github/release/zu1k/book-searcher)](https://github.com/zu1k/book-searcher/releases)
[![GitHub issues](https://img.shields.io/github/issues/zu1k/book-searcher)](https://github.com/zu1k/book-searcher/issues)
[![GitHub license](https://img.shields.io/github/license/zu1k/book-searcher)](https://github.com/zu1k/book-searcher/blob/master/LICENSE)

## Usage

### 1. Download the pre-compiled binary from [Release](https://github.com/zu1k/book-searcher/releases).

Or you can compile by yourself.

### 2. Create the index.

Or you can make your own via `bin/index.rs`.

It should look like the following:

```
project_dir
├── index
│   ├── some index files...
│   └── meta.json
└── book-searcher
```

### 3. Run `book-searcher`, it will listen to `127.0.0.1:7070`.

Access http://127.0.0.1:7070/ to use webui, or you can use the original api.

#### original search api

You can search by the following fields:

- title
- author
- publisher
- extension
- language
- isbn
- id

Examples:

- `http://127.0.0.1:7070/search?limit=30&query=余华`
- `http://127.0.0.1:7070/search?limit=30&query=title:机器学习 extension:azw3 publisher:清华`
- `http://127.0.0.1:7070/search?limit=30&query=id:18557063`
- `http://127.0.0.1:7070/search?limit=30&query=isbn:9787302423287`

## Raw data

```
id, title, author, publisher, extension, filesize, language, year, pages, isbn, ipfs_cid
```

## License

**book-searcher** © [zu1k](https://github.com/zu1k), Released under the [MIT](./LICENSE) License.<br>
