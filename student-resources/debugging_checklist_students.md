# Student Debugging Checklist - Unit 2
**Your Step-by-Step Guide to Fixing Programming Problems**

---

## 🚨 When Your Program Isn't Working

**DON'T PANIC!** Every programmer, from beginners to experts, spends time debugging. It's a normal and important part of programming. Use this checklist to systematically find and fix problems.

---

## 🔍 Step 1: Identify the Problem

### What Exactly Is Wrong?
**Check one or more that describes your situation:**

□ **My program won't start/run at all**
□ **My program starts but doesn't do what I expected**
□ **My program does some things right but has errors**
□ **My program crashes or stops unexpectedly**
□ **My program runs forever and won't stop**
□ **I get an error message I don't understand**

### Describe the Problem Specifically
*Write exactly what happens vs. what you expected*

**What I expected to happen:**
_____________________________________________________________________
_____________________________________________________________________

**What actually happens:**
_____________________________________________________________________
_____________________________________________________________________

**Error message (if any) - copy it exactly:**
_____________________________________________________________________
_____________________________________________________________________

---

## 🔧 Step 2: Basic Troubleshooting

### The "Quick Fixes" Checklist
*Try these simple solutions first - they fix many common problems*

□ **Save your work and refresh/restart your program**
□ **Check spelling of ALL variable names** (they must match exactly)
□ **Check spelling of ALL function names** (they must match exactly)
□ **Make sure you have matching parentheses ( ) and brackets [ ]**
□ **Verify quotation marks are closed properly " " or ' '**

### Visual Programming Track (Scratch) Specific
□ **Make sure blocks are connected properly (no gaps)**
□ **Check that custom blocks are defined before using them**
□ **Verify you're using the right blocks (motion vs. looks vs. control)**
□ **Make sure sprites have the costumes/sounds you're trying to use**

### Game Development Track (Godot) Specific
□ **Check that all lines end with proper punctuation**
□ **Make sure indentation is consistent (spaces or tabs, not mixed)**
□ **Verify function names match when calling them**
□ **Check that variables are declared before using them**

---

## 🕵️ Step 3: Systematic Investigation

### Test Small Pieces
*Don't try to debug your entire program at once*

**1. Isolate the Problem**
- Which part of your program works correctly?
- Which part has the problem?
- What's the smallest piece you can test by itself?

**2. Use Debug Output**
Add temporary messages to see what your program is thinking:

**Visual Programming (Scratch):**
```
Say (join "Variable value is: " [variableName]) for 2 seconds
```

**Game Development (GDScript):**
```gdscript
print("Variable value is: " + str(variable_name))
```

**3. Test Step by Step**
- Comment out or temporarily remove parts of your code
- Add one piece back at a time
- Test after each addition to see when the problem appears

### Variable Debugging
*Check that your variables contain what you think they do*

□ **Are variables created before you try to use them?**
□ **Do variables have the right data type? (text, number, true/false)**
□ **Are you accidentally changing variables when you don't mean to?**
□ **Are list positions correct?** (Scratch starts at 1, Godot starts at 0)

---

## 🎯 Step 4: Common Problem Solutions

### Problem: "My loop never stops" (Infinite Loop)

**Scratch Debugging:**
□ Check if your "repeat until" condition can ever become true
□ Make sure variables inside the loop are actually changing
□ Verify you're using the right comparison operators

**Godot Debugging:**
□ Check your while loop condition - will it ever become false?
□ Make sure variables in the condition are being updated inside the loop
□ Verify your for loop has proper range or collection

**Emergency Fix:** Add a counter to force the loop to stop:
```
Set [safetyCounter] to [0]
Repeat until (([safetyCounter] > [100]) or (your normal condition)):
  # Your loop code here
  Change [safetyCounter] by [1]
```

### Problem: "My conditional statements don't work"

**Check These Common Issues:**
□ **Assignment vs. Comparison:** 
  - Scratch: Use `=` for comparison
  - Godot: Use `==` for comparison, `=` for assignment
□ **Data Types:** Make sure you're comparing compatible types
□ **Boolean Logic:** Check if you need AND vs OR vs NOT

**Test Your Conditions:**
Add debug statements to see if conditions are true or false:
```
If (your condition) then
  Say "Condition is TRUE" for 1 seconds
Else
  Say "Condition is FALSE" for 1 seconds
```

### Problem: "My functions don't work"

**Scratch Custom Blocks:**
□ Is the custom block defined before you try to use it?
□ Are you passing the right number of inputs/parameters?
□ Are parameter names spelled correctly in the definition?

**Godot Functions:**
□ Is the function defined before you call it?
□ Are you passing the right number and type of parameters?
□ Is the function indentation correct?
□ Are you calling the function from the right object/script?

### Problem: "My lists/arrays have errors"

**Common List Issues:**
□ **Wrong Position Numbers:**
  - Scratch lists start at position 1
  - Godot arrays start at position 0
□ **Empty Lists:** Check if your list has items before accessing them
□ **Position Out of Range:** Make sure position exists in your list

**Safe List Access:**
```
# Scratch - check if position exists
If ((listPosition) ≤ (length of [myList])) then
  Set [item] to (item (listPosition) of [myList])

# Godot - check if index exists
if list_position < my_list.size():
    var item = my_list[list_position]
```

---

## 💬 Step 5: Getting Help Effectively

### Before Asking for Help
□ **I've tried the basic troubleshooting steps**
□ **I've identified the specific problem and can describe it clearly**
□ **I've tested smaller pieces of my code**
□ **I've added debug statements to understand what's happening**

### How to Ask for Help

**1. Show Your Code**
- Don't just describe the problem - let others see your actual code
- Point to the specific part that's causing trouble

**2. Explain Your Goal**
- "I'm trying to make the character move when I press a key"
- "I want to calculate the average of numbers in a list"

**3. Describe the Problem**
- "The character moves too fast"
- "I get an error message that says..."
- "The program stops at this line"

**4. Share What You've Tried**
- "I already checked the spelling of my variables"
- "I tested this part and it works, but this part doesn't"

### Good Help Request Example:
*"I'm trying to make my character jump when I press the space key. The character should move up and then come back down. Right now, when I press space, the character moves up but never comes back down. I've checked that my key detection works (I added a debug message), but something is wrong with my gravity code. Here's the specific part that's not working..."*

### Poor Help Request Example:
*"My game doesn't work. Can you fix it?"*

---

## 🧠 Step 6: Learn from the Fix

### After You Solve the Problem
**Take a moment to understand WHY it works now**

**Reflection Questions:**
1. What was the actual cause of the problem?
2. How could I have prevented this error in the first place?
3. What debugging technique helped me find the solution?
4. What should I remember for next time?

**Common Lessons:**
- "Always test small pieces before building complex programs"
- "Check variable spelling first - it's often the simplest problems"
- "Use debug print statements to see what my program is thinking"
- "Read error messages carefully - they usually tell me exactly what's wrong"

---

## 🏆 Debugging Success Strategies

### Build Good Habits
□ **Test frequently** - Don't write 50 lines of code before testing
□ **Use meaningful names** - `playerScore` is better than `x`
□ **Comment your code** - Explain what complex parts do
□ **Save working versions** - Before making big changes, save what works

### Debugging Mindset
- **Debugging is detective work** - look for clues systematically
- **Every bug is fixable** - it might take time, but there's always a solution
- **Mistakes are learning opportunities** - each bug teaches you something new
- **Ask for help when stuck** - even professional programmers collaborate

### Track Your Progress
**Problems I've Successfully Debugged:**

**Date:** _______ **Problem:** _________________________________ **Solution:** _________________________________

**Date:** _______ **Problem:** _________________________________ **Solution:** _________________________________

**Date:** _______ **Problem:** _________________________________ **Solution:** _________________________________

---

## 🎯 Emergency Debugging Protocol

### When You're Really Stuck (15+ minutes of no progress)

**1. Take a Break (5 minutes)**
- Step away from your computer
- Do something completely different
- Come back with fresh eyes

**2. Start Over (if needed)**
- Save your current work with a different name
- Create a simple version that just does the basic function
- Add complexity gradually

**3. Find a Study Partner**
- Explain your problem out loud to someone else
- Often you'll realize the solution while explaining
- Two people can spot errors faster than one

**4. Ask Your Teacher**
- Use the help request format from Step 5
- Be specific about what you've already tried
- Show your code and explain your goal

---

**🔧 Remember: Every programmer debugs constantly. The difference between beginners and experts isn't that experts don't have bugs - it's that experts are better at finding and fixing them quickly. Debugging is a skill that improves with practice! 💪🐛✨**