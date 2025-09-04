# AnyBlox

<img src="anyblox-logo.svg" alt="AnyBlox Logo" width="200" align="right">

**AnyBlox is a framework for reading arbitrary datasets using lightweight WebAssembly decoders bundled with the data.**

We continuously develop better encodings and compression schemes for data, but your datasets are stuck on using whatever your query engine supports reading. We propose a different paradigm for data encodings – making datasets decode themselves.

AnyBlox is build around four pillars: **Portability**, **Security**, **Performance**, and **Extensibility**.

## For System Developers

When you build a new data system you need to write code for reading datasets in all formats you want to support separately. Parquet, ORC, JSON, The Hot New Thing&trade; &ndash; each requires time, effort, and creates a maintenance burden. With AnyBlox, **you only need one reader**. Enabling AnyBlox in your system is easy and immediately allows you to read any future dataset with an AnyBlox decoder.

To prove ease-of-use, we implemented AnyBlox into:

- [DuckDB](https://github.com/AnyBlox/duckdb-anyblox),
- [DataFusion](https://github.com/AnyBlox/anyblox/tree/main/anyblox-datafusion),
- [Umbra](https://github.com/AnyBlox/umbra-anyblox), and
- [Spark](https://github.com/AnyBlox/spark-anyblox).

In all cases, the integration takes just a few hundred lines of code and gives you access to cutting-edge data formats like [Vortex](https://github.com/spiraldb/vortex),
exotic, domain-specific formats like [ROOT](https://root.cern/), or even instance-optimised encodings tailored to your data.

## For Format/Encoding Developers

Once you create your new, world-changing data format, you're only a step away from having it immediately readable by any system &ndash; just compile the decoder into WebAssembly! AnyBlox requires one simple exported function and it takes everything from there. Our framework allows you to seamlessly share memory with the decoder sandbox and thus makes your data portable, secure, and efficient to decode.

## Usage

Head to the main [anyblox repository](https://github.com/AnyBlox/anyblox) to use our library, or integrate one of our extensions for existing data systems ([DuckDB](https://github.com/AnyBlox/duckdb-anyblox),
[DataFusion](https://github.com/AnyBlox/anyblox/tree/main/anyblox-datafusion),
[Spark](https://github.com/AnyBlox/spark-anyblox)).

## Best Paper of VLDB2025

Our paper was voted the Best Paper at VLDB 2025! [You can read it here](https://gienieczko.com/anyblox-paper).
