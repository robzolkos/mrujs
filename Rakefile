require "bundler/setup"

task :test do
  Dir.chdir("test/rails/dummy") { system("bundle exec rails test:all") }
end


namespace :ci do
  task :test do
    Dir.chdir("test/rails/dummy") do
      sh("bundle exec rails db:prepare")
      sh("bundle exec rails test:all")
    end
  end
end
