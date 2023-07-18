**Q1> Given an array [1,2,3,2,5,6,9,6,5,3,2,2,1,8,10,10,7]. Create a hash and store the frequency of the array element.** 
 ```
 arr = [1, 2, 3, 2, 5, 6, 9, 6, 5, 3, 2, 2, 1, 8, 10, 10, 7]
m = Hash.new(0)

arr.each do |i|
  m[i] += 1
end

puts m
 ```
 output:
 ```
 {1=>2, 2=>4, 3=>2, 5=>2, 6=>2, 9=>1, 8=>1, 10=>2, 7=>1}
 ```
**Q2> Write a program to print sum of numbers from 100 to 200** 
```
sum=0
for i in 100..200
    sum+=i
end    
p sum
```
output:
```
15150
```
 
**Q3> Write an exception for dividing by zero in Ruby.** 
```
class DivisionByZeroError < StandardError
  def initialize(message = "Division by zero is not allowed.")
    super(message)
  end
end

def divide_numbers(a, b)
  raise DivisionByZeroError.new("Cannot divide #{a} by zero.") if b == 0
  a.to_f / b.to_f
end

puts divide_numbers(6,9)
puts divide_numbers(3,0)
```
output:
```
0.6666666666666666
main.rb:8:in `divide_numbers': Cannot divide 3 by zero. (DivisionByZeroError)
        from main.rb:13:in `<main>'
```
**Q4 > Write a program to find and replace all occurrences of a character in a string.** 
```
s="Sarthak Tiwari is a Trainee at Kreeti Technologies"
s=s.gsub("T","A")
s=s.gsub("t","a")
p s
```
output:
```
"Sarahak Aiwari is a Arainee aa Kreeai Aechnologies"
```
