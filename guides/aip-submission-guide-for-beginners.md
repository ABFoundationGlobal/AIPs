---
title: AIP Submission Guides for Beginners
description: Detailed guide for unfamiliar with the AIP Process
weight: 11
---

{{< hint info >}}
This doc was originally from https://github.com/ABFoundationGlobal/AIPs/wiki and should be added to a AIP as reference.
{{< /hint >}}

This guide is for those unfamiliar with the AIP Process and provides simple instructions for AIP submission, update, and request for final. This guide won't cover complex AIP status change and other requests described in AIPs Guideline.

This guide covers:

- Start A AIP

- To Submit AIP for The First Time

- To Update a Draft AIP

- To Make A AIP to Final / Active

## I. Start A AIP

You can start writing your thoughts of a AIP first. And check if your thoughts are already in the existing AIPs.

You can choose from the AIP templates to get started. Since you already wrote down your thoughts, try to use a template from and finish the Summary and Abstract section. If your thoughts are not formed well enough, you can choose to skip the templates and use it later.

Discussion with other people, try to get one or more people become your co-authors, that helps your AIP become more carefully considered. Also it is recommended to have a public discussion board from the beginning. You can choose any public discussion services such as Google Groups, Facebook Pages, or your own Github repos.

You can choose any text editor apps to work with. If you are more familiar with Google Docs, Apple Pages, Microsoft Word, it is okay to use them to begin with. But the formal AIP for submission requires a Mark Down format. You will need to use a AIP template later.

## II. To Submit AIP for The First Time

All AIP submissions require to make a Pull Request(PR) from your own git repository on Github. If you haven't forked the AIPs repository, please follow the guide below to fork the AIPs repository and add your AIP to your repository.

### Fork the AIPs Repository

- You need a Github account and to be logged in

- Click the `Fork` button on the upper right of the [AIPs Github Page](http://github.com/ABFoundationGlobal/aips)

- You have successfully forked the AIPs repository

### Add your AIP to your repository

- Choose a template to start with.

- Add your AIP to `AIPS/AIP-X/index.md` file

### Create Pull Request for AIP submission

Make sure your AIP documents and assets follow the AIPs guideline. All AIPs submission not following the guideline require may get rejected.

- Change the AIP status from `WIP` to `Draft` when it's ready for submission

- Perform a PR from your repository to Newton's AIPs repository.

- State clear you are submitting the AIP for the first time in the title.

- Make sure to check **Allow edits from maintainers**

### AIP Editor Review

- AIP Editors will review your submission.

- If your AIP requires modifications, AIP Editors will point out and ask you to make changes in your repository.

- If the AIP editor thinks your AIP is ready for the Review Board to review. A AIP Editor will assign a AIP number and update your documents. You can not add/change your AIP number by yourself. If you self added/changed the AIP number. The submission will be rejected.

### AIP Board Review

- The AIP Review Board host meetings for AIP review regularly.

- The Authors may be invited to join the meeting depending on the type or contents of your AIP.

- If your AIP passed the review. Your AIP submission will pass and AIP Editors will include(merge) your AIP to Newton's AIPs Repository.

- If your AIP is good but require small changes like description, content naming space, add references to support your AIP. You should update your AIP documents. Once you have completed the change, add a reply to your PR and mention a AIP Editor to review your change. Once reviewed and the AIP Editor thinks it meets all the questions/problems from the Review Board. The AIP Editor will pass your AIP without additional review from the AIP Review Board, the AIP Editor will include(merge) your AIP to Newton's AIPs Repository.

- If the AIP Review Board thinks the AIP will not pass. Your submission will be rejected. And the PR will be closed. If you wish to continue on the same AIP, you can make a new PR in the future.

- As long as your new AIP PR is talking about the same thing and you kept AIP number assigned history from the AIP Editor in your repository. You can use the same AIP number in your future submission.

## III. To Update a Draft AIP

**You have to be one of the Author to update a AIP**

To update a Draft AIP, you must be one of the Authors mentioned in the AIP. If you are not amount the authors, your submission will be rejected. Contact the AIP Authors you are willing to join and ask them to add you to the AIP first.

If you tried contact the Authors and get no response, you may ask the AIP Editors for assistance. If the AIP Editors can't reach the AIP Authors, the editor may consider they have abandoned the AIP and change the status to abandoned. You may work on that and submit new updates to that AIP.

**Only AIP in Active/Draft status can accept updates\***

Once a AIP become Final. It can no longer accept changes.

An Active status AIP can accept updates for adding features, but other parts can not be changes.

### Create Pull Request for AIP update submission

- Perform a PR from your repository to Newton's AIPs repository.

- State clear you are updating a Draft AIP in the title. E.g. "Update AIP-3"

- Tell what have been changed to the last Draft in the descriptions.

- Make sure to check **Allow edits from maintainers**

### Review Procedure

The review is pretty much alike to Submit your AIP for the first time. Except there may be no AIP Review Board reviews required depending on the updates of the AIP.

## IV. To Make A AIP to Final / Active

A AIP Draft must be already in Newton AIPs repository before requesting for it to be finalised.

### Create an Issue for AIP to be finalised

- Create an issue in Newton's AIPs repository on Github.

- State you want to finalised a AIP in the title. E.g. "AIP-3, request for Final"

- Tell why you think it can be finalised in description.

### AIP Editor Review

- AIP Editors should check the request and go through the current Draft.

- AIP Editors should also check if the request is agreed from all the authors.

- AIP Editors should ask the AIP Review Board to include this topic in the next meeting.

### AIP Review Board Review

- AIP Review Board should make the decision whether the AIP can/should be finalised.

- AIP Review Board should also giving a Public Review period. Normally 14 days, but depending of the AIP, the period may change.

### Public Review

- If the AIP Review Board decides a AIP can be finalised, a Public Review is going to happen.

- AIP Editors should change the AIP status to Public Call.

- The Public Call of a AIP should be prominently listed on Newton Project's official website.

- Any change request to the AIP document during the Public Review will result the AIP status revert to Draft.

- When a AIP has passed the Public Review. AIP Editors will update the status to Final/Active.
