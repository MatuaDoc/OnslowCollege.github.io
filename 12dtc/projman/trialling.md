---
title: Testing & trialling
---

As part of your project, you are required to test and trial the components that you develop. These are the basic requirements for **Achieved**, so you should not skip out on this important part of the process.

# Testing

Testing is straight-forward. You are checking whether your component functions as intended.

For programming testing, the portfolio provides a small version of the testing table from the Programming Assessment. Use this to test the components that you have worked on in a given sprint.

Though you are not required to find EBI (expected/boundary/invalid) cases as part of the standard itself, you should continue to do this — exercise best practice to ensure that your components can actually move from the testing phase to completion.

> If you do not thoroughly and accurately test your components, they will not be able to move to completion. This will clog up your Testing and In-Progress sections in your project boards. **Test properly and thoroughly!**

# Trialling

Trialling is a process of trying different things to see what works best for the component.

Similar to the design process you explored in 11DIT, you can think of this as a feedback cycle:

- you have tried a couple of different approaches to the component
- you ask your end-users/classmates/teacher which approach they think works best
- based on their feedback, you make a decision about which approach to use

Not all trialling needs to be feedback-based. You may trial different ways to structure the code of a component — for example, lists vs 2D lists vs dictionaries — and wish to determine which would be best. In that case, you could do a PMI analysis of each approach, then select the one you wish to continue with in your development.

## Example 1

***What components are you going to trial?***

One of the things that will need to be done during Sprint 1 is a good description of the game, one per user group. The description needs to clearly explain the goal of the game and how to play – for the students, and functionality of the game and how to use it – for the teachers. 

| Option 1 | Option 2 | Option 3 |
| :-- | :-- | :-- |
| Dear colleagues, thank you for choosing Simple math quiz for your classroom. The aim of the program is to help you to ascertain student’s previous maths knowledge in a fun and engaging way. Research determined that uncertainty of an upcoming reward has been a great motivator for the students to keep playing the game and learning essential math skills in the process. As a teacher you have an option to change the questions to make them easier or harder, depending on the year level. The student’s will be able to rate the questions difficulty, giving you an indication of their confidence levels. The report printed at the end will have all the questions answered with rating the student gave them. Hope you and your students enjoy the game. For support email contact@simplemaths.co.nz or call 0800 FUNMATH. | Kia Ora koutou katoa. Great times ahead of us! Welcome to Simple maths! Great to see you here. Simple game the students will love due to the uncertainty of the final reward. Functional game for you. Adjust the question to your needs. Print the final report and let it guide your pedagogy. Win win all around. If any questions occur do not hesitate to reach us on contact@simplemaths.co.nz or call us on 0800 FUNMATH. | Welcome everyone! Such a great day to teach and learn about maths. At simple maths we value your time and want to make math fun for our learners. With two menus (one for teachers and one for students) we achieve just that. Your students will be able to play, learn and have fun, while you are in full control of what questions they get. The program also prints out a handy report to help you plan. The uncertain reward is what will bring the students back time after time. Check it out. Any feedback is appreciated. You can reach us on contact@simplemaths.co.nz or call directly 0800 FUNMATH. |

**Feedback**

| | |
| :-- | :-- |
| **Component** | Teacher's game description |
| **Name** | Mr Example |
| **Feedback** | Like the first option, but include Te Reo in it. |

| | |
| :-- | :-- |
| **Component** | Teacher's game description |
| **Name** | Mx Sample |
| **Feedback** | I like how descriptive option 1 is. I think it gives a really good overview. I like the use of Te Reo Maori in option two but think the rest is a little too informal. I don’t like option three – it feels more like a sales pitch than a description. I think option one works best but would like to include some Te Reo in it too. |

| | |
| :-- | :-- |
| **Component** | Teacher's game description |
| **Name** | Ms Exemplar |
| **Feedback** | The first option is a very comprehensive overview of all the functions the program has for teachers to help their students. However, the language in the first option is very formal and could perhaps be more casual and friendly. I also like the use of Te Reo in the second option as it is an important part of our cultural identity. Perhaps this could be used in place of the greeting of the first option. |

***What is the outcome of my feedback?***

From all of the feedback the teachers gave it is obvious that Te Reo will need to be included in the description to show the commitment to the Treaty of Waitangi and the role that education plays in promotion of that commitment. Otherwise the first option will be reviewed and updated to be less formal, but just as descriptive.

**Final version**

Kia Ora koutou katoa and thank you for choosing Simple math quiz for your classroom. The aim of the program is to help you to ascertain student’s previous maths knowledge in a fun and engaging way. Research determined that uncertainty of an upcoming reward has been a great motivator for the students to keep playing the game and learning essential math skills in the process. As a teacher you have an option to change the questions to make them easier or harder, depending on the year level. The student’s will be able to rate the questions difficulty, giving you an indication of their confidence levels. The report printed at the end will have all the questions answered with rating the student gave them. Hope you and your students enjoy the game. For support email contact@simplemaths.co.nz or call 0800 FUNMATH. 

## Example 1

***What components are you going to trial?***

I need to store the different attacks that the hero will be able to do in a data structure, but I'm not sure which. I will try using the three collection types that we have learnt in 11DIT and 12DTC. I have created code samples of how each of these would look.

| Option 1 | Option 2 | Option 3 |
| :-- | :-- | :-- |
| Lists | 2D Lists | Dictionary |

**Feedback**

```python
attacks = ["Punch", "Sword", "Hammer"]
power = [5, 25, 50]
```

| | |
| :-- | :-- |
| **Component** | List |
| **Name** | Me |
| **Feedback** | P: these are easy to understand |
| | N: I have to store the damage in a separate list |

```python
attacks = [["Punch", 5], ["Sword", 25], ["Hammer", 50]]
```

| | |
| :-- | :-- |
| **Component** | 2D Lists |
| **Name** | Me |
| **Feedback** | P: I can store the different types of attacks in different lists within the main attack list |
| | N: I have to remember all the different indices for each different type of attack |

```python
attacks = {
    "Punch": 5,
    "Sword": 25,
    "Hammer": 50
}
```

| | |
| :-- | :-- |
| **Component** | Dictionary |
| **Name** | Me |
| **Feedback** | P: these are easy to understand, and I can store different attack types under different keys. These are more descriptive than 2D list indices |
| | N: I'm not as experienced with dictionaries |

***What is the outcome of my feedback?***

I have trialled using all the types and analysed them. From this, I have concluded that lists are unsuitable because I can't separate out different types of attacks. Of the two remaining types, dictionaries are easier to model because I don't have to remember which position in the main list I need to get the attack data from.

I will use dictionaries for the attack list.