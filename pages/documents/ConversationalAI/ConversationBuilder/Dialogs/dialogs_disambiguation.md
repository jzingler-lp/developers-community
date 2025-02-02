---
pagename: Disambiguation Dialogs
Keywords:
sitesection: Documents
categoryname: "Conversational AI"
documentname: Conversation Builder
subfoldername: Dialogs
permalink: conversation-builder-dialogs-disambiguation-dialogs.html
indicator: both
---

### What's disambiguation?

[Standard dialogs](conversation-builder-dialogs-standard-dialogs.html) are triggered when the bot recognizes the consumer's message via an intent match or a pattern match. [Fallback dialogs](conversation-builder-dialogs-fallback-dialogs.html) are triggered when the bot doesn't recognize the consumer's message at all. But what happens when the bot recognizes the consumer's message and matches it to *multiple intents*? This is where disambiguation can be used.

Disambiguation is the process whereby the bot gets clarification from the consumer on what is meant by the consumer's message.


Sometimes two or more intents match closely to the message, so clarification is needed:

<img style="width:325px" src="img/ConvoBuilder/dialogs_disambiguation1.png">

Other times, the user has expressed multiple intents in a single message, so, here again, clarification is needed:

<img style="width:325px" src="img/ConvoBuilder/dialogs_disambiguation2.png">

When a disambiguation dialog is used, the bot presents the best matches to the consumer and lets the consumer choose which is correct. This is shown in the examples above. The result is a better, smoother conversation.

#### An example use case

As an example, suppose the consumer enters "I lost my" and presses enter by mistake. The intent in this case isn't clear and might yield multiple, close matches. For example, it might mean a lost card or even a bereavement situation. Using a disambiguation dialog to clarify the consumer's intent means you can quickly address the correct issue.

### How a bot triggers a disambiguation dialog

If you create a disambiguation dialog, and if the bot matches the user's message to a single intent with a high confidence level (VERY_GOOD or GOOD), then the dialog that's associated with the matched intent is triggered directly. The disambiguation dialog isn't triggered. Also, the disambiguation dialog isn't triggered if the user's message matches a pattern. Only intents can be disambiguated.

A disambiguation dialog is triggered when the bot matches the message to *multiple intents*. Once the disambiguation dialog is triggered, it presents the consumer with the best intent matches.

<img style="width:350px" src="img/ConvoBuilder/dialogs_disambiguation4.png">

Once the user selects the correct intent, if that intent is associated with a User Says interaction in one of the bot's dialogs, that dialog's flow begins. Or, in the Disambiguation interaction, you can configure response match conditions to direct the flow as desired.

### Create a disambiguation dialog

1. Open the bot, and click **+ DIALOG** in the lower-left corner.
2. In the dialog that appears, specify the following:
    - **Dialog Name**: Enter a descriptive name.
    - **Dialog Type**: Select "Disambiguation Dialog."
    - **Match Threshold**: Select the minimum ranking that an intent match must have to be considered for disambiguation. For example, if you select FAIR_PLUS, then all intents that match with a rank of FAIR_PLUS and higher are considered for disambiguation.
    - **Disambiguate only selected domains**: If you only want the bot to include matches to intents in specific domains, select this check box, and then select those domains. You can select from all domains associated with dialogs in the bot.
3. Click **Save**.
4. Open the **Interaction Details** for the disambiguation interaction, click **Settings**, and specify the following:
    - **\# of intents to show**: Select whether to show 2 or 3 intent choices to the consumer. The intents are selected based on the match results that are in the same category.
    - **Something else** (checkbox): Select this if you want to add a "none of the above" type of choice to the clarification question. By default, in the conversation, this option returns a reply of, *"That's not what I was expecting, Please select from one of these options."* However, you can add a response condition to the disambiguation interaction and use pattern matching to direct the conversation flow in a different way.
    - **Something else** (label): This is the label for the "Something else" choice. The default value is, "Something else," but you can change this if desired.
5. Click **Save**.
6. In the Disambiguation interaction, enter the question text to send to the consumer.
    <img style="width:800px" src="img/ConvoBuilder/dialogs_disambiguation5.png">

    The intents will be dynamically populated, and their labels will be drawn from their intent display names as configured in [Intent Builder](intent-builder-overview.html).

    <img style="width:600px" src="img/ConvoBuilder/dialogs_disambiguation6.png">

7. Build out the Disambiguation dialog as desired.
    
    You can add any number of interactions to the dialog. For example, you might want to add a LivePerson Agent Escalation integration.
    
    To debug or access disambiguation intent data, use the built-in [disambiguation functions](conversation-builder-scripting-functions-get-set-contextual-data.html#get-disambiguated-intent).

### FAQs about disambiguation

**What happens if I don't use a disambiguation dialog?**

If you don't use a disambiguation dialog, here's how things work:

- If the user's message matches multiple intents that have the same rank (several matches are VERY GOOD, or several are GOOD), the bot picks the one with the highest raw match score, and then it processes the associated dialog.

- During matching, the bot considers only intents that evaluate to a VERY_GOOD or GOOD rank; intents that evaluate to FAIR_PLUS and FAIR are not considered.

**What happens if I use a disambiguation dialog, but no intents at or above the specified threshold are matched?**

When this happens, the fallback dialog is triggered if one exists. Otherwise, the default fallback message is sent to the consumer. For more on fallback, see [here](conversation-builder-dialogs-fallback-dialogs.html).

**How many disambiguation dialogs can I create?**

Like fallback dialogs, there can be only one disambiguation dialog in a bot.
