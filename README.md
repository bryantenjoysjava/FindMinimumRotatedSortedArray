# Thoughts
When I was thinking of a proper solution, my immediate thought was to just use a set and check which unique number in the set is the smallest, but the question asked for Olog(n) time
complexity. I then thought of using binary search. We can do this because the list is sorted. The way the algorthim works is that we instatitate a left pointer, middle pointer, and
right pointer in the list, the middle pointer starts at the beginning of the list, the middle pointer is the middle index of the list, and the right pointer is the last index of the 
list. We compare the element in the middle of the list with the last element in the list, if the middle value is greater than the last value in the list, we know that the 'split'
is on the right side of the list, and therefore the minimum value is also on the right side of the middle element. If this is the case, we cut the left half including the middle value
and look at the right half. However, if this isnt true, then the minimum value must be the middle value or any element before the middle value in the list, so we cut the all elements
out to the right of the middle element. After checking each of these conditions, the list is then split in half. These iterations are continued while the left pointer is less than the right pointer.
After, we return the middle element, although, we can return any of the pointers because they'll all have converged to the same element.
