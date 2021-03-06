# gpgs.videos.loadCapabilities()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.videos.*][plugin.gpgs-v2.videos]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Retrieves the video capabilities of the service, whether the mic or front-facing camera are supported, if the service can write to external storage, and what capture modes and quality levels are available.

## Syntax

	gpgs.videos.loadCapabilities(listener)

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [loadCapabilities][plugin.gpgs-v2.videos.event.loadCapabilities] event.