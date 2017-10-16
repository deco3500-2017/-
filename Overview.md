<h1>What is this</h1>
This file follows the whole design process for Project Moonlight, with design aspects highlighted to ensure ease of marking.
</br></br>
<h1>Stages</h1>

<h2>Initial Idea</h2>
The initial idea of Moonlight was to promote a feeling of safety by better connecting people with a geographical proximity. The use case driving this application was the concept of <i>someone wanting someone else to walk them to their car after a late lecture</i>. The key target was an application that would allow people to feel safer.

<h2>Early Idea Development</h2>
The course coordinator was contacted early in the development process for feedback. Key areas of focus were isolated from this feedback (emphasis added to quote).

</br><q>
Yes, I would say that is in the problem domain. Establishing trust & ensuring safety are definite challenges for community based applications - especially communities where people <b>don't already know each other socially</b>. 
Exploring the concept of trust/safety would be interesting - though you would want to <b>focus on a particular sector/area</b> (ie. communities connecting strangers) to help constrain it.
</q></br></br>

From this the following requirements of the intial idea were developed:
<ul>
<li>A way to develop trust between strangers</li>
<li>A way to facilitate this development of trust</li>
</ul>

<h2>Group Work 1</h2>
Initial connection with the group was made, and the idea was adopted. During the first week of discussion, the major work order was for completion of research into similar applications which was to be completed by the next week. This was to be completed in paralell to the critical feature the group agreed upon, that in order for any part of the application to be adopted, it would need to be perceived as *secure*.

<h2>Security Features</h2>
<h3>Government ID</h3>
The first stage of development required determining a set of features that would provide "safety" in the context of the applications usage. After studying research by information security experts regarding abuse of systems, the <i>identity</i> component of the application was found to be the key to the safety.</br>
If all users (not the accounts of the users, but the user themselves) of the application could be uniquely identified, then any offence would be tied to them as a person, meaning they would not have anonimity. Research revealed this anonimity was a key cause of abuse. Research was then conducted to determine the best way to do this.</br>

<h4>Research</h4>
It was found that as part of a </i>100 points of identification</i> scheme introducted to prevent money laundering in Australia, many finanical institutions are required to collect a government ID. This included many fully online sites, trading in currencies such as Bitcoin. This did not deter usage by users. It was also found that other peer to peer applications exist where such a Government ID is required, such as Uber. This positively supported the inclusion of this as a feature for preventing anonimity.

<h4>Reception</h4>
Interviews conducted with users during the term showed users would be willing to upload a government ID, as long as the application was secure, and would not disclose this. Comments were made comparing this process to Uber, showing that people are already open to authentication such as this through Uber.

<h4>Integration</h4>
This feature was then accepted as an addition. The signup process would require that before an account could perform any functions involving interaction with other users, an ID would need to be uploaded. This could easily be performed from any mobile device with a reasonable resolution camera. Existing solutions already exist that would allow this to automatically be verified.

<h3>Trustmark</h3>
Once identity is positively established. Then an objective rating system can be applied that ensures no abuse will go unpunished. Due to the nature of the application, and the dangers associated, it was decided that any abuse could not be forgiven, and would need to result in a permanent ban.</br>
This resulted in the concept of a *TrustMark*. This is associated with each user, and is a sign that a user has not commited any offence, and has uploaded a government ID. This would be revoked if any abuse was committed.</br>
