require 'time'

desc "Deploy"
task :deploy do
  puts "## Deploying to Github Pages.."

  build_dir = "_site"
  deploy_dir = "gh-pages"

  (Dir["#{deploy_dir}/*"]).each { |f| rm_rf(f) }

  puts "## Copying #{build_dir} to #{deploy_dir}"
  cp_r "#{build_dir}/.", deploy_dir

  cd "#{deploy_dir}" do
    system "git add ."
    system "git add -u"

    puts "## Commiting: Site updated at #{Time.now.utc}"
    message = "Site updated at #{Time.now.utc}"
    system "git commit -m \"#{message}\""

    puts "## Pushing generated #{deploy_dir} website"
    system "git push origin gh-pages --force"

    puts "## Deploy Complete!"
  end
end
