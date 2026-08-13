# frozen_string_literal: true

desc 'Sort words in txt files into alphabetical order and remove duplicates.'
task :sort do
  Dir.glob('*.txt') do |filename|
    puts "Sorting and removing duplicates from #{filename}\n"
    file = File.open(filename)
    wordlist = file.readlines.map(&:chomp)
    # tie-break on the original string so equal-case-insensitive words sort deterministically
    wordlist = wordlist.sort_by { |w| [w.downcase, w] }
    wordlist = wordlist.uniq
    words = wordlist.join("\n")
    File.write(filename, words)
    file.close
  end
end
