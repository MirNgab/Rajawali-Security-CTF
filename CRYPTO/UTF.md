# UTF - 10 Points
> \u{43}\u{54}\u{46}\u{52}\u{53}\u{54}\u{7b}\u{55}\u{54}\u{46} \u{31}\u{36}\u{5f}\u{69}\u{35}\u{5f}\u{61}\u{77}\u{33}\u{73} \u{30}\u{6d}\u{65}\u{7d}
### Solution
This is an unicode escape sequence with extra step thanks to the curly brackets, and there are spaces too for whatever reason but i don't think this one is too much of a prblem. We need to remove the curly brackets cause that causes it to be an invalid. 

![image](https://github.com/user-attachments/assets/6a0da657-40c9-4916-b89f-a1ec2dd48b72)

I used this [site](https://onlinecaseconvert.com/remove-characters-from-text-online/) to remove all the curly brackets and spaces. From the looks of it, it's probably valid by now and we can start decoding it, but it was still said to be invalid. It got me confused for a bit and went a little deep dive on utf in which i learnt about padding.

