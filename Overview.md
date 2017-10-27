<h1>What is this</h1>
This file follows the whole design process for Project Moonlight, with design aspects highlighted to ensure ease of marking.

<h2>Initial Idea</h2>
The initial idea of Moonlight was to promote a feeling of safety by better connecting people with a geographical proximity. The use case driving this application was the concept of <i>someone wanting someone else to walk them to their car after a late lecture</i>. The key target was an application that would allow people to feel safer.

<h2>Early Idea Development</h2>
The course coordinator was contacted early in the development process for feedback. Key areas of focus were isolated from this feedback (emphasis added to quote).

</br><q>
Yes, I would say that is in the problem domain. Establishing trust & ensuring safety are definite challenges for community-based applications - especially communities where people <b>don't already know each other socially</b>. 
Exploring the concept of trust/safety would be interesting - though you would want to <b>focus on a particular sector/area</b> (ie. communities connecting strangers) to help constrain it.
</q></br></br>

From this the following requirements of the intial idea were developed:
<ul>
<li>A way to develop trust between strangers</li>
<li>A way to facilitate this development of trust</li>
</ul>

<h2>Group Work 1</h2>
Initial connection with the group was made, and the idea was adopted. During the first week of discussion, the major work order was for completion of research into similar applications which was to be completed by the next week.</br>
The group also decided that the security of the application was a critical feature that required exploring. It was decided that the security aspects of the application be investigated in parallel to the research component.

<h2>Security Features</h2>
<h3>Government ID</h3>
The first stage of development required determining a set of features that would provide "safety" in the context of the applications usage. After studying research by information security experts regarding abuse of systems, the <i>identity</i> component of the application was found to be the key to the safety.</br>
If all users (not the accounts of the users, but the users themselves) of the application could be uniquely identified, then any offence would be tied to them as a person, meaning they would not have anonymity. Research revealed this anonymity was a key cause of abuse. Research was then conducted to determine the best way to do this.</br>

<h4>Research</h4>
It was found that as part of a </i>100 points of identification</i> scheme introduced to prevent money laundering in Australia, many financial institutions are required to collect a government ID. This included many fully online sites, trading in currencies such as Bitcoin. This did not deter usage by users. It was also found that other peer to peer applications exist where such a Government ID is required, such as Uber. This positively supported the inclusion of this as a feature for preventing anonymity.

<h4>Reception</h4>
Interviews conducted with users during the term showed users would be willing to upload a government ID, as long as the application was secure, and would not disclose this. Comments were made comparing this process to Uber, showing that people are already open to authentication such as this through Uber.

<h4>Integration</h4>
This feature was then accepted as an addition. The signup process would require that before an account could perform any functions involving interaction with other users, an ID would need to be uploaded. This could easily be performed from any mobile device with a reasonable resolution camera. Existing solutions already exist that would allow this to automatically be verified.

<h3>Trustmark</h3>
Once identity is positively established. Then an objective rating system can be applied that ensures no abuse will go unpunished. Due to the nature of the application, and the dangers associated, it was decided that any abuse could not be forgiven, and would need to result in a permanent ban.</br>
This resulted in the concept of a <i>TrustMark</i>. This is associated with each user, and is a sign that a user has not committed any offence, and has uploaded a government ID. This would be revoked if any abuse was committed.</br>

<h4>Development</h4>
The idea of the trust mark was further developed by creating a set of criteria that must be met to ensure that a TrustMark would be retained. These were made as objective as possible to reduce the scope for abuse. The initial criteria decided on were:
<ol>
<li>My helper openly offered his trust mark</li>
<li>My helper tried to help me</li> 
<li>My helper was polite</li>
<li>My helper did not make any unwanted requests or advances</li>
<li>My helper respected me and my beliefs</li>
<li>My helper requested consent before engaging in any activity that involved physical interaction</li>
<li>My helper did not request I connect with them later</li>
</ol>

<h4>Reception</h4>
It was found during prototyping that users liked the idea of a TrustMark and found most of the criteria agreable. However, the criteria <i>my helper requested consent before engaging in any activity that involved physical interaction</i> was flagged as unnecessary by users, as if the help request was for this type of activity, it would be implicit.
</br>
<table>
<tr><td>
<h6>Changes on the Rate My Helper interface</h6>
</td></tr>
<tr><td>
<a href="http://rft.io/deco3500/overview/change01.png"><img src="http://rft.io/deco3500/overview/change01.png"></img></a></br>
</td></tr>
</table>

<h4>Integration</h4>
This feature was accepted as an addition, pending removal of criteria 6. It was found that users felt the system was objective, so no abuse marshaling would be required outside of an avenue to contest the assessment (if it would result in your TrustMark being revoked).

<h3>Interaction Recording</h3>
Another idea staged was the ability to record the audio of an interaction for later use if a user wanted to prove they had been falsely accused of not adhering to the Moonlight guidelines. This was to prevent abuse whereby a helper or helpee leave a negative rating and results in the offender having their TrustMark revoked.

<h4>Research</h4>
Research revealed there may be legal implications of performing this recording. Firstly, both parties would need to consent to the recording, meaning one party could block the recording if they desired. In addition, it was found that recordings would need to be treated securely. This could be resolved through a consent screen in the application itself, along with a policy to only send recordings if there is a contest of the review.

<h4>Reception</h4>
The reception was overall positive. During the prototyping stage, everyone indicated they would opt to record the interaction, and that they believed it was a good security feature. However, it was also observed that people already felt secure before the recording option was presented.

<h4>Integration</h4>
It was decided that due to the challenges posed such as privacy and storage space, and the simplicity needed to subvert this security measure, a decision made to omit this feature in the high fidelity prototype. See <a href="#changes-on-the-rate-my-helper-interface">initial inclusion on the mockups</a>.

<h3>MLSec</h3>
The underlying security mechanism of the application was then developed. After obtaining someone's identity, whenever a help request was actioned, the ID of the helper and helpee would be transmitted online. This would ensure that if any offence were to be committed during assistance, the helper could be contacted for information by law enforcement. This would prevent convenience predation, as it would introduce a barrier, and significantly increase the risk of being caught. 

In addition, before helpers could connect, the helpee would be required to scan the helper's barcode, which would prove the responder was the correct responder, preventing people attempting to target people using the application. A photo would also be displayed during this process to prevent phone theft.

<h4>Reception</h4>
It was found that people implicitly accepted the security of the application without being aware of the prescence of the transparent security features of the application. When they manifested in a user facing form, such as the "Scan code to verify your helper" interface, people did not find this to reduce accessibility, and understood the security premise.
</br>
<table>
<tr><td>
<h6>MLSec Mockup Implementation</h6>
</td></tr>
<tr><td>
<a href="http://rft.io/deco3500/overview/feature03.png"><img src="http://rft.io/deco3500/overview/feature03.png"></img></a></br>
</td></tr>
</table>

<h4>Integration</h4>
These features were accepted for addition into the application without requiring changes. 

<h2>Initial Interviews</h2>
See also <a href="https://github.com/deco3500-2017/-/blob/master/2_Initial_Interviews_20170822.md">initial interviews</a>
Initial interviews were conducted in parallel to the initial development of security features of the application. These were designed to determine peoples views on safety as a whole, and if there had been times in their lives they had felt vulnerable. Also to determine if there were any contributing or mitigating factors to this.

<h3>Results</h3>
It was found that all people surveyed had experiences in their lives that had left them feeling vulnerable. Many were at night, in times where they were alone. Areas quoted such as bridges or walkways were common.</br>

People also indicated that in general there was nothing other than getting to know someone that would promote trust. But, it is sometimes possible from a distance to determine if someone is untrustworthy, through body language.

When probed for trusted people in their lives, and what made them trustworthy, there was mention of qualities such as kindness/caring. 

Finally, people indicated that it would be unlikely they would trust a stranger for an interaction such as <i>walking them to their car.</i>

<h3>Evaluation</h3>
Initial interviews indicated strongly that developing an application such as Moonlight to facilitate trust would not be trivial. From interviews, it was clear that one of the only factors that would actually develop this trust was getting to know a person over a time period greater than the one expected during an app managed interaction. It was decided that the best approach to continue would be to perform in-depth research into literature surrounding trust, to determine what factors could be changed to promote people to trust strangers.

<h2>Application intent shift</h2>
The intent of the application as a result of the first round of interviews and discussion was shifted. Initially, the application was specifically catering to safety in situations where people felt unsafe. However, it was discovered that the need for assistance was more general than just assistance with safety. 

It was decided that a "general assistance" feature should be trialed, that would allow people to request assistance in a 1:1 context, with one helper and one receiver. This was a large shift but would extend the use case of the application outside the very narrow 'emergency' use case.

The motivation behind this was to ensure there would be a reason for 'helpers' to use the application. Helpees have an incentive to use the application to use the application because they receive help. However, a helper may not need to request help, and due to the situations when people feel unsafe (mostly late, and empty areas), it is likely many helpers would not be able to help others. This would prevent the application from gaining traction (reducing its usefulness), as helpers would not be motivated to sign up.

To resolve this issue, by introducing a general assistance section, all users will be exposed to help requests and can request help in a wider context, which would promote general usage. A pre-release could also be conducted to ensure that there would be enough supply to meet demand. 

<h2>Trust research</h2>
Following the interviews extensive research into trust was conducted. See also <a href="https://github.com/deco3500-2017/-#building-and-establishing-trust-">building and establishing trust</a>.

Research revealed the key components of trust were that the trustor is vulnerable to the trustee, that the trustor thinks well of the trustee in some domain, that the trustor is optimistic the trustee is competent in some respect, and that the trustor is optimistic the trustee will have a certain motive for acting.

This was discussed in the context of Moonlight and key areas for improvement were identified.

<ol>
<li>Trust is a byproduct of vulnerability, as such the application cannot completely remove vulnerability if trust is to be developed.</li>
<li>The motivation (or expected motivation) of the trustee has to be in line with what the trustor wants it to be.</li>
</ol>

<h4>Safety vs Trust</h4>
The first of these caused a change in the direction of the design. Initially the application was meant to directly build trust, however, it was realized after research, and the information collected in initial interviews, that trust was not something that could be directly formed through an application without risk, and required that the helpee first accept some level of risk. Because of this, we decided to shift the design in the direction of creating a <b>safe</b> environment, where trust could form naturally, note the distinction between safety and trust.

Trust is defined as (although a definition of trust is difficult) a <i>firm reliance on the integrity, ability, or character of a person or thing</i> whereas safety is defined as <i>the condition of being safe; freedom from danger, risk, or injury</i>. By ensuring people are physically safe, the natural formation of trust can be promoted through the application.

<h4>Motivations behind Helping</h4>
It was also realized that a key motivation of using the application for many people would be for social connection. A helper may help someone in order to connect socially, as a helpee may request help for the same reason. Because of this, it was identified that the final condition of trust, that a trustee's motivation is in line with the trustor's expectation, may not always be satisfied.

This caused a significant design change in two areas of the application. The first was the connections interface. The connections interface is a feature that allows helper and helpee to reconnect a later time if they felt a connection.

<h5>Types of Connection</h5>
Further research revealed that in a broad sense connections could be broken into four key categories:
<ul>
  <li>Friendship - for example <i>a friend group</i></li>
  <li>Romantic Relationships - for example <i>a married couple</i></li>
  <li>Professional Relationships - for example <i>a mentor and mentee</i> / <i>professional networks</i></li>
  <li>Intellectual / Activity Partners - for example <i>study mates</i> / <i>sports teams</i> / <i>research teams</i></li>
</ul>

Although intellectual relationships and activity partners are more situational then dispositionally based, they would allow reconnection on the grounds of similar interests, where friendship would not necessarily need to be considered. For example reconnecting with a helper who offered to help with learning a certain skill.

<h5>Implementation</h5>
The idea behind the connections interface is that if people share a mutual type of connection they can reconnect, and they will receive a notification of the connection. If they do not, they will not be notified. This allows people to extend an offer for a connection in the area the person truly wants to reconnect in, without the risk of judgement if this is not reciprocated.

There was a debate about the importance of this for the Moonlight application, which was resolved by breaking down the use cases of the application wrt/ people using the application for a social outlet.

<b>Both users are not using the application as a social outlet</b></br>
Both users expect the other user is using the application in the same context as them, satisfying the final condition of trust. The connections interface will not pose an issue as if they want to reconnect they can, but they are under no pressure to do so.

<b>One user is using for social connection, the other is not</b></br>
Both users expect the other user is using the application in the same context as them, however, each is <i>truly</i> using it within a different context. The application policy mandates that one user cannot request another user 'reconnect' with them (with the justification of safety), See <a href="#changes-on-the-rate-my-helper-interface">feature on TrustMark mockup</a>. So although there is a different intent behind the usage, this will not become apparent to the non-social user, so the fourth condition of trust is still satisfied. Finally, on reaching the connection interface, the social context user can still use this outlet, and the non-social user can make a non-pressured decision about how they feel, potentially satisfying the usage intent of the social user. 

<b>Both users are using the application as a social outlet</b></br>
Both users expect the other user is using the application in the same context as them, satisfying the final condition of trust. The connection interface will allow both users to reconnect if desired, potentially satisfying both their usage intents.

In addition. It is possible two social users will be looking for a different type of connection. By offering the connection categories discussed above, it prevents two users reconnecting with different intents, which could create a negative feeling which would be associated with the application.

<h5>Reception</h5>
In user testing conducted with mockups, users responded that they liked the idea of the feature, however, felt uncomfortable with the terminology used for 'romantic relationships'. Female users expressed that this made the application feel 'sleazy', and that it made them uncomfortable.</br>

It was identified that the reason behind this was the terminology used itself. A variety of different terms were trialed, and finally, it was settled that 'Felt a deeper connection' did not have negative connotations, and did not elicit a negative response.

High fidelity testing with this change implemented showed that the reception of the feature was very positive, and the previous reservations about the terminology had been resolved.
</br>
<table>
<tr><td>
<h6>Changes on the Connections Interface</h6>
</td></tr>
<tr><td>
<a href="http://rft.io/deco3500/overview/change02.png"><img src="http://rft.io/deco3500/overview/change02.png"></img></a></br>
</td></tr>
</table>

<h2>Social Usage</h2>
Further discussion promoted the idea that users primarily using the application for a social outlet could be specifically catered to by providing a 'lobby' service for people looking to reach out and have a conversation. This would also have a positive social effect, with many depression campaigns and wellness campaigns promoting the idea of reaching out if you need to talk.

However, due to the social stigmas associated with engaging conversations with stranger's this is not always possible. This application could provide a judgement-free environment to facilitate this, where a positive and judgement-free environment could be enforced through the TrustMark. This would provide a unique opportunity to bundle the utility of general assistance, along with the potential benefits of social assistance (feeling like there is always someone there, no matter what type of help is required).

<h3>Implementation</h3>
This feature manifested in the 'Hello' feature set. The helo feature set would function in a similar way to help requests, although would only match a user with other people in the area also using the Hello feature. This would be opt in however, with the possibility of subscribing to these events even if you were not using the feature itself directly.
</br>
<table>
<tr><td>
<h6>Primary Features Exposed by Application</h6>
</td></tr>
<tr><td>
<a href="http://rft.io/deco3500/overview/feature04.png"><img src="http://rft.io/deco3500/overview/feature04.png"></img></a></br>
</td></tr>
</table>

<h3>Reception</h3>
Reception for this feature was overwhelmingly positive, with many testers using, or indicating that they would use this feature before using the assistance feature. The initial expansions tested such as conversation starters in application (during the mockups stage)  Although this was not the primary target feature for development, it poses an interesting avenue to explore in greater detail.

<h2>Second Round Interviews</h2>
A second round of interviews were conducted, and this revealed a number of changes that would be required as well as providing valuable insight.

At this stage many of the earlier worries and pain points had already been removed. However, there was still refinement. One particular area of concern expressed by many users was the assistance request "same sex / same nationality" option, which would allow users to request help from someone of the same gender or same nationality. Users stated that they felt uncomfortable with this in the assistance screen. However, users did state that for the 'Helo' / social request, this would be a useful feature.

</br>
<table>
<tr><td>
<h6>Changes to assistance request</h6>
</td></tr>
<tr><td>
<a href="http://rft.io/deco3500/overview/change05.png"><img src="http://rft.io/deco3500/overview/change05.png"></img></a></br>
</td></tr>
</table>

<h2>Continuing design processs</h2>
The design process was continued in a similar fashion, conducting high fidelity prototypes, and conducting and synthesising new research. This continued until the demonstration, where a fully functioning demo prototype was made available for people to use. The feedback during testing at the showcase was very promising.
