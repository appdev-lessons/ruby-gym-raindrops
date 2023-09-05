# Ruby Gym: Raindrops

Convert a number to a string, the contents of which depend on the number's factors.

- If the number has 3 as a factor, output `"Pling"`.
- If the number has 5 as a factor, output `"Plang"`.
- If the number has 7 as a factor, output `"Plong"`.
- If the number has any combination of those factors, output each (e.g. `"PlingPlangPlong"` if all three are factors)
- If the number does not have 3, 5, or 7 as a factor, just print the number.

Examples:

- 28's factors are 1, 2, 4, 7, 14, 28. In raindrop-speak, this would be a simple `"Plong"`.
- 30's factors are 1, 2, 3, 5, 6, 10, 15, 30. In raindrop-speak, this would be a `"PlingPlang"`.
- 34's factors are: 1, 2, 17, and 34. In raindrop-speak, this would be `"34"`.

More Examples:

- `integer = 1`, prints `1`
- `integer = 5`, prints `"Plang"`
- `integer = 21`, prints `"PlingPlong"`

Your program should output the correct response for all of the randomly `sample`d `integer` values below, then you should get the tests to pass.

```ruby
integers = [1, 21, 35, 105]
integer = integers.sample
# write your program below
```
{: .repl #raindrops title="Raindrops" readonly_lines="[1,2,3]"}


```ruby
describe "Raindrops" do
  it "prints '52' if the integer is 52" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(52)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/52/), "Expected output to be '52', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_1 for="raindrops" title="Raindrops prints '52' if the integer is 52" points="1"}


```ruby
describe "Raindrops" do
  it "prints 'PlingPlangPlong' if the integer is 105" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(105)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/PlingPlangPlong/), "Expected output to be 'PlingPlangPlong', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_2 for="raindrops" title="Raindrops prints 'PlingPlangPlong' if the integer is 105" points="1"}


```ruby
describe "Raindrops" do
  it "prints 'Plang' if the integer is 3125" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(3125)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/Plang/), "Expected output to be 'Plang', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_3 for="raindrops" title="Raindrops prints 'Plang' if the integer is 3125" points="1"}


```ruby
describe "Raindrops" do
  it "prints 'Plong' if the integer is 49" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(49)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/Plong/), "Expected output to be 'Plong', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_4 for="raindrops" title="Raindrops prints 'Plong' if the integer is 49" points="1"}


```ruby
describe "Raindrops" do
  it "prints 'PlangPlong' if the integer is 35" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(35)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/PlangPlong/), "Expected output to be 'PlangPlong', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_5 for="raindrops" title="Raindrops prints 'PlangPlong' if the integer is 35" points="1"}


```ruby
describe "Raindrops" do
  it "prints 'Plang' if the integer is 25" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(25)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/Plang/), "Expected output to be 'Plang', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_6 for="raindrops" title="Raindrops prints 'Plang' if the integer is 25" points="1"}


```ruby
describe "Raindrops" do
  it "prints 'PlingPlong' if the integer is 21" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(21)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/PlingPlong/), "Expected output to be 'PlingPlong', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_7 for="raindrops" title="Raindrops prints 'PlingPlong' if the integer is 21" points="1"}


```ruby
describe "Raindrops" do
  it "prints 'PlingPlang' if the integer is 15" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return(15)
    output = capture_stdout { require_relative(path) }
    expect(output).to match(/PlingPlang/), "Expected output to be 'PlingPlang', but was '#{output}'."
  end

  def capture_stdout
    old_stdout = $stdout
    $stdout = StringIO.new
    yield
    $stdout.string
  ensure
    $stdout = old_stdout
  end
end
```
{: .repl-test #raindrops_test_8 for="raindrops" title="Raindrops prints 'PlingPlang' if the integer is 15" points="1"}
