# Documents

Once you have created or uploaded documents, you can manage revisions, collaborate on the document content, share with other Document Manager users, publish to libraries, add to personal collections, set reminders and activities, and more.

## Managing documents

### Action bar

* **Comment.** Each document comes with its own timeline to allow users to discuss, plan, and collaborate. Click **Comment** to add a new comment to the timeline discussion.
* **Share.** Share your document with other users that are helping write or review the document.
* **Upload.** Upload a new version of the document.
* **Change Owner.** Providing ownership of a document helps ensure that the document is maintained and managed. When a handover is needed, use the Change Owner option to assign the document to another owner.
* **Add to Collection.** Collections are used to help organize your documents and make them easier to find within your document list. Use this action item to add the document to one of your existing collections.
* **Review.** Create a review activity for the document.
* **Change Status.** Three statuses are available: Draft, Active, and Retired. Draft status indicates that the document is still being worked on and is not ready for consumption. Active documents are deemed ready for publishing to a library. Once a document is active, the Publish option is made available. A retired document is hidden from any library that it is associated with.
* **Publish.** The Publish action is only available on a document once the status of the document has been set to Active. Once a document is Active, you can then publish it to one or more libraries.
* **More.** Here you can delete a document or lock/unlock it.

## Lifecycle processes

![Lifecycle processes](/_books/documentmanager-user-guide/images/document-manager-progress-tracker.png)

Invoke a lifecycle process to automate management of documents lifecycle events. Typical examples of document lifecycle processes include:

* **Publishing a document to a library**
  * Approvals
  * Status Changes
  * Publishing

* **Document reviews**
  * Managing documents edits and approvals
  * Retiring documents and removing them from libraries
  * Managing review dates
  * Lifecycle processes. By default, this is off. You must enable this setting in the admin console: `webapp.documentmanager.bpmLifecyle.enabled`

* **Roles**
  * Configure lifecycle processes in the admin console under the Document Manager tile. Lifecycle processes are accessible to users assigned the Business Process Manager role.
  * All users will need a User level Document Manager role in order to perform actions in the lifecycle process (e.g. DocManager User).
  * Lifecycle processes can only be invoked by users who have the Can Modify Metadata Permissions for the document they want to invoke a lifecycle against.

### Using lifecycle processes

Lifecycle processes can be manually invoked from the document view. If no lifecycle processes are created, the lifecycle option will not be visible in the document view.

Once lifecycle processes are created and active, users with the docmanager designer role will be able to configure which lifecycle processes to make available using the **Design this** button.

Document users will then be able to manually invoke available active lifecycle processes. Only one lifecycle process can be running at any given time. Once a lifecycle process is started, its progress tracker will be visible at the top of the document view.

Once a lifecycle process has finished, its progress tracker will disappear from the document view.

### Lifecycle history

Once a lifecycle process has completed, the Heads Up Display (HUD) will disappear. You can view all previous lifecycle processes that have run on the document from the **Lifecycle** button dropdown > **Show History** option.

You can view the HUD for each lifecycle process that was run against the document.

### Configuring the lifecycle process button

![Lifecycle button](/_books/documentmanager-user-guide/images/dm-lifecycle-button.png)

* **Default Label.** Give the button a display value (which will be visible when a lifecycle process is not in flow).
* **Translated Label.** Add additional language variants of the default label, which will be displayed to users viewing the document view in the language defined in the user settings.
* **Button Styling.** Choose a background color that will be used for the button when a lifecycle process is not in flow.
* **Drop Down Options.** Configure the lifecycle processes you wish to make available from the button. By default, this will show all Document Manager-defined lifecycle processes defined in the admin console and marked as active.
  * Use the trash bin icon to remove any lifecycle processes you do not want to make available from the button.
  * Use the arrows to re-order the lifecycle processes in the dropdown.
  * Edit each dropdown option to set the following:
    * Set the Default Label as it will appear in the dropdown.
    * Set any translated label values.
    * Set button style and image when the lifecycle process is running.

### Disabling manual options when a lifecycle process is running

Optionally, you may want to disable the ability for a user to perform certain manual actions while a lifecycle process is running. The following options can be disabled globally, from the settings tile under Document Manager in the admin console. These settings will then apply to any document that has a lifecycle process actively running against it.

* Publishing: webapp.documentmanager.bpmLifecyle.whileLifecycleRunning.disableManual.publishing. OFF by default, so manual actions are permitted.
* Set Review Date: `*webapp.documentmanager.bpmLifecyle.whileLifecycleRunning.disableManual.setReview` OFF by default so manual actions are permitted.
* Status Change: `webapp.documentmanager.bpmLifecyle.whileLifecycleRunning.disableManual.statusChange` OFF by default so manual actions are permitted.

### Opening, downloading, and checking out files for editing

If the document you are viewing has been *uploaded to* Document Manager, you will see options to:

* **Open.** Download the current version of the document.
* **Checkout for Editing.** Download the current version of the document but also lock the document preventing other users from checking out the current version of the document for editing.
  * If you check out a document for editing, when finished, you can upload a new version and unlock the document from the **More** dropdown option.

If the document you are viewing has been *created in* Document Manager, you will see the option to open. This opens the document and provides the following options:

* **Edit.** Open the document for editing. If you save changes to the document while editing, this will create a new version of the document and add the previous version of the document as a revision (if revision tracking was enabled for the document).
* **Details.** Switch back to the Details view of the document.
* **Full Screen.** Display the document in full-screen mode.
* **Print.** Allow for the printing of the document.
* **Toggle View.** Switch between the full-screen mode and the normal-view mode.

## Revisions

The Revisions feature allows for version tracking. For documents where revision tracking has been enabled, a Revisions section holds all previous versions of the document. Users who have rights to the document can open and download any previous versions of the document.

Revisions are added in different ways depending on whether the document was *created in* Document Manager or *uploaded to* Document Manager:

* **Uploaded documents.** Each time a new upload is added to the document, the previous active version is added to the revision history and the new upload becomes the live version.
* **Created documents.** If a document has been created using Document Manager's text or drawing document options, each time you save changes to the document, this creates a new live version of the document, and the previous live version is added to the revision history.

You can view the changes between revisions in the Revisions section of the document. This shows anything that has been removed (in red) or added (in green).

## Timeline

The timeline (activity stream) on a document plays two roles. Firstly, it acts as an audit trail for changes to the document, such as new revisions added or ownership of the document having changed, as well as recording any changes of rights assigned to users the document has been shared with.

Secondly, the timeline provides an environment for users who have rights to the document to be able to collaborate on the content of the document and discuss changes or additions they would like to make. As with all activity streams, all collaboration in the form of posts and comments is recorded and supports the embedding of rich media content like images, videos, and so on. It also supports wiki markup.

* **Follow.** See updates to the document timeline appear in your news feed.
* **Mobile.** Follow updates on your native mobile. Contribute on the go to collaborative work on the document via the documents timeline.

## Tags

Add tags to your document to help with searching and organizing.

* Use the global search to find documents based on tags.
* Create self-organizing collections of documents based on documents with specific tags.
* Filter and find documents in libraries based on tags.
* View all documents you have access to through a tag cloud view.

## Activities

Create activities relating to the management of the document. View and receive notifications relating to document activities in your My Activities views, and on your mobile app.
