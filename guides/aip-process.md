---
title: AIP Process
weight: 21
description: How AIP is proccessed and status is changed during the process
---

{{< hint info >}}
This doc was originally from https://github.com/ABFoundationGlobal/AIPs/wiki and should be added to a AIP as reference.
{{< /hint >}}

## Shepherding a AIP

Parties & Roles involved in the process a AIP are: AIP you, the AIP Champion(Lead) or Authors, AIP Editors, AIP Review Board, and the Public Communnity.

Before you begin writing a formal AIP, you should vet your idea. Ask the Newton community first if an idea is original to avoid wasting time on something that will be be rejected based on prior research.

In addition to making sure your idea is original, it will be your role as the author to make your idea clear to reviewers and interested parties, as well as inviting editors, developers and community to give feedback. You should try and gauge whether the interest in your AIP is commensurate with both the work involved in implementing it and how many parties will have to conform to it. Negative community feedback will be taken into consideration and may prevent your AIP from moving past the Draft stage.

## General AIP Flow

```bash
General AIP Status Flow
---
"WIP" -> "Draft" -> "Public Call" -> "Final / Active"
```

See [AIP Status](aip-status.md) for more AIP Statuses and flowchart.

### I. Submit a AIP Draft for the first time

Follow the procedure in Contributing a AIP or AIP Submission Guides for Beginners to Start a AIP.

Once the AIP is ready to become a `Draft`, create a PR to the AIPs repository.

{{< details title="View AIP Process">}}

```bash --simplified
# Submit a AIP Draft for the first time
AIP_Status = "WIP"
$Authors:
  change AIP_Status = "Draft"
  create PR = "New AIP-X Draft"
{ CHECK CONTENTS }
  $AIP_Editor:
    case Good >> { ASSIGN NUMBER }
    case Ready >> { BOARD REVIEW }
    case Require Edit
      request $Authors to Edit >> { CHECK CONTENTS }
    case Not Pass && Will Not Continue
      PR = "Closed" && exit AIP Process
{ ASSIGN NUMBER }
  $AIP_Editor:
    assign AIP_Number = "Issue/PR Number"
    update PR = "New AIP-# Draft" && >> { CHECK CONTENTS }
{ BOARD REVIEW }
  $AIP_Review_Board:
    case Accept
      PR = "Merged" && exit AIP Process
    case Deny
      PR = "Closed" && exit AIP Process
```

{{< /details >}}

### II. Update a AIP Draft

- Only AIP in `Draft` status can accept updates

- You have to be one of the Authors to update a AIP

To update a Draft AIP, you must be one of the Authors mentioned in the AIP. If you are not amount the authors, your submission will be rejected. Contact the AIP Authors you are willing to join and ask them to add you to the AIP first.

If you tried contact the Authors and get no response, you may ask the AIP Editors for assistance. If the AIP Editors can't reach the AIP Authors, the editor may consider they have abandoned the AIP and change the status to abandoned. You may work on that and submit new updates to that AIP.

{{< details title="View AIP Process">}}

```bash --simplified
# Update a AIP Draft
AIP_Status = "Draft"
$Authors:
  create PR = "Update AIP-# Draft"
{ CHECK CONTENTS }
  $AIP_Editor:
    case Ready >> { CHECK IF REVIEW REQUIRED }
    case Require Edit
      request $Authors to Edit >> { CHECK CONTENTS }
    case Not Pass && Will Not Continue
      PR = "Closed" && exit AIP Process
{ CHECK IF REVIEW REQUIRED }
  $AIP_Editor:
    case Required >> { BOARD REVIEW }
    case Not Requred
      PR = "Merged" && exit AIP Process
{ BOARD REVIEW }
  $AIP_Review_Board:
    case Accept
      PR = "Merged" && exit AIP Process
    case Deny
      PR = "Closed" && exit AIP Process
```

{{< /details >}}

### III. Make a AIP Draft to AIP Final / Active

- A AIP `Draft` must be already in Newton AIPs repository before requesting for it to be finalised to `Final` / `Active`

- You have to be one of the Authors to make a AIP `Final` / `Active`

- Once a AIP become `Final`. It can no longer accept changes

- Create an PR in Newton's AIPs repository on Github

- Tell why you think it can be finalised in description

If you are not amount the authors, your submission will be rejected. Contact the AIP Authors you are willing to join and ask them to add you to the AIP first.

If you tried contact the Authors and get no response, you may ask the AIP Editors for assistance. If the AIP Editors can't reach the AIP Authors, the editor may consider they have abandoned the AIP and change the status to abandoned. You may work on that and submit new updates to that AIP.

{{< details title="View AIP Process">}}

```bash --simplified
# Make a AIP Draft to AIP Final
AIP_Status = "Draft"
$Authors:
  change AIP_Status = "Public Call"
  create PR = "Make AIP-# Final"
{ CHECK CONTENTS }
  $AIP_Editor:
    case Ready >> { BOARD REVIEW }
    case Not Pass && Will Not Continue
      PR = "Closed" && exit AIP Process
{ BOARD REVIEW }
  $AIP_Review_Board:
    case Accept
      PR = "Merged" && >> { PUBLIC REVIEW }
    case Deny
      PR = "Closed" && exit AIP Process
{ PUBLIC REVIEW }
  case Accept
    AIP_Status = "Final" && exit AIP Process
  case Deny
    AIP_Status = "Draft" && exit AIP Process
```

{{< /details >}}

### IV. Update an Active AIP

- You have to be one of the Authors to update an `Active` AIP

- An `Active` status AIP can accept updates for adding features, but other parts can not be changes

{{< details title="View AIP Process">}}

```bash --simplified
# Update an Active AIP
AIP_Status = "Active"
$Authors:
  create PR = "Update Active AIP-#"
{ CHECK CONTENTS }
  $AIP_Editor:
    case Ready >> { CHECK IF REVIEW REQUIRED }
    case Require Edit
      request $Authors to Edit >> { CHECK CONTENTS }
    case Not Pass && Will Not Continue
      PR = "Closed" && exit AIP Process
{ CHECK IF REVIEW REQUIRED }
  $AIP_Editor:
    case Required >> { BOARD REVIEW }
    case Not Requred
      PR = "Merged" && exit AIP Process
{ BOARD REVIEW }
  $AIP_Review_Board:
    case Accept
      PR = "Merged" && exit AIP Process
    case Deny
      PR = "Closed" && exit AIP Process
```

{{< /details >}}

## Special AIP Flow

```bash
Special AIP Status Flow
---
"Draft" -> "Abandoned" -> "Draft"
"Final" -> "Implemented"
"Final" -> "Deferred" -> "Implemented"
"Final" / "Implemented" -> "Superseded"
"Draft" -> "Rejected"
```

### Flow of Abandoned AIP

See [Transferring AIP Ownership](transfer-aip-ownership.md).

### AIP Final become Implemented or Deferred

`tbd`

### AIP Got Superseded

`tbd`

### Rejected AIP

`tbd`
