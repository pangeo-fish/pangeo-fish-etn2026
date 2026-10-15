# Your fish in a future ocean with GFTS

The maps you have just computed in the [pangeo-fish notebook](pangeo-fish) tell you where the fish probably was in the past. The **Global Fish Tracking Service (GFTS)**, a [Destination Earth](https://destination-earth.eu) use case, takes the next step: it uses the same Pangeo-Fish method and the same HEALPix grid, and shows the reconstructed tracks together with the sea temperatures projected by the Destination Earth Climate Change Adaptation Digital Twin for 2025–2039. You can then ask: *will the places my fish used stay within the temperatures it experienced?*

**What you computed is what GFTS needs.** The results of the notebook are saved in your output folder (printed in its section 10): `states.zarr` (the probability of presence at each time step) and `trajectories.parq` (the mean and mode tracks). With these files, your fish can be added to GFTS and compared with future temperatures.

**Try it after the workshop:**

1. Register on the [Destination Earth Platform](https://platform.destine.eu) (free account).
2. Open the [GFTS dashboard](https://gfts.destine.eu) and sign in with your Destination Earth account. Explore the sea bass and pollack tracks already there and the projected temperatures in their habitat.
3. Read more in the [GFTS documentation](https://destination-earth.github.io/DestinE_ESA_GFTS).

### We are looking for collaborations

Do you have archival (DST) or acoustic tags and would like to see your fish in GFTS? We would like to analyse more species and regions with you. Open an issue in the [GFTS repository](https://github.com/destination-earth/DestinE_ESA_GFTS/issues/new) and tell us briefly:

- that you heard about GFTS at the ETN Symposium 2026,
- which species and region your tags cover, how many tags, and which type (archival, acoustic, both),
- that you would like to analyse your fish with Pangeo-Fish and use GFTS.

If you cannot open the GFTS dashboard after registering, say so in the same issue and we will help you get access.
