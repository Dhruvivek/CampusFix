# Comparable Tools and Simpler Alternatives

Research for [issue #3](https://github.com/Dhruvivek/CampusFix/issues/3). The question: what existing tools and simpler alternatives already let students report campus problems and see what happened, and what does each do well or badly? This is input for the brief's "evaluation of alternative solutions" deliverable and for the first-version scope decision. It is evidence, not a decision.

**Today's process (for comparison):** a student writes a paper application to the HOD. Most students don't bother. The HOD wants to know who reported each problem and to see photo proof.

**How to read this:** **Fact** means it is sourced, with a citation. **Inference** means it is my reasoning and has no source behind it. Sources were fetched on 2026-10-26. I made up no statistics. Every number below is quoted from the cited source.

## At a glance

| Alternative | How reporting works | Reporter sees status? | Duplicates | Identity / anonymity | Main adoption problem |
|---|---|---|---|---|---|
| Google Form + shared Sheet | Form fields, with optional photo upload. Responses land in a Sheet | No built-in status. At most a copy of their own response | None. A human dedupes by eye in the Sheet | Configurable. A photo upload forces Google sign-in | Feedback stops at "submitted", so it looks like nothing happened (inference) |
| WhatsApp group / class rep | Free-text message plus photo to a group or rep, who passes it on | Only if someone replies in the chat | Social: people see earlier messages, if they scroll | Sender's account is visible to the group, or hidden behind the rep | Reports get buried in the chat. No record. Depends on the rep (inference) |
| Indian statutory grievance portal (UGC 2023) | Online application, then a committee, hearing and Ombudsperson | Formal: report and decision copied to the student | Not addressed | Named complainant, hearing in person or by representative | Built for disputes, so far too heavy for a broken bench (inference) |
| Campus maintenance / work-order portal (e.g. IIT Kanpur Campus Care, UNLV Rebels@Work) | Logged-in request with category, location and media | Yes, tracked status and notifications | Varies by product. Not documented in the sources | Institutional login, so identified | Login and form friction. Often aimed at staff, not students (partly inference) |
| Civic reporters (FixMyStreet, SeeClickFix) | Pin on a map, category, description, photo. Public report | Yes: public status, updates, follow/subscribe | Shown nearby or similar before you submit. Follow instead of re-reporting | Identified to the authority, optionally pseudonymous in public | Skewed, concentrated participation. Continued use depends on visible fixes |

## 1. Google Form + shared Sheet (the baseline)

**Facts**
- If a form asks for a file upload, "responders need to sign in to a Google Account", and the uploaded files go to a new Drive folder owned by the form owner. File uploads can't be used if the form is stored in a shared drive or if an admin has turned on Data Loss Prevention. The owner sets the allowed file types, the number of files and the maximum size. [Google Forms Help: file upload](https://support.google.com/docs/answer/7322334)
- "Collect email addresses" has two modes. **Verified** means respondents confirm their Google Account email is collected. **Responder input** means they type an email themselves. The owner can also send respondents "a copy of their response" either *When requested* or *Always*. [Google Forms Help: settings](https://support.google.com/docs/answer/139706)

**Inferences**
- *Reporting:* this is the cheapest option that works. It can be set up in under an hour, and a photo upload plus Verified email covers both of the HOD's demands (identity and photo proof).
- *Status:* Forms has nothing for "what happened next". The most a reporter gets is a copy of their own submission. To show status, someone has to add a status column to the Sheet and share it. Sharing the raw Sheet would expose reporters' emails and photos to everyone who can see it, so a separate filtered view would be needed.
- *Duplicates:* there is no deduplication. Ten students reporting the same broken projector make ten rows, and a person has to collapse them by hand.
- *Adoption risk:* this has the same "submit and hear nothing" shape as the paper application, just with less friction. The Sjoberg et al. finding below suggests that missing feedback is what holds back repeat reporting.

## 2. WhatsApp group / class-rep reporting

**Facts**
- WhatsApp groups support up to 1024 users. WhatsApp also offers in-chat polls and Communities, where admins can "send important updates to everyone in the Community" (announced 3 Nov 2022). [WhatsApp blog: Communities now available](https://blog.whatsapp.com/communities-now-available)
- In the OfS / Public First poll of English students (June 2025, see §4), students were "at least twice as likely" to complain informally, "such as a course representative or conversation (23 per cent)", as through formal channels (11 per cent). [OfS / Public First](https://www.officeforstudents.org.uk/media/lhrlukbb/ofs-explorations-consumer-rights.pdf)
- I found no primary source on WhatsApp reporting for campus maintenance specifically. Everything else in this section is inference.

**Inferences**
- *Reporting:* the effort is close to zero. Students already sit in class groups, and sending a photo plus "bench 3 in room 204 is broken" is natural. A class rep can collect these and pass them to staff.
- *Status:* status exists only if someone replies. There is no state per report, and the reply competes with every other message in the group.
- *Duplicates:* this is handled socially. People can see that someone already reported it, but only if the earlier message hasn't scrolled away. That gives some natural deduplication and some "+1" pressure.
- *Identity:* the sender's WhatsApp account identifies them to the group. The class rep route hides the reporter from staff but also loses the identity the HOD wants.
- *Adoption problems:* there's no durable record, so you can't answer "how many open issues are there in Block B?". Everything depends on one rep's diligence. Reports mix with social chatter, and nothing aggregates them for the HOD. **What WhatsApp does well**, though, is low friction and photos by default. Those are the traits CampusFix should try to match.

## 3. Campus grievance and maintenance portals

### 3a. Statutory student grievance portals (India)

**Facts** (from [UGC (Redressal of Grievances of Students) Regulations, 2023, Gazette of India](https://www.ugc.gov.in/pdfnews/4675881_Regulation.pdf))
- These rules apply to universities, deemed universities and colleges under the UGC Act. "Grievance" covers 18 categories. Category xi is "failure by the institution to provide student amenities as set out in the prospectus" (Reg. 3(1)(f)).
- "Each institution shall, within a period of three months from the date of issue of this notification, have an online portal where any aggrieved student may submit an application seeking redressal of grievance." The institution has to refer each complaint to the Students' Grievance Redressal Committee (SGRC) "within 15 days" (Reg. 8(i)–(ii)).
- The SGRC is a Professor as Chairperson plus four senior faculty members. It fixes a hearing date, and it sends its report "to the competent authority… and a copy thereof to the aggrieved student, preferably within a period of 15 working days". Students can appeal to an Ombudsperson, who should resolve the matter within 30 days (Regs. 5, 7(iv), 8(iii)).

**Inferences**
- Your college probably already has a mandated grievance portal, so check whether one exists before building anything. It is designed for disputes between a student and the institution (admissions, fees, discrimination, evaluation), with hearings and natural-justice procedure. Using it for "a bench is broken" would be badly disproportionate. It doesn't deduplicate. Status is formal and slow, measured in weeks. The complainant is named.
- It is useful as a frame, though. Category xi (amenities) means classroom facilities are arguably within the grievance scope, which gives CampusFix a legitimacy argument with the HOD.

### 3b. Campus maintenance / work-order portals

**Facts**
- **IIT Kanpur, Campus Care:** a smartphone complaint system connecting users with the maintenance team for civil, electrical, AC, water supply, telephone and network issues. "Users can lodge a request/complaint through text input, audio, or video mode", with GPS-based location. Minor complaints go through Pingala / Campus Care, and major works go through a separate "DOIP 101" work requisition for institute employees. [IIT Kanpur DoIP: Campus Care](https://iitk.ac.in/doip/campus-care)
- **UNLV, Rebels@Work** (a US university, running on WebTMA): login with university credentials, fill in a service request form, and get "automatic notifications and status updates throughout the process". [UNLV Facilities: Rebels@Work](https://unlv.edu/facilities/rebels-work)

**Inferences**
- *What these do well:* tracked status, routing to the right trade, and media attachments. IIT Kanpur's page says video describes some problems better than text.
- *What they do badly for CampusFix's case:* they are institution-wide, need IT and procurement buy-in, and are often built around staff work orders. Each reporter files in isolation, so none of the sources show public visibility of other people's reports, and duplicate handling isn't documented. None of this can be bought or deployed by one department in one week.
- *Student sentiment:* a student newsletter at IIT Patna (Forthright, 14 Jul 2022) complained that "hardly do you see any visible change from such hefty mechanisms" and of a "lack of any visible impact or clarity in what happens afterward". This is opinion, not data, but it fits the visibility theme. [Forthright IIT Patna: "Feedback – What's the Point?"](https://forthrightiitp.substack.com/p/feedback-whats-the-point)

## 4. Civic issue reporters

### FixMyStreet (mySociety, UK; open-source platform)

**Facts**
- *Platform:* "Open source report-mapping software… flexible enough to fit any project that matches geographical points to email addresses." [fixmystreet.org](https://fixmystreet.org/)
- *Identity:* the report and your name and contact details go to the responsible body. On the public site, "Your email address and phone number are not published, and your name is only published if you have opted to do so." Reporters can anonymise past reports. A report isn't sent until the reporter clicks a confirmation email. [FixMyStreet privacy](https://www.fixmystreet.com/about/privacy)
- *Status and feedback:* by default, "four weeks after a user reports a problem, FixMyStreet sends an email" survey asking about the problem's state, for example whether it's fixed. If it isn't confirmed fixed, the reporter can opt in to another survey four weeks later. [FixMyStreet Platform: surveys](https://fixmystreet.org/running/surveys/) Council replies normally go straight to the reporter's email, "outside the FixMyStreet system", unless the council has integrated, in which case responses appear on the report page. [FixMyStreet privacy](https://www.fixmystreet.com/about/privacy)
- *Duplicates:* existing pins are visible on the map. A feature that "checks to see if there are any other open reports in the same category within a small radius" shows likely duplicates, and the user can subscribe to an existing one instead of filing a new report. [mySociety blog, 24 Apr 2019](https://www.mysociety.org/2019/04/24/stop-right-there-thats-already-been-reported/) The radius defaulted to 250 m and FixMyStreet Pro clients can now customise it, including per category. [SocietyWorks, 25 May 2023](https://www.societyworks.org/2023/05/25/the-duplicate-report-suggestion-radius-on-fixmystreet-pro-is-now-customisable/)

### SeeClickFix (CivicPlus 311 CRM, US)

**Facts**
- *Identity:* you can "submit a request anonymously" or create a free account. With an account you get updates automatically. If you report anonymously you have to check the site yourself. Public requests stay on the map "until they are closed". [City of Bellingham SeeClickFix FAQ](https://cob.org/about/contacts/report/seeclickfix-frequently-asked-questions) (this is a city deployment FAQ, not CivicPlus's own documentation)
- *Duplicates and staff tools:* the vendor lists "Automatically detect duplicate requests before they are submitted" and "Internal comments for staff… without public visibility". [CivicPlus: SeeClickFix 311 CRM unified platform](https://www.civicplus.com/seeclickfix-311-crm/unified-platform/)
- *Community signals:* residents can comment on and "vote to fix" issues reported by others. Voting needs an email address. [Raleigh LocalWiki: SeeClickFix instructions](https://localwiki.org/raleigh/SeeClickFix_Instructions) (a community wiki, a weaker source)
- *Interop standard:* Open311 GeoReport v2, which civic reporting systems use to exchange requests, defines only two statuses, `open` and `closed`. Photos are an optional `media_url`, reporter `email`/`first_name`/`last_name` are optional, and "Duplicate request." is used as an example `status_notes` value. [Open311 GeoReport v2](https://wiki.open311.org/GeoReport_v2/)

### Adoption evidence (published studies)

- **Responsiveness drives repeat reporting.** Sjoberg, Mellon and Peixoto studied FixMyStreet.com data (n=399,364 reports from 154,957 users): "a successful first experience using FixMyStreet.com is associated with a 57 percent increase in the probability of an individual submitting a second report". Responsiveness to the first report predicts all future submissions. Note that "fixed" was largely marked by users, and the authors run checks that exclude self-reported fixes. *Public Administration Review* (2017). [Author copy, Oxford ORA](https://ora.ox.ac.uk/objects/uuid:2bd169fd-0b27-46e4-8b81-1ccfccf7c55a/files/ma5b19b3d0c0005e21d0bc3e457691bf5)
- **Participation is concentrated.** On FixMyStreet, "The top 0.1% of users made 16% of the reports and 10% of users account for 62%". "Two-thirds of users made only one report", and those reports are 20% of the total. [mySociety, 20 Aug 2019](https://www.mysociety.org/2019/08/20/super-contributors-and-power-laws/)
- **Participation is skewed.** Across civic tech in the US and UK, users "tend to be above the age of 45 (over 70%) and well educated". Generally more men than women use it, and ethnic minorities are under-represented. [Rumbul, mySociety, "Who Benefits from Civic Technology?", Oct 2015](https://www.mysociety.org/2015/10/28/who-benefits-from-civic-technology/) A study of 30,041 FixMyStreet Brussels reports found that such platforms "tend to marginalize low-income and ethnically diverse communities". [Pak, Chua & Vande Moere, *Journal of Urban Technology* 24(2), 2017](https://ideas.repec.org/a/taf/cjutxx/v24y2017i2p65-87.html)
- **Why students don't complain (England, formal complaints, not facilities specifically).** In a poll of 2,001 students by Public First for the Office for Students, the biggest barriers were doubt "that it would make a difference (36 per cent)" and "a lack of time or energy to go through the process (35 per cent)". Students were "at least twice as likely" to complain through informal channels, "such as a course representative or conversation (23 per cent)", as through formal ones (11 per cent). [OfS / Public First, June 2025](https://www.officeforstudents.org.uk/media/lhrlukbb/ofs-explorations-consumer-rights.pdf)

**Inferences**
- Civic reporters are the closest match to "report and see what happened". Their key patterns are: show existing reports before submitting, let people follow instead of duplicating, keep the reporter identified to the authority but optionally pseudonymous in public, and close the loop by asking the reporter whether it's fixed.
- What they do badly, at least for this context: they are city-scale, map-centric products. A pin on a map is less useful inside one building than "Room 204, bench 3". Their engagement is heavily concentrated in a few super-users, and their status depends on the authority actually updating it.

## Cross-cutting takeaways

1. **The feedback loop is the main adoption lever.** One fact supports this directly: the 57% repeat-reporting effect. The OfS barrier data (36% "won't make a difference") and the IIT Patna student piece back it up indirectly. Every low-tech option here, including the paper application, Forms and WhatsApp, fails on this point. *(Fact plus inference.)*
2. **Friction is the second lever.** The 35% "time or energy" barrier counts as a fact, but it comes from a different context. WhatsApp's success is mine to infer from that.
3. **"Identified to the authority, pseudonymous to peers" is an established pattern** (FixMyStreet). It reconciles the HOD's need for identity with students' fear of consequences. In the OfS focus groups, some students "mentioned feeling intimidated or fearing repercussions". A secondary [Wonkhe summary](https://wonkhe.com/blogs/students-dont-think-anything-will-change-theyre-probably-right/) puts poll figures of about a quarter on this, but I could not find them in the report text, possibly because they are only in a chart.
4. **Deduplication works best at the moment of reporting.** Showing similar open reports, with "follow" or "+1" in place of a new report, beats merging after the fact.

## Gaps and limitations

- Indian civic apps (e.g. municipal grievance apps) were not investigated. There is no primary data here on adoption of campus complaint systems in India.
- No source gave duplicate handling for campus work-order portals.
- The SeeClickFix sources are a city FAQ, the vendor's marketing page and a community wiki, not product documentation.
- The OfS figures come from English higher education and are about formal complaints. Treat them as directional only for an Indian department.

## Implications for CampusFix v1 (considerations, not decisions)

- **Status visibility is the feature that sets CampusFix apart.** A Google Form already covers "submit with photo and identity". For v1 to beat the baseline, it should probably show reporters (and maybe peers) a status per report, even one as simple as Open → Acknowledged → Fixed. A reply to the reporter when the status changes also matters.
- **Consider showing open issues for the same room before submitting**, with a "me too / follow" action. This dedupes cheaply and gives a demand signal (how many students care) without any matching algorithm.
- **Consider splitting identity:** the reporter is identified to the HOD and staff (meeting the HOD's requirement), while the name is hidden from other students by default.
- **Location could be room plus item, not a map.** One department is a few rooms, so a picker such as room → asset/category is likely faster and more precise than GPS or pins (inference).
- **Match WhatsApp's friction level.** The photo should be the first step, with few required fields, and it should work on a phone. Requiring a separate account may cost reports. A college Google login, if one exists, may already be acceptable.
- **A Form + Sheet prototype is a legitimate first test** for the evaluation deliverable. It could check whether students report more once friction drops, before a custom build is justified. Its known weakness, no feedback loop, is exactly what a later iteration would fix.
- **Check whether the college already runs a UGC-mandated grievance portal.** Position CampusFix as the lightweight facilities route that sits beside it, not as a replacement.
- **Watch for concentrated participation.** Expect a few heavy reporters, such as class reps, and don't read report counts as student-wide demand.
