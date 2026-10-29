# VHERE Demo FAQ

[Overview](../README.md) · [User manual](MANUAL.md)

### What does VHERE navigate with?

Camera observations are localized against a prepared visual map. The app presents the resulting position in a road/lane view and uses phone observations for assistance and continuity.

### Does the phone need an RTK receiver?

No connected RTK receiver is required for normal demo use. RTK supports map preparation; the phone uses its camera, system position, and available speed/course observations at runtime.

### Is this entirely GNSS-free?

No. Visual geometry is central to localization, but the current product uses phone location for initialization, reference search, and fallback.

### Is this a complete route planner?

The current demo focuses on positioning and road/lane visualization. Full route planning and turn-by-turn voice guidance are outside its scope.

### Can it work anywhere roads are visible?

It requires a prepared area and compatible service. A visible display road may lack suitable visual references, and changes in viewpoint, lighting, or appearance may still cause rejection.

### What works without a network?

Packaged or cached road scenes can be displayed. New server-side visual localization requires connectivity. Phone positioning depends on valid system observations; scene browsing alone is not offline visual localization.

### Why is the image rate different from the result rate?

Capture, submission, and solving have separate cadences. One outstanding request, service admission, network conditions, rejection, and timeout can all affect the result rate. Evaluate the complete phone-to-terminal-result path.

### Why can the vehicle keep moving after a rejected image?

A previous visual anchor may remain valid and be updated with fresh phone motion. Phone positioning can take over after visual expiry. Continuous display does not mean every new image was accepted.

### Is `Lane unknown` an error?

Not necessarily. The road may be identifiable while adjacent lanes remain ambiguous. The app preserves that uncertainty.

### Does a road-aligned vehicle prove accurate orientation?

It demonstrates display behavior. Vehicle heading is constrained by the current road and motion state. Camera-orientation accuracy requires independent comparison of the original estimate with an appropriate reference.

### Is lane-level or centimeter-level accuracy guaranteed?

There is no universal accuracy guarantee in this demo. Results need a specified map, device, scene, sample set, and independent reference, including rejection and large accepted errors.

### Can this repository start the complete system?

No. It distributes a signed demo APK, documentation and selected derived evidence. The numerical service is operated separately; full source, model weights, reference maps and access tokens are not included. See [service access](SERVICE.md).

### What does final availability include?

It includes valid phone fallback and supported motion between visual anchors. It measures usable final position over the full evaluation time, rather than the fraction of camera images producing a visual estimate. Final error must be reported on the same output stream and with its evaluation scope stated.
