# How to Help
## Add a New Rulebook
There are two ways to create a new rulebook. You can either do it yourself or [make a rulebook request](#make-a-request) if you're not comfortable using GitHub. 

To create a rulebook yourself, you'll need to use Markdown to format it.

If you have an existing rulebook PDF that you'd like to use, I recommend using http://pdf2md.morethan.io/ to do an initial conversion to Markdown. Then, copy all the plain text output and run it through http://removelinebreaks.net/ to fix any weird PDF line breaks. I recommend using the settings "Convert line breaks to: Spaces" and "Convert paragraphs to: Empty line."

Edit your rulebook as you see fit. At any time, you can  [view a live preview.](#test-your-rulebook) 

Don't forget to add [required metadata to your rulebook!](#rulebook-metadata)

When your rulebook is ready to be submitted for review, [create a new file here](https://github.com/camden/rulebooks/tree/master/rulebooks). Name your file with the full name of the rulebook, in lowercase, replacing any spaces with hyphens. Remember to add a ".md" file extension. For example, "Settlers of Catan" should be named "settlers-of-catan.md".

## Update an Existing Rulebook
There are two ways to edit an existing rulebook. You can either do it yourself or  [make a change request](#￼make-a-request) if you're not comfortable using GitHub.

To edit a rulebook yourself, click the **Edit** button on the rulebook page.

![](/api/assets/edit.gif)

This will open **GitHub**. GitHub is a site that developers use to host code. I opted to use GitHub to host all the rulebook data. [Read more about that here.](/about)

If you don’t have a GitHub account, you’ll be asked to create one. Don’t worry, it should only take a minute! Once you’re in, you’ll see a bunch of text. The text is in a format called **Markdown**. [Learn more about Markdown here.](https://en.wikipedia.org/wiki/Markdown) 

![](/api/assets/github.png)

Wait a minute… what’s that bit at the top?

![](/api/assets/front-matter.png)

This is called **Front Matter**. Front Matter allows us to insert metadata about the current rulebook without affecting the presentation. Front Matter is written in a language called [YAML](https://learnxinyminutes.com/docs/yaml/). 

See [*Rulebook Metadata*](#rulebook-metadata) to learn more about **Required** and **Optional** metadata.

Edit the rulebook as you see fit. At any time, you can [view a live preview.](#test-your-rulebook)

#### Submit Your Changes
When you’re satisfied, submit your changes. Enter a title and a description (be descriptive!) and then hit “Propose file change.”

![](/api/assets/propose-change.gif)

Then, create a **pull request**! Creating a pull request means that I’ll get a notification about your change, and if I agree with your changes, I’ll merge them into the live website!

![](/api/assets/create-pull-request-for-edit.gif)

## Make a Request
To request either a new rulebook or a rulebook change, [create a new GitHub issue here](https://github.com/camden/rulebooks). Be sure to tag the issue correctly.

Hopefully, the request will be responded to shortly by myself or another contributor.

## Rulebook Metadata
The metadata of a rulebook lives in the top of the file, in what’s known as Front Matter. Front Matter is just [YAML](https://learnxinyminutes.com/docs/yaml/) inserted between two `---`. 

### Required Metadata
#### Title
The title of the game.

Example: `title: Settlers of Catan`

#### Source
The source of the rulebook. Usually a link to a PDF file.

Example: 
```
source: http://www.catan.com/en/download/?SoC_rv_Rules_091907.pdf
```

#### Tags
Any tags associated with your game. I usually like to find the game on BoardGameGeek and use some of their tags.

Example:
```
tags:
  - bluffing
  - deduction
  - party
  - card-game
```

### Optional Metadata
#### Information
Information about the game, like player counts and playing time.

Example:
```
information:
  player-count: 2-8
  play-time: 15 minutes
```

##### Player Count
The minimum and maximum numbers for this game, in the following format: `{min}-{max}`

Example: `player-count: 3-4`

##### Play Time
The minimum and maximum play time for this game (roughly), in the following format: `{min}-{max} {time-units}`

Example: `play-time: 60-120 Minutes`

#### Glossary
The words/phrases in the glossary will be highlighted and clickable to reveal their definition.

Each glossary item has the following properties:
* **Name**: The display name of the glossary item.
* **Matches**: A list of words to match for this glossary item. Useful for irregular plurals.
* **Definition**: A plain-text (i.e. no markdown) definition of the glossary item. This is what will be shown when the word is clicked.

Example:
```
glossary:
  - name: Villager
    definition: |
      The Villager has no special abilities, but he is definitely not a werewolf. Players may often claim to be a Villager. The Villager is on the village team.

  - name: Werewolf
    matches: 
      - werewolf
      - werewolves
    definition: |
      At night, all Werewolves open their eyes and look for other werewolves. If no one else opens their eyes, the other Werewolves are in the center. Werewolves are on the werewolf team.
```

## Test Your Rulebook
To preview your rulebook, copy the whole thing (in markdown!) and head over to the handy [Rulebook Previewer](/custom-rules). Paste your rulebook into the little text box at the top, then hit “Enter.”

![](/api/assets/preview.gif)

Spiffy!

## Report Bugs & Request Features
To report a bug or request a feature, you can either [create an Issue on GitHub](https://github.com/camden/rulebooks) or tweet at (@camdenbickel)[https://twitter.com/camdenbickel].

## Help Keep the Lights On
If you're enjoying Rulebook.io, consider making a small donation to help with server costs. 

[PayPal.me/camden](https://paypal.me/camden/5)

Thank you! :)

