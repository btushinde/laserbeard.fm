guard 'minitest' do
  # with Minitest::Unit
  watch(%r|^test/(.*)\\/?test_(.*)\\.rb|)
  watch(%r|^lib/(.*)([^/]+)\\.rb|)     { |m| "test/\#{m[1]}test_\#{m[2]}.rb" }
  watch(%r|^test/test_helper\\.rb|)    { 'test' }
 
  # with Minitest::Spec
  # watch(%r|^spec/(.*)_spec\\.rb|)
  # watch(%r|^lib/(.*)([^/]+)\\.rb|)     { |m| "spec/\#{m[1]}\#{m[2]}_spec.rb" }
  # watch(%r|^spec/spec_helper\\.rb|)    { "spec" }
 
  watch(%r|^app/controllers/(.*)\\.rb|) { |m| "test/controllers/\#{m[1]}_test.rb" }
  watch(%r|^app/helpers/(.*)\\.rb|)     { |m| "test/helpers/\#{m[1]}_test.rb" }
  watch(%r|^app/models/(.*)\\.rb|)      { |m| "test/unit/\#{m[1]}_test.rb" }  
end

guard 'spinach' do
  watch(%r|^features/(.*)\\.feature|)
  watch(%r|^features/steps/(.*)([^/]+)\\.rb|) do |m|
    "features/\#{m[1]}\#{m[2]}.feature"
  end
end
