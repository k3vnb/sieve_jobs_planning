# _Capstone Project Planning_  2/22/18

##### Planning session for my upcoming capstone project, a job interview preparation app in React/Redux.

#### By _**Kevin Boyle**_


### Project Description

![CapstoneProposal](img/CapstoneProposal1.png?raw=true)


#### Planning Session Notes

After re-reading 'Thinking in React' and puzzling over how best to break down my UI, I made a preliminary draft.
#### Flashcard UI
![FlashcardUI](img/basicUImockup.jpg?raw=true)
#### Tutorial UI
![TutorialUI](img/TutorialInterface.jpg?raw=true)
#### Component Tree Draft
![DraftComponentTree](img/componenttreeA.jpg?raw=true)

I believe there will need to be lots of revisions, especially to the component tree, at this time I realize the further away I get from the top of the component tree, the more abstract the concept feels, and I think I need to start plugging away at some of the higher components to get a better feel for how the information will start flowing.

###### Mock Ups
I used Google Slides to make some  very basic mock-ups of the pages to help facilitate the understanding of a better component tree

**Landing Page**
![LandingPage](img/landingpage.jpg?raw=true)
The Landing Page will have a more inviting visual element, however at its most basic it will give users the options to route to either flashcard mode or tutorial mode, or to see/edit their previous responses.

**Tutorial Page 1**
![Tutorial1](img/tutorialpage1.jpg?raw=true)
Tutorial page one is a brief tutorial about the kinds of questions that can be asked in an interview. Users are encouraged to click expand to see more & to compose their own stories for answers.

**Tutorial Page 2**
![Tutorial2](img/tutorialpage2userinput.jpg?raw=true)
Tutorial page 2 gives more info about the type of question, and suggestions for answering the questions. There is a user input field where the user will enter answers according to suggestions of how to break down the answers.

**Flashcard Page 1**
![Flashcard1](img/flashcardpage1.jpg?raw=true)
Simply the front side of a flashcard, they will be displayed randomly on page load. Users can choose to see 'answers' or to go to next flashcard.

**Flashcard Page 2- Answers**
![Flashcard2](img/flashcardpage2.jpg?raw=true)
Users will see a page analogous to Tutorial Page 2 with the user's input stories displayed.

**See My Stories 2- Answers**
![userinputstories](img/seemystoriespage.jpg?raw=true)
Users can go to this page to see their previously input stories to review, or edit.


#### MASTER OBJECT
**Preliminary Master JSON**
Trying to figure out how to lay out a better component tree, it occurred to me that I may want to envision my master object in JSON format, and find re-usable components, as I will be able to render different displays based on such an object.

1: {

	Meta-Topic:  ‘Your Experience History’,

	Example-Questions: [‘Tell Me About Yourself…’, ‘Tell me about your work history’, ‘What career accomplishments are you most proud of?’, ‘What’s the biggest mistake you made in your career and what did you do to learn from it?’],

	Recommended-Breakdown: [‘anchor’, ‘goal’, ‘obstacle’, ‘decision’, ‘result’],

	User-Input-Example: [null, null, null, null, null]
}

In this scenario, sometimes the key-pair values will correspond with one another, for example, index [0] of Recommended Breakdown would correspond with index [0] of User-input-example.

Having written out the JSON I also realize that I may need to allow the user to input more than one story, in which case there may need to user-input-example-1, user-input-example-2, etc.

The flashcards can randomly draw from example-questions key.

The pages can all render to some degree based on this sort of object though, to some degree with conditional rendering, for example if the User-Input-Example is void of actual user input then that will have to be controlled for, and if the user does not input items into all fields when filling out the personal stories, I think that can be ok as long as they fill out some of them, the returns will just render accordingly.

## Component Tree

Based on this planning, I made a new component tree:
![updatedComponentTree](img/sieve-jobs-component-tree.png?raw=true)

And this following component tree incorporates considerations about where state will reside:
![updatedComponentTreeWithState](img/component_tree_state.png?raw=true)


I have begun initializing a repository for building out a static version of the site, it can be found at:
https://github.com/lemurriot/job_prep.git
