+++
title = "Pom Utility for Rust"
description = "Rust module for reading Maven Poms."
date = 2021-09-06

[taxonomies]
categories = ["Projects"]
tags = ["rust", "maven"]

[extra]
toc = false
comments = true
+++

[Pom Utility for Rust](https://github.com/iambort/pom-util) is a Rust module that can be used to read maven poms. The reason for creating this utility is I wanted to read certain attributes from Maven POMs without having to run a full JVM docker container. The eventual goal is to support variable interpolation and to be able to evaluate the effective POM when multiple parents are in the hierarchy. 

This project makes use of [serde](https://crates.io/crates/serde) and [quick-xml](https://crates.io/crates/quick-xml) to parse the xml into structs in Rust. Additionally, the project uses the [rstest](https://crates.io/crates/rstest) crate to add parameterized integration tests.