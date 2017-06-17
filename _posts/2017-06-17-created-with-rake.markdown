---
layout: post
title:  "Created with rake"
date:   2017-06-17 21:40:13 +0300
categories: jekyll rake
---
As the title suggests this post was created using a rakefile.
Here is the rakefile if anyone's interested in using it in their own blog:
{% highlight ruby %}
# Sources:
# http://jasonseifer.com/2010/04/06/rake-tutorial
# http://elia.wordpress.com/2008/11/07/get-input-in-rake-tasks/
# http://www.layouts-the.me/rake/2011/04/23/rake_tasks_for_jekyll/

# Asking for title
def ask message
print message
STDIN.gets.chomp
end

# Print before the task is complete
STDOUT.sync = true
title = ask('Title: ')

#Create new a post
desc "Default command runs the 'new' command"
task default: %w[new]

desc "'new' command creates a new post"
task :new do
  filename = "#{Time.now.strftime('%Y-%m-%d')}-#{title.gsub(/\s/, '-').downcase}.markdown"
  path = File.join("_posts", filename)
  if File.exist? path; raise RuntimeError.new("File exists #{path}"); end
  File.open(path, 'w') do |file|
    file.write <<-EOS
---
layout: post
title: #{title}
date: #{Time.now.strftime('%Y-%m-%d %k:%M:%S')} +0300
---
EOS
end
# invoke code to edit file
 sh "code -g #{path}:6"
 end
 
{% endhighlight %}
Source: [quyennguyen](http://quyennguyen.com/code/rake_for_jekyll/) (Edited a bit)