# Gilded Rose Refactoring Kata

This Kata was originally created by Terry Hughes (http://twitter.com/TerryHughes). It is already on GitHub [here](https://github.com/NotMyself/GildedRose). See also [Bobby Johnson's description of the kata](http://iamnotmyself.com/2011/02/13/refactor-this-the-gilded-rose-kata/).



### Run the program
- clone this repo
- install gems
```bash
$ cd ruby
$ bundle
```
- run in irb
```bash
$ irb -r './lib/gilded_rose.rb'
```

### Testing
- from the root file run:
```bash
rspec
```
### Test Linting
- from root file run:
```bash
 $ rubocop
 ```

## Specification

### User Stories

```bash
As a user
So that I can keep track of stock quality
I want a program to do that for me
```

```bash
As an inkeeper
So that I can add new products
I want it to be easily modifiable
```

```bash
As an inkeeper
Due to buying new products which are conjured
I want the code to degrade my new product type twice as fast as a normal item
```


### Aim

- implement a new item type condition in the GildedRose class
  - new type is conjuring
    - Every day, an item of this type's quality will degrade by 2 if the sell_in value is 0 or above
    - after this, it will decrease by 4 every time. 
- refactor existing code to make it easier to implement new features
- provide a solid test base with high coverage

## Rubocop
Although linting was initially done with rubocop, I disagreed with the use of an if else statement over a case statement in the update_quality method. I found it less readable so have opted for the case statement. Due to this, rubocop does have active offences on this program. 
