<p align="center">
    <h2 align="center">Indigo Minimalist Jekyll Template - <a href="https://sergiokopplin.github.io/indigo/">Demo</a></h2>
</p>

<p align="center">This is a simple and minimalist template for Jekyll for those who likes to eat noodles.</p>

***

<p align="center">
    <b><a href="README.md#what-has-inside">What has inside</a></b>
    |
    <b><a href="README.md#setup">Setup</a></b>
    |
    <b><a href="README.md#settings">Settings</a></b>
    |
    <b><a href="README.md#how-to">How to</a></b>
</p>



<p align="center">
    Light and Dark themes.
</p>


## Setup

0. :star: to the project. :metal:
1. Fork the project [Indigo](https://github.com/sergiokopplin/indigo/fork)
2. Edit `_config.yml` with your data
3. Write some posts :bowtie:

To run locally do the following:

1. Install [Jekyll](https://jekyllrb.com) and [Bundler](https://bundler.io/).
2. Clone the forked repo on your machine
3. Enter the cloned folder via terminal and run:
```sh
bundle install
bundle exec jekyll serve
```

4. Open it in your browser: [http://localhost:4000](http://localhost:4000)


5. To build:

```
bundle exec jekyll build
```


## Docker

```
docker compose build
docker compose up -d
cd _site/
zip -r ../site.zip *
```