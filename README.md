momentum
===========================

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

Momentum is a (hopefully) unique variant of the classic to-do list.
The main philosophies of the Momentum project are as follows.
* Must offer a visual progress indicator
* Simple, uncluttered interface
* Unique (and intuitive) item entry


## concept brainstorming area (for cleanup later)

**Item entry:** 
I don't like the typical static input box that most todo lists offer. On one hand, it makes entering items atomically simple and quick for the user ('get milk', enter, 'pick up kids', enter, ..., etc). On the other hand, this gives you very little control over the structure of your list. Furthermore, the user doesn't have a great idea of what the list actually *looks* like, especially if the input box is at the top of the page and your items keep getting appended to the bottom.

On the opposite end of the spectrum, we have something like a notepad or text editor. Some people prefer to just jot out their thoughts. They have complete control over the layout of their list, and they know exactly what it will look like while they are writing it. This appeals to me. However, for the purpose of a simple checklist, this is often times too much freedom. What flexibility the user gains by being able to jump between lines with arrow keys is countered by the loss of ability to drag items around without resorting to selecting, cutting, and pasting. Also, it is difficult to put any kind of controls on items (delete button, for example) as it isn't a discrete unit; it's just a line of text contained within the greater context of a text input box.  

I think the best approach is a hybrid of both methods. Those automatic tokenizations you see in certain fields like tag entry in StackOverflow somewhat inspired this. Behavior as follows:
* user is presented with a blank page (using "page" in this context to describe the to-do list itself, not the overall webpage design)
* active field. blinking cursor with a single placeholder line to get the user started
* return key drops to new line, which is also a new entry (so revolutionary I know)
* double space causes new line to be a child item. automatic indentation behavior (if using something like codemirror) so that the user remains in child entry until s/he breaks out. 
* child item might be formatted differently. perhaps a lighter gray color. perhaps italic font. perhaps a smaller font size. OH, and there needs to be a vertical bar to the left to offer better visual structure.
* user is allowed free carriage returns. i don't want to put up walls if i don't need to. plus it may help let the user organize their lists into different chunks
* project stages- user can make a header with # symbol, like markdown. 

As for UI and control layout, I am not 100% sure. This will take some experimentation. Right now this is what I envision:
* hopefully no visual separators (if necessary, make them very minimal or perhaps just make separators visible on mouse hover)
* controls on the right somewhere. I want them close to the items but far enough that the user has plenty of space to write lengthier item descriptions. i'm thinking of a light gray circle with a checkmark, or perhaps just a status indicator like "not done" "in progress" "complete". clickable of course. 
* controls only get appended to lines that actually contain valid entries. headers and blank lines will be ignored.

**concepts to ponder at a later juncture:**
* I want my items draggable. Figure out best approach.
* Should there be any magic formatting when a valid entry line is inputted, sort of like those tag things I was talking about? 

