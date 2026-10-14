# SOP: Build and edit Facebook ads through GHL

Owner: Growth Factor. Procedure based on the October 2026 GHL workflow; labels and available controls may change. Recheck the live interface rather than treating this document as an API reference.

## 1. Establish the brief and access

Record the business/sub-account, Meta ad account, Page and Instagram identity, objective, campaign and ad set names, daily or lifetime budget and its level, schedule/time zone, audience, placements, assets, copy, CTA, destination, and requested final status.

For edits, record the exact campaign/ad set/ad and requested before/after change. Resolve ambiguity that could affect a live campaign before changing it. A draft duplicate is appropriate when requested; do not overwrite a live original merely to prepare a proposal.

Use the logged-in authorized browser when required. In GHL, select the correct location, then Marketing > Ad Manager > Meta. If the browser cannot read/click, establish which tool is available and whether the correct browser/tab is attached. Credentials alone cannot enable browser control. Request login from the user if necessary; never extract session credentials.

Use official documented API operations where available. For any API implementation, first record its verified documentation, endpoint, scopes, request shape, limitations, and date in the capability registry. An unverified operation is UNKNOWN. Browser observations do not establish that an endpoint is public or that no public API exists.

## 2. Build the campaign and ad set

Create a Meta campaign from scratch, or open the exact authorized draft. Select the objective appropriate to the brief and inspect the connected identities. Rename the campaign and ad set deliberately.

Set the budget at the intended level. A $10/day ad set shared by three ads is $10/day total, not $10 per ad. Read back currency, budget type, budget level, and any start/end dates or default schedule. Do not activate or schedule a draft-only campaign.

Configure audience age and gender. Search for the exact street address, choose the correct returned location, select miles or kilometers, and set the radius. Read back both the radius and units. Remove unintended broad included targets such as a default United States entry; do not exclude the entire country containing the intended radius. Review location-presence and expansion settings if offered and disclose any constraint the UI cannot enforce.

Choose manual placements when requested. For Ben's established preference, select only Facebook feed, stories, reels and Instagram feed, stories, reels. Inspect every category for defaults such as Marketplace, search, in-stream, right column, Explore, profile feed, Messenger, or Audience Network. Do not assume a parent checkbox means only the desired children are selected. If requested controls are unavailable, record the limitation instead of silently substituting automatic placements.

## 3. Build and duplicate the ads

Prepare one base ad with approved primary text, headline, description, CTA, identity, and destination. Choose single-image media for a one-image-per-ad comparison. Optional blank variant fields may appear automatically; verify only the intended populated variants are present.

For an image comparison, duplicate the completed base ad, rename the copies Ad 2 and Ad 3 (or the requested names), and replace only the image. Verify inherited settings on each copy. Do not create a carousel or add different copy unless the brief calls for it.

Review creative enhancements, automatic text/media variations, and multi-advertiser settings where available. Record the effective settings and avoid unrequested changes. Automatic variations can confound an intended image-only comparison.

### Media uploads

Use the browser tool's supported file chooser/upload mechanism with the supplied local files. In the observed UI, Upload media opens the library; Upload then opens a menu where Upload file starts the chooser. Arm the chooser listener before selecting that action if the runtime requires it.

Wait for the library to finish loading. An initially empty panel is not proof that the library is empty. If an upload is slow or times out, inspect progress and search for the uploaded file before retrying. Stop repeated retries when state remains unknown to avoid duplicates.

Select the correct image and re-observe the ad. Selection may close the modal automatically; a disappearing Insert button may mean the image was already attached. Verify the preview, not just the filename. Keep all supplied assets separate and inspect resolution/aspect ratio without silently redesigning them.

### Lead forms and website destinations

For “the usual form,” inspect a relevant recent campaign read-only and capture the exact selected form after the dropdown finishes loading. Match the Page, form name, and ID/date or other metadata when names repeat. If several plausible forms remain, ask which to use rather than guessing.

Select the form on every ad and reopen each saved ad to confirm it persisted. A Mapped label does not prove CRM routing, workflow execution, notifications, or lead delivery. Test those only within an authorized test scope, using an identified test lead and cleanup plan. Do not submit production leads or send notifications just to check a draft.

For website destinations, use the supplied/verified booking URL and preserve agreed tracking parameters. Do not replace a lead form with a homepage because it is easier to access.

## 4. Edit an existing ad

Capture original copy, image, destination, audience/budget settings relevant to the change, and delivery status. Confirm whether saving affects the live ad immediately in the current interface.

Apply the requested change at the correct level: campaign objective/budget, ad set audience/placements/budget, or ad creative/form. Preserve unrelated settings. For changes to a comparison test, update all intended variants consistently or explicitly document the new experimental difference.

Save and reopen the item. Compare before/after values and delivery status. Keep a record sufficient to restore the previous content; do not promise restoration of historical delivery or learning state. If save status is unclear, inspect persistence before retrying the mutation.

## 5. Verify and save the handoff

Use Review and reopen the saved campaign. Check the following against the brief:

| Check | Evidence to record |
| --- | --- |
| Account and identity | Correct GHL location, Meta account, Page, Instagram identity |
| Structure | Campaign/ad set names, expected ad count, unique ad names |
| Budget and schedule | Amount, currency, daily/lifetime, level, dates/time zone |
| Audience | Exact included location, radius/units, no unintended broad targets, ages/gender |
| Placements | Effective selected placements and any expansion limitation |
| Copy comparison | Same intended copy, CTA, and destination across image variants |
| Assets | Correct image attached to each ad |
| Destination | Saved form or URL on every ad; routing tested separately if authorized |
| Previews | Feed, story, and reel previews checked for text/logo cropping and readability |
| Status | Campaign, ad set, and each ad remain draft when requested |

Distinguish clipping in the source image, clipping in the preview pane, and actual placement cropping. Letterboxing alone is not evidence of failed upload. Report previews not checked, unavailable controls, or unclear persistence instead of marking them passed.

For draft-only work, stop before Publish, Publish campaign now, activation toggles, or scheduling. Close any publish menu accidentally opened. Record the status visible after reopening; do not infer it from having avoided one button.

Provide a short completion note with links, verified settings, ad-to-image assignments, saved status, and outstanding items. Include screenshots where useful. An ad quality score is not proof of future performance. For shared-budget comparisons, delivery may differ between ads; evaluate results using the agreed outcome and lead quality, not a presumed equal split or a few clicks. Do not automatically pause losers or raise spend without authorization.

## Browser recovery notes

- Use fresh UI snapshots after navigation, dropdown changes, debounce, or duplication. Old accessibility indices can point to different elements.
- A custom dropdown may expose only “loading” in one view while its DOM snapshot shows the selected value. Inspect current rendered state using supported tools.
- Virtualized age/options lists require scrolling to reveal choices. Verify the final value rather than assuming keyboard steps succeeded.
- Scope unlabeled controls to their observed parent. Do not guess screen coordinates, hardcode a previous session's menu IDs, or use hidden application state/private APIs.
- If a mutation fails ambiguously, check for its result before repeating it. If blocked, finish copy and the configuration brief locally and report the precise unfinished step.

## Example brief from the Nashville MMA build

This is a client-specific example, not a default for other campaigns.

| Field | Requested configuration |
| --- | --- |
| Campaign / ad set | Fitness Classes / Fitness Classes |
| Budget | $10/day total at ad set level |
| Audience | Men 18-45, 8 miles around 1504 Elm Hill Pike, Nashville, TN |
| Placements | Manual Facebook and Instagram feeds, stories, reels |
| Ads | Ad 1, Ad 2, Ad 3; one supplied image each |
| Comparison | Identical primary text, headline, description, CTA, and form |
| Destination | Existing usual lead form, verified against a relevant campaign |
| Completion | Saved drafts; no publishing |

## Reusable handoff record

Copy this record into the task's private output, not into a public skill package:

```text
Business / GHL location:
Meta account / Page / Instagram identity:
Campaign / ad set / ad links:
Requested change and final status:
Budget / currency / level / schedule:
Audience / radius / units:
Placements and expansion settings:
Primary text / headline / description / CTA:
Destination form or URL:
Ad-to-image assignments:
Original values (editing only):
Saved values and status after reopening:
Previews checked:
Delivery/routing tests actually performed:
Unverified items or blockers:
```
