# frozen_string_literal: true

desc 'Sort words in txt files into alphabetical order and remove duplicates.'
task :sort do
  Dir.glob('*.txt') do |filename|
    puts "Sorting and removing duplicates from #{filename}\n"
    file = File.open(filename)
    wordlist = file.readlines.map(&:chomp)
    wordlist = wordlist.sort_by(&:downcase)
    wordlist = wordlist.uniq
    words = wordlist.join("\n")
    File.write(filename, words)
    file.close
  end
end
