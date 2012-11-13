freeling-home
=============

This repository is a clean template to create a start-up folder for Freeling.

This are the repository contents:
```
 + /opt/freeling/
    + bin/
      - freeling.jar
      - libfreeling_javaAPI.so
    + etc/
      - custom-mappings.rdf
      - custom-rules.rdf
      - data.rdf
      - dbpedia-mappings.rdf
      - languageIdentifierConfiguration.cfg
```

# Installation

Checkout the repository in `/opt/freeling`:
```sh
git clone https://github.com/insideout10/freeling-home.git /opt/freeling
```

## bin folder

The *bin* folder contains the following files:

* freeling.jar: a support library for Java,
* libfreeling_javaAPI.so: the native counterpart of the Java library.

## etc folder

The *etc* folder contains configuration files for different engines. Most of these files will be probably moved elsewhere (custom-mappings.rdf, custom-rules.rdf, data.rdf, dbpedia-mappings.rdf).

The most important file is `languageIdentifierConfiguration.cfg` that contains the configuration for the *Freeling Language Identifier engine* for *Apache Stanbol*.

You **must** create a *symbolic link* to the *Freeling share* folder inside this folder:
```sh
ln -s /usr/local/share/freeling /opt/freeling/etc/freeling
```