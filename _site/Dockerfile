FROM ruby:3.1-slim-bullseye as jekyll

RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    git \
    && rm -rf /var/lib/apt/lists/*

# used in the jekyll-server image, which is FROM this image
COPY docker-entrypoint.sh /usr/local/bin/

RUN gem update --system && gem install jekyll && gem cleanup

EXPOSE 4000

WORKDIR /site

ENTRYPOINT [ "jekyll" ]

CMD [ "--help" ]

# build from the image we just built with different metadata
FROM jekyll as jekyll-serve

# Set environment variables
ENV JEKYLL_ENV=production
ENV URL=https://yourdomain.com

# On every container start, check if Gemfile exists and warn if it's missing
ENTRYPOINT [ "docker-entrypoint.sh" ]

# Command to serve the Jekyll site
CMD [ "bundle", "exec", "jekyll", "serve", "--force_polling", "--host", "0.0.0.0", "--port", "4000" ]

