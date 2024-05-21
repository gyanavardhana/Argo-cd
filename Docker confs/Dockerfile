# Use the official Ruby image from Docker Hub with the correct version
FROM ruby:2.7.0

# Install Bundler with the version specified in the Gemfile.lock
RUN gem install bundler:2.4.22

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the Gemfile and Gemfile.lock into the container
COPY Gemfile Gemfile.lock ./

# Install dependencies using the specified Bundler version
RUN bundle install

# Copy the Rails application into the container
COPY . .

# Expose port 3000 to the outside world
EXPOSE 3000

# Start the Rails server when the container starts
CMD ["rails", "server", "-b", "0.0.0.0"]
