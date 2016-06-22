title: RSPEC Notes
tags: ["testing", "rspec"]
notebook: DBC
---
you can't see this ->>> [](testing)
[](rspec)

# RSPEC Notes

```

describe AppleTree do
  let(:tree){AppleTree.new(2, 5)}


  #The rest of my tests are wrapped in this statement
end

```

## Object equivalance

expect(tree.pick_an_orange.class).to eq Orange 	#passes if actual == expected


## Truthiness and exestentialism

 expect(tree.has_oranges?).to be false 	# passes *if* actual == false
 expect(tree.age.class == Fixnum).to be_truthy 	# passes if actual is truthy (not nil or false)

## Change Observation

expect {tree.pass_growing_season}.to change{tree.age} 	#changes object value from old to new

## Comparisons
        
expect(tree.pass_growing_season).to be > 0