---
pagename: Knowledge Bases
redirect_from:
Keywords:
sitesection: Documents
categoryname: "Conversational AI"
documentname: Knowledge Base
permalink: knowledge-base-knowledge-bases.html
indicator: both
---

This topic provides information on managing a knowledge base. For an introduction to knowledge bases, see [here](knowledge-base-overview.html).

### Add a knowledge base

**To add a knowledge base**

1. In the Dashboard, click **Add Knowledge Base** in the upper-right corner.
2. Specify the following:
    * **Data source name**: 
    * **Data source type**: Select "Knowledge Base."
    * **Language**: 
    * **Import articles from**: You can add articles manually, but if you have them in an external file, you can import them when you add the knowledge base. Select either "CSV" or "Google Sheet," and use the controls provided to upload the file's contents.
    * **Intent Association**: Select either "Knowledge Base Intents" or "Domain Intents." If you select "Domain Intents," also select the domain from the list that appears.
3. Click **Add**.

### Configure knowledge base settings

**To configure knowledge base settings**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Specify the following:
    * **Data source name**: 
    * **Data source type**:
    * **Language**: 
    * **Import articles from**:
    * **Knowledge Base ID**: 
    * **Intent Association**: This field is read only. However, if the knowledge base uses Knowledge Base intents, you can convert them to Domain intents; for help with this, see [below](knowledge-base-knowledge-bases.html#convert-knowledge-base-intents-to-domain-intents).
    * **Associated Domain for Entity**: This field is only displayed if the knowledge base uses Knowledge Base intents.
    * **Associated Domain**: This field is only displayed if the knowledge base uses Domain intents. 
    * **Account**: 
    * **Public**: 
4. Click **Update**.

### Convert Knowledge Base intents to Domain intents

Intro to be added

Converting the intents is a non-recoverable action, so be certain about doing so before taking this action.

**To convert from Knowledge Base intents to Domain intents**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Click **More Options**, and scroll down to the **Intent Association** section.
4. Click **Convert to Domain Intents**.
5. In the dialog that appears, select the domain.
6. In the confirmation dialog, click **Confirm**.

### Add stop words

Intro to be added

**To add a stop word to a knowledge base**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Click **More Options**, and scroll down to the **Stop Words** section.
4. Enter the word, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_add.png"> (Refresh icon).


### Add keyword patterns

Intro to be added

**To add a keyword pattern to a knowledge base**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Click **More Options**, and scroll down to the **Keyword Patterns** section.
4. Enter the pattern, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_add.png"> (Refresh icon).

### Sync with a Google sheet

Intro to be added

**To sync a knowledge base with a Google sheet**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Click **More Options**, scroll down to the **Sync Google Sheet Data Source** section, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_syncGoogleSheet.png"> (Refresh icon).


### Refresh the intents

Intro to be added

**To refresh the intents in a knowledge base**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Click **More Options**, scroll down to the **Refresh Intents** section, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_refresh.png"> (Refresh icon).


### Download a knowledge base

Export of a knowledge base creates a CSV file.

You might need to download a knowledge base for a few reasons:

* a
* b
* c

**To download a knowledge base**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Click **More Options**, scroll down to the **Download Knowledge Base** section, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_download.png"> (Download icon).
4. Follow the browser prompts to access and save the CSV file to a location of your choice.


### Delete a knowledge base

Deleting a knowledge base is a non-recoverable action, so be certain about doing so before taking this action.

**To delete a knowledge base**
1. Open the knowledge base, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_settings.png"> (Knowledge Base Menu icon) in the lower-right corner.
2. In the Settings panel, click **KB Settings**.
3. Click **More Options**, scroll down to the **Delete Knowledge Base** section, and click <img style="width:25px" src="img/ConvoBuilder/icon_kb_delete.png"> (Delete icon).
4. In the confirmation dialog, click **Yes**.