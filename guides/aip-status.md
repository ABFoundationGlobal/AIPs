---
title: AIP Status
description: Standard AIP Status for Newton Evolution Proposals.
weight: 41
---

{{< hint info >}}
This doc was originally from https://github.com/ABFoundationGlobal/AIPs/wiki and should be added to a AIP as reference.
{{< /hint >}}

## I. Available AIP Statuses

Statuses listed below is the Standard AIP Status for Newton Evolution Proposals.

### Regular Statuses

1. WIP
2. Draft
3. Public Call
4. Final
5. Implemented

### Special Statuses

6. Deferred
7. Superseded
8. Active
9. Abandoned
10. Rejected

## II. Status Definations

Each status change is requested by the AIP author and reviewed by the AIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your AIP. The AIP editors will process these requests as per the conditions below.

### 1. WIP(Work In Progress)

**WIP**: Work In Progress is the status before a AIP is submitted to Newton for review. The champion can use other status name such as an _IDEA_ to share the AIP for discussion outside Newton's Github repository.

#### `WIP` --> `Draft`

- Once the champion has finished a AIP and consider it's ready to be merged to Newton's Github repository. they will write a draft AIP as a **pull request**. Consider including an implementation if this will aid people in studying the AIP.

### 2. Draft

**Draft**: If the draft is agreeable amount the Newton community, AIP editor will assign the AIP a number (generally the issue or PR number related to the AIP) and merge your pull request. The AIP editor will not unreasonably deny an AIP.

#### `Draft` -> update `Draft`

- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the AIP to be mature and ready to proceed to the next status.

#### `Draft` -> `Public Call`

- ✅: If agreeable, the AIP editor will assign `Public Call` status and set a review end date (_review-period-end_), normally 14 days later.

- ❌ -> `Draft`: A request for `Public Call` status will be denied if material changes are still expected to be made to the `Draft`. We hope that AIPs only enter `Public Call` once, so as to avoid unnecessary resource.

#### `Draft` -> `Rejected`

- See `Rejected` status.

#### `Draft` -> `Abandoned`

- See `Abandoned` status.

### 3. Public Call

**Public Call**: This AIP will listed prominently on the https://newtonproject.org/aip website.

#### `Public Call` -> `Active` / `Final`

- ✅: A successful `Public Call` without material changes or unaddressed technical complaints will become Final.

- ❌ -> `Draft`: A `Public Call` which results in material changes or substantial unaddressed technical complaints will cause the AIP to revert to `Draft`.

### 4. Final

**Final**: This AIP represents the current state-of-the-art. A `Final` AIP should only be updated to correct errata.

#### `Final` -> `Implemented`

- See `Implemented` status.

#### `Final` -> `Deferred`

- See `Deferred` status.

#### `Final` -> `Superseded`

- See `Superseded` status.

### 5. Implemented

**Implemented**: Some AIP is required one-time only implementation to meets the AIP's to be completed. Once the implementation is complete, the status will be changed to "Implemented" by an editor. Only AIPs with status `Final` can be changed to `Implemented`.

#### `Implemented` -> `Superseded`

- See `Superseded` status.

### 6. Deferred

**Deferred**: An AIP with plan to be `Implemented` will become `Deferred` if haven't met the criteria to be marked as `Implemented`.

### 7. Superseded

**Superseded**: An AIP which was previously `Final` but is no longer considered state-of-the-art. Another AIP will be in `Final` status and reference the `Superseded` AIP. An AIP cannot move on from this state.

### 8. Active

**Active**: Some Informational and Process AIP may also have a status of `Active` if they are never meant to be completed.

### 9. Abandoned

**Abandoned**: This AIP is no longer pursued by the original authors or it may not be a preferred option anymore.

#### `Abandoned` -> `Draft`

- Authors or new champions wishing to pursue this AIP can ask for changing it to `Draft` status.

### 10. Rejected

**Rejected**: An AIP that is fundamentally broken. An AIP cannot move on from this state.

## III. Flowchart

{{<mermaid class="text-center">}}
graph TD

AuthorEdit[Authors' Edit] --> |PR| Draft

subgraph "AIP Review Process"
Draft --> Rejected
Draft --> PublicCall[Public Call]
Draft --> Abandoned
Abandoned --> Draft
end

PublicCall --> PublicCall_Merged[Public Call]

PublicCall_Merged --> Draft
PublicCall_Merged --> Final
PublicCall_Merged --> Active

subgraph "Status Change on Conditions"
Final --> Deferred
Deferred --> Implemented
Final --> Implemented
Deferred --> Superseded
Implemented --> Superseded
Final --> Superseded
end

subgraph "AIP Review Process"
Active --> |PR| Active
end

{{</mermaid >}}
