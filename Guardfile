# A sample Guardfile
# More info at https://github.com/guard/guard#readme

# Add files and commands to this file, like the example:
#   watch(%r{file/path}) { `command(s)` }
#

#guard :shell do
#  watch /lib\/(.*)\.lib/ do |m|
#    m[0] + " has changed."
#    `cd test && tests.sh`
#  end
#end

guard :shell do
  watch /(test|lib)\/(.*)\.(lib|bats)/ do |m|
    m[0] + " has changed."
    `cd test && bats #{m[2]}.bats`
  end
end
