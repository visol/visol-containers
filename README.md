## Sitediff CLI

```shell
git submodule add https://github.com/evolvingweb/sitediff.git sitediff/1.1.1 \
&& cd sitediff/1.1.1 \
&& git checkout v1.1.1 \
&& cd ../..

git submodule add https://github.com/evolvingweb/sitediff.git sitediff/1.2.1 \
&& cd sitediff/1.2.1 \
&& git checkout v1.2.1 \
&& cd ../..
```

```shell
cd sitediff/1.1.1 \
&& docker buildx build . --platform linux/arm64/v8,linux/amd64 --tag docker.io/visol/sitediff:1.1.1 --file Dockerfile --push \
&& cd ../..

cd sitediff/1.2.1 \
&& docker buildx build . --platform linux/arm64/v8,linux/amd64 --tag docker.io/visol/sitediff:1.2.1 --file Dockerfile --push \
&& cd ../..
```

## Solr

```shell
git submodule add -b release-9.0.x https://github.com/TYPO3-Solr/ext-solr.git typo3solr/9.0.3 \
&& cd typo3solr/9.0.3 \
&& git checkout 9.0.3 \
&& cd ../..

git submodule add -b release-10.0.x https://github.com/TYPO3-Solr/ext-solr.git typo3solr/10.0.5 \
&& cd typo3solr/10.0.5 \
&& git checkout 10.0.5 \
&& cd ../..

git submodule add -b release-11.5.x https://github.com/TYPO3-Solr/ext-solr.git typo3solr/11.5.0 \
&& cd typo3solr/11.5.0 \
&& git checkout 11.5.0 \
&& cd ../..

git submodule add -b release-11.5.x https://github.com/TYPO3-Solr/ext-solr.git typo3solr/11.5.1 \
&& cd typo3solr/11.5.1 \
&& git checkout 11.5.1 \
&& cd ../..
```

```shell
cd typo3solr/9.0.3 \
&& docker buildx build . --platform linux/arm64/v8,linux/amd64 --tag docker.io/visol/typo3solr:9.0.3 --file Dockerfile --push \
&& cd ../..

cd typo3solr/10.0.5 \
&& docker buildx build . --platform linux/arm64/v8,linux/amd64 --tag docker.io/visol/typo3solr:10.0.5 --file Docker/SolrServer/Dockerfile --push \
&& cd ../..

cd typo3solr/11.5.0 \
&& docker buildx build . --platform linux/arm64/v8,linux/amd64 --tag docker.io/visol/typo3solr:11.5.0 --file Docker/SolrServer/Dockerfile --push \
&& cd ../..
```

## Redis Commander

```shell
git submodule add https://github.com/joeferner/redis-commander.git redis-commander/0.8.0 \
&& cd redis-commander/0.8.0 \
&& git checkout v0.8.0 \
&& cd ../..
```

```shell
cd redis-commander/0.8.0 \
&& docker buildx build . --platform linux/arm64/v8,linux/amd64 --tag docker.io/visol/redis-commander:0.8.0 --file Dockerfile --push \
&& cd ../..
```

## Beanstalkd

```shell
git submodule add https://github.com/beanstalkd/beanstalkd.git beanstalkd/1.12 \
&& cd beanstalkd/1.12 \
&& git checkout v1.12 \
&& cd ../..
```

```shell
cd beanstalkd/1.12 \
&& git checkout master -- Dockerfile .dockerignore \
&& docker buildx build . --platform linux/arm64/v8,linux/amd64 --tag docker.io/visol/beanstalkd:1.12 --file Dockerfile --push \
&& cd ../..
```