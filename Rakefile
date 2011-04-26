require 'bundler'
Bundler::GemHelper.install_tasks

begin
  require 'yard'
  YARD::Rake::YardocTask.new(:yard) do |t|
    t.options = ['--title', 'MetaTags Documentation']
    if ENV['PRIVATE']
      t.options.concat ['--protected', '--private']
    else
      t.options.concat ['--protected', '--no-private']
    end
  end
rescue LoadError
  puts 'Yard not available. Install it with: sudo gem install yard'
end
