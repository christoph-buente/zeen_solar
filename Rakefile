require 'nanoc3/tasks'

task :converter do
  
  begin
    filepath = 'output/kontakt/index.php'
    content = File.read(filepath)
    content.gsub!(/\&lt;/, '<')
    content.gsub!(/\&gt;/, '>')
    content.gsub!(/\&quot;/, '"')
    content.gsub!(/\&apos;/, "'")
    File.open(filepath, "w") {|file| file.puts content}
  rescue => err
    puts "Exception: #{err}"
    err
  end
  
end