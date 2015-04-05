Use this command for build image:

    $ docker build --no-cache --force-rm -t juev/ruby -f Dockerfile .

Run image:

    $ docker run --rm -v $(pwd):/srv/work -p 127.0.0.1:4000:4000 juev/ruby bundle install
    $ docker run --rm -v $(pwd):/srv/work -p 127.0.0.1:4000:4000 juev/ruby rake

Default location for gems:

    ./vendor/bundle
