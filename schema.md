# API

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Mutation](#mutation)
  * [Objects](#objects)
    * [AppliedStatus](#appliedstatus)
    * [BasicField](#basicfield)
    * [Profile](#profile)
    * [Program](#program)
    * [ProgramForm](#programform)
    * [ProgramStatus](#programstatus)
    * [ReviewProgress](#reviewprogress)
    * [ReviewResult](#reviewresult)
    * [ReviewRubric](#reviewrubric)
    * [SubmittedForm](#submittedform)
    * [SubmittedRecommendLetter](#submittedrecommendletter)
    * [UploadField](#uploadfield)
    * [User](#user)
  * [Inputs](#inputs)
    * [NewBasicField](#newbasicfield)
    * [NewBuildForm](#newbuildform)
    * [NewProfile](#newprofile)
    * [NewReasonRubricSetting](#newreasonrubricsetting)
    * [NewRegister](#newregister)
    * [NewReviewSetting](#newreviewsetting)
    * [NewRubric](#newrubric)
    * [NewRubricSetting](#newrubricsetting)
    * [NewScoreRubricSetting](#newscorerubricsetting)
    * [NewSubmitData](#newsubmitdata)
    * [NewSubmitFile](#newsubmitfile)
    * [NewSubmitForm](#newsubmitform)
    * [NewSubmitRecommenderInfo](#newsubmitrecommenderinfo)
    * [NewUploadField](#newuploadfield)
    * [NewUser](#newuser)
  * [Enums](#enums)
    * [AppliedStatusType](#appliedstatustype)
    * [FieldType](#fieldtype)
    * [ReasonRubricType](#reasonrubrictype)
    * [Role](#role)
  * [Scalars](#scalars)
    * [Boolean](#boolean)
    * [Float](#float)
    * [ID](#id)
    * [Int](#int)
    * [String](#string)
    * [Time](#time)
    * [Upload](#upload)
    * [Void](#void)

</details>

## Query
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>users</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td>

Get all users for testing

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profile</strong></td>
<td valign="top"><a href="#profile">Profile</a>!</td>
<td>

Get user's profile

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>openedPrograms</strong></td>
<td valign="top">[<a href="#program">Program</a>!]!</td>
<td>

Get the programs opened now

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ownedPrograms</strong></td>
<td valign="top">[<a href="#program">Program</a>!]!</td>
<td>

Get user's own programs, for role of applicant, program mananger and reviewer

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>programForm</strong></td>
<td valign="top"><a href="#programform">ProgramForm</a></td>
<td>

Get program form format, return null if program doesn't setup

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program ID

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>appliedStatus</strong></td>
<td valign="top">[<a href="#appliedstatus">AppliedStatus</a>!]!</td>
<td>

Get all staus of programs user applied

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>appliedForm</strong></td>
<td valign="top"><a href="#submittedform">SubmittedForm</a>!</td>
<td>

Get the form applicant submmited

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program user applied

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>programStatus</strong></td>
<td valign="top"><a href="#programstatus">ProgramStatus</a>!</td>
<td>

Check the status of the program

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>programApplicants</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td>

Get the applicants of the program

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submittedForms</strong></td>
<td valign="top">[<a href="#submittedform">SubmittedForm</a>!]</td>
<td>

Get the form applicant submmited, return null if program doesn't setup

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">applicantId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>docReviewProgress</strong></td>
<td valign="top">[<a href="#reviewprogress">ReviewProgress</a>!]</td>
<td>

Get the document review progress, return null if program doesn't setup

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>docReviewResult</strong></td>
<td valign="top"><a href="#reviewresult">ReviewResult</a></td>
<td>

Get the document review result, return null if program doesn't setup

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>oralReviewProgress</strong></td>
<td valign="top">[<a href="#reviewprogress">ReviewProgress</a>!]</td>
<td>

Get the oral review progress, return null if program doesn't setup

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>oralReviewResult</strong></td>
<td valign="top"><a href="#reviewresult">ReviewResult</a></td>
<td>

Get the oral review result, return null if program doesn't setup

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>applicantsToDocReivew</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td>

Get the applicants with eligibility of document review in the program

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>applicantsToOralReivew</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td>

Get the applicants with eligibility of roal review in the program

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>viewSubmmitedForm</strong></td>
<td valign="top"><a href="#submittedform">SubmittedForm</a>!</td>
<td>

Get the form applicant submmited for review

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">applicantId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Applicant id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Get the count of all users

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>programManagerCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Get the count of all program managers

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reviewerCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Get the count of all reviewers

</td>
</tr>
</tbody>
</table>

## Mutation
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createUser</strong></td>
<td valign="top"><a href="#user">User</a>!</td>
<td>

Create user for testing

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newuser">NewUser</a>!</td>
<td>

User to create

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>login</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Login user with email and password

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">email</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

User's eamil

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">password</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

User's password

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>register</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Register new user

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newregister">NewRegister</a>!</td>
<td>

Register data for new user

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>verifyRegister</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Verify register of user

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>forgotPassword</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Send email for reset password

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">email</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

User's eamil

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>resetPassword</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Reset user password

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">newPassword</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

New password to reset

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatePassword</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Update user password with old password check

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">oldPassword</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Old password

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">newPassword</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

New password

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateProfile</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Update user's profile

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newprofile">NewProfile</a>!</td>
<td>

New profile to update, null field won't be update

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submitForm</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Applicant submit a form for apply to program

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">data</td>
<td valign="top"><a href="#newsubmitform">NewSubmitForm</a>!</td>
<td>

New form to submit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submitRecommendLetter</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Recommender submit a letter for applicant

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">programId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Program id

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">applicantId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Applicant id

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">content</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Letter content

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createProgram</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Create new program

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">name</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Name of the program

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>buildForm</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Build form for program

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newbuildform">NewBuildForm</a>!</td>
<td>

Form to build

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>setupDocReview</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Set up program document review setting

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newreviewsetting">NewReviewSetting</a>!</td>
<td>

Setting to apply to the program

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>setupOralReview</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Set up program oral review setting

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newreviewsetting">NewReviewSetting</a>!</td>
<td>

Setting to apply to the program

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>saveDocRubric</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Save a document rubric for applicant by reviewer

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newrubric">NewRubric</a>!</td>
<td>

Rubric for applicant

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>saveOralRubric</strong></td>
<td valign="top"><a href="#void">Void</a></td>
<td>

Save a oral rubric for applicant by reviewer

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#newrubric">NewRubric</a>!</td>
<td>

Rubric for applicant

</td>
</tr>
</tbody>
</table>

## Objects

### AppliedStatus

Status of the program user applied

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>programName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#appliedstatustype">AppliedStatusType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recommendLetter</strong></td>
<td valign="top">[<a href="#boolean">Boolean</a>!]!</td>
<td>

Return an empty array if no letter to write

</td>
</tr>
</tbody>
</table>

### BasicField

Form basic field format

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#fieldtype">FieldType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Profile

User profile

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>role</strong></td>
<td valign="top"><a href="#role">Role</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>idNumber</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>birthday</strong></td>
<td valign="top"><a href="#time">Time</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>telephone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cellphone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>address</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>school</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Program

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>openAt</strong></td>
<td valign="top"><a href="#time">Time</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>closeAt</strong></td>
<td valign="top"><a href="#time">Time</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ProgramForm

Program form format

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>basic</strong></td>
<td valign="top">[<a href="#basicfield">BasicField</a>!]!</td>
<td>

Basic field like name, email and phone, etc.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>upload</strong></td>
<td valign="top">[<a href="#uploadfield">UploadField</a>!]!</td>
<td>

Upload field for files upload

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recommendLetterNumber</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Num of recommend letters

</td>
</tr>
</tbody>
</table>

### ProgramStatus

Status of the program

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>formBuilded</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>docSetup</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>oralSetup</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ReviewProgress

Review progress of a reviewer

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>reviewer</strong></td>
<td valign="top"><a href="#user">User</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>done</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Num of the reviewer has reviewed

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>total</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Num of the reviewer to reviewed

</td>
</tr>
</tbody>
</table>

### ReviewResult

Results reviewers made for applicants

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>applicants</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reviewers</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rubrics</strong></td>
<td valign="top">[<a href="#reviewrubric">ReviewRubric</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### ReviewRubric

Scores and reason reviewer made for an applicant

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>applicant</strong></td>
<td valign="top"><a href="#user">User</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reviewer</strong></td>
<td valign="top"><a href="#user">User</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>scores</strong></td>
<td valign="top">[<a href="#int">Int</a>!]</td>
<td>

Null if the program doesn't setup score rubric

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>total</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Null if the program doesn't setup score rubric

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Null if the program doesn't setup reason rubric

</td>
</tr>
</tbody>
</table>

### SubmittedForm

Form applicant submitted

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>basic</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>uploads</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td>

Url to file

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recommendLetters</strong></td>
<td valign="top">[<a href="#submittedrecommendletter">SubmittedRecommendLetter</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### SubmittedRecommendLetter

Recommend letter of applicant

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>recommenderName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UploadField

Form upload field format

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### User

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

User id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Name of user

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Email of user

</td>
</tr>
</tbody>
</table>

## Inputs

### NewBasicField

Basic field for form building

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#fieldtype">FieldType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### NewBuildForm

Form building for program

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>programId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>basic</strong></td>
<td valign="top">[<a href="#newbasicfield">NewBasicField</a>!]!</td>
<td>

Basic field like name, email and phone, etc.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>uploads</strong></td>
<td valign="top">[<a href="#newuploadfield">NewUploadField</a>!]!</td>
<td>

Upload field for files upload

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recommendLetterNumber</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Num of recommend letters

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>openAt</strong></td>
<td valign="top"><a href="#time">Time</a>!</td>
<td>

Date of the program open at

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>closeAt</strong></td>
<td valign="top"><a href="#time">Time</a>!</td>
<td>

Date of the program close at

</td>
</tr>
</tbody>
</table>

### NewProfile

For register and update, keep field null for not to update

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>idNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>birthday</strong></td>
<td valign="top"><a href="#time">Time</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>telephone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cellphone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>address</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>school</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### NewReasonRubricSetting

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#reasonrubrictype">ReasonRubricType</a>!</td>
<td>

Reason rubric type

</td>
</tr>
</tbody>
</table>

### NewRegister

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>password</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profile</strong></td>
<td valign="top"><a href="#newprofile">NewProfile</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### NewReviewSetting

Review settings for program

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>programId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rubric</strong></td>
<td valign="top"><a href="#newrubricsetting">NewRubricSetting</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>applicantIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td>

This array is used to store the review order of the applicants

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reviewerIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>distribution</strong></td>
<td valign="top">[[<a href="#boolean">Boolean</a>!]!]!</td>
<td>

`Distribution[i][j] == true` mean `applicants[i]` is asigned to `reviewers[j]`

</td>
</tr>
</tbody>
</table>

### NewRubric

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>programId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>applicantId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>scores</strong></td>
<td valign="top">[<a href="#int">Int</a>!]</td>
<td>

Null if the program doesn't setup score rubric

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Null if the program doesn't setup reason rubric

</td>
</tr>
</tbody>
</table>

### NewRubricSetting

Rubric settings for program

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>score</strong></td>
<td valign="top">[<a href="#newscorerubricsetting">NewScoreRubricSetting</a>!]</td>
<td>

Null if the program doesn't setup score rubric

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reason</strong></td>
<td valign="top"><a href="#newreasonrubricsetting">NewReasonRubricSetting</a></td>
<td>

Null if the program doesn't setup reason rubric

</td>
</tr>
</tbody>
</table>

### NewScoreRubricSetting

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Score rubric name

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ratio</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td>

Score rubric ratio

</td>
</tr>
</tbody>
</table>

### NewSubmitData

Basic field

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>formFieldId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### NewSubmitFile

Upload field

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>formFieldId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#upload">Upload</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### NewSubmitForm

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>programId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>applicantId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>data</strong></td>
<td valign="top">[<a href="#newsubmitdata">NewSubmitData</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>files</strong></td>
<td valign="top">[<a href="#newsubmitfile">NewSubmitFile</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recommender</strong></td>
<td valign="top">[<a href="#newsubmitrecommenderinfo">NewSubmitRecommenderInfo</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### NewSubmitRecommenderInfo

Recommender info

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### NewUploadField

Upload field for form building

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### NewUser

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>password</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Enums

### AppliedStatusType

Status type of the program user applied

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>APPLIED</strong></td>
<td>

Applied but not yet determined eligibility

</td>
</tr>
<tr>
<td valign="top"><strong>ACCEPTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REJECTED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FieldType

Form field input type

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DEFAULT</strong></td>
<td>

Default text field

</td>
</tr>
<tr>
<td valign="top"><strong>NUMBER</strong></td>
<td>

Number field

</td>
</tr>
<tr>
<td valign="top"><strong>EMAIL</strong></td>
<td>

Email field

</td>
</tr>
</tbody>
</table>

### ReasonRubricType

Type of reason rubric

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NONE</strong></td>
<td>

No reason for rubric

</td>
</tr>
<tr>
<td valign="top"><strong>RECOMMENDATION</strong></td>
<td>

Used for teacher selection

</td>
</tr>
<tr>
<td valign="top"><strong>DIRECTADMISSION</strong></td>
<td>

Used for undergraduate special achievement , graduate and doctoral admission

</td>
</tr>
</tbody>
</table>

### Role

Role of user

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>USER</strong></td>
<td>

All users

</td>
</tr>
<tr>
<td valign="top"><strong>ADMIN</strong></td>
<td>

System administrators. Responsible for the maintenance, configuration, and reliable operation of system

</td>
</tr>
<tr>
<td valign="top"><strong>PROGRAMMANAGER</strong></td>
<td>

Program managers. Responsible for management of program like creation, modification and deletion

</td>
</tr>
<tr>
<td valign="top"><strong>REVIEWER</strong></td>
<td>

Reviewers. Responsible for applicant document and oral review

</td>
</tr>
<tr>
<td valign="top"><strong>APPLICANT</strong></td>
<td>

Applicants. The person submit form for reviewing

</td>
</tr>
</tbody>
</table>

## Scalars

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### Float

The `Float` scalar type represents signed double-precision fractional values as specified by [IEEE 754](https://en.wikipedia.org/wiki/IEEE_floating_point).

### ID

The `ID` scalar type represents a unique identifier, often used to refetch an object or as key for a cache. The ID type appears in a JSON response as a String; however, it is not intended to be human-readable. When expected as an input type, any string (such as `"4"`) or integer (such as `4`) input value will be accepted as an ID.

### Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.

### String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.

### Time

The `Time` scalar type represents time in RFC3339Nano format

### Upload

The `Upload` scalar type represents file data that can be uploaded

### Void

The `Void` scalar type represents null value, it shoud always be null

