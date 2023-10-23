# Linking and Listing

This is the GDSC DSA challenge for week whatever-this-is-lets-just-call-it-one. We're trying out a new thing and we'd love to hear your feedback on this, so text [@omgitsalongusername](https://t.me/omgitsalongusername) on Telegram if you have any questions or comments (like if it's too hard, nit-picky, or easy and trivial).

If you've done [Advent of Code](https://adventofcode.com/) before, the layout of the questions will be familiar for you, but if you haven't here's a quick primer:

- The question is divided into two parts, part one sets up the story and problem statement, and part two builds on that by adding additional constraints
- You shouldn't look at the second part until you're done with the first...normally it would be gated, but this is a Markdown file, so there's only so much I can do.
- Once you're done with the first, make a copy your part one code and then work on part two with the copy.
- Make a git repository on your platform of choice (GitHub, Bitbucket, your home server etc.) and let it look somewhat like this:

  ```sh
  you/gdsc-dsa-stuff
  |
  |- week-one
  |  |
  |  |- part-one.c
  |  |- part-two.c
  |
  |- week-two
  |
  ...
  ```
  
  This will be where your submissions live.

<summary>
<h2>Part 1</h2>
</summary>

<details>
Hey there, it's your first day at your super fabulous job where you...sort and arrange boxes. It's not much, but in this economy? You'll take anything you got.

Upon arriving at the office, you see them all just scattered willy-nilly all over the place and your first task is to find, and implement a more efficient way to arrange them all relative to each other.

Your boss tells you the following things:
- A box can contain one thing, in this case, a name (which can be considered to be a string of ASCII characters).
- Boxes are arranged on the shelves in the storeroom, and for your purposes, they're essentially of infinite length.
- The boxes should be arranged in such an order that every box has one "after" it — beginning from the first box you should be able to follow the order all the way to the next one, until you reach the last one.
- The first and last box do not have anything before or after them, respectively.
- The order is not necessarily the way the boxes are placed on the shelves — you can "jump" to the end and back and around if that's what your boss wants. 
- Boxes should be able to be inserted at any point in the chain, **WITHOUT** having to move every box after it to the right on the shelves — moving each and every one of them would take way too long, and you're the only worker here.

After careful consideration, you decide to store the boxes as nodes in a [linked list](https://en.wikipedia.org/wiki/Linked_list), with the shelves being taken to represent computer memory. You choose this over an array because of the last requirement by your boss — a contiguous array would require you having to move everything to the right of where you want to insert a new node, and that would take too long.

In your language of choice, implement a linked list, where the nodes contain a string (it's a name so it's probably not more than 50 characters). 

Do not use the standard library implementation of a linked list (`std::list` in C++, `std::collections::LinkedList` in Rust etc), but you are free to look at their implementation to see what you can do.

It doesn't necessarily have to be the most performant implementation, focus on writing clear, concise code.

The list should have the following methods:
- `at(position)`, where `position` is a positive number denoting the position of the box in the order — it should return the box at that number, or an appropriate value if it doesn't exist.
- `add(box)`, which adds a new box to the end of the list and returns the position that it got added at.

Make any appropriate classes/structures/objects as you need, and try to use error-handling techniques that are best for your language.

If using a non-garbage collected language, ensure you implement proper memory management for your objects.
</details>

<summary>
<h2>Part 2</h2>
</summary>

<details>
Your boss is happy with your work so far, but wants a few more changes to be made:

- Currently you can't go "back" to a box before you on the shelves, because boxes only store information about what comes immediately after them. Fix this by allowing boxes to store info. about what comes "before" them too.
- Add methods that allow you to delete boxes at a position, and insert a box at a specific place in the order — with errors handled appropriately.
- Make a function that can "prettily" print the contents of the entire list (or specific boxes) to standard output — preferably by implementing `ToString()` or its equivalent in your language.
</details>

Good luck!
