# osm4routing2

This project is a rewrite in rust from https://github.com/Tristramg/osm4routing

It converts an OpenStreetMap file (in the `.pbf` format) into a CSV file.

## Build
Get a rust distribution with `cargo`: https://www.rust-lang.org/en-US/downloads.html

Run `cargo install osm4routing`

You can now use `osm4routing <some_osmfile.pbf>` to generate the `nodes.csv` and `edges.csv` that represent the road network.

If you prefer running the application from the sources, and not installing it, you run

`cargo run --release -- <path_to_your_osmfile.pbf>`

The identifiers for nodes and edges are from OpenStreetMap. That means that edges id can be duplicated.

## Importing in a database

If you prefer having the files in database, you can run the very basic `import_postgres.sh` script.

It supposes that a database `osm4routing` exists (otherwise modify it to your needs).
