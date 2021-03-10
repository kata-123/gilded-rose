## Gilded Rose Refactoring Challenge

Gilded Rose is a small inn buying and selling the finest goods. We have a system in place helping to update our inventory each day for their quality and days left to sell the item.

### The system
- For each day, this program runs to calculate the quality of each item
- Different items have different rules

### Current specification
- Each item has a SellIn value which denotes the number of days we have to sell the item
- Each item has a Quality value which denotes how valuable the item is
- At the end of each day our system lowers both values for every item
- Once the sell by date (SellIn=0) has passed, Quality degrades twice as fast
- The Quality of an item is never negative
- The Quality of an item is never more than 50, except for "Sulfuras" of which the Quality stays 80. 
- "Aged Brie" actually increases in Quality the older it gets
- "Sulfuras", being a legendary item, never has to be sold or decreases in Quality
- "Backstage passes", like aged brie, increases in Quality as its SellIn value decreases; Quality increases by 2 when there are 10 days or less and by 3 when there are 5 days or less but Quality drops to 0 after the concert

### The Task
- Review and refactor the current code
- Add support to a new type of item "Conjured", with the rule: "Conjured" items degrade in Quality twice as fast as normal items
