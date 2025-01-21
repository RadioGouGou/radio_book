---
orphan: true
---

# Limited area model

To support the campaign, we perform daily hindcasts of the atmospheric conditions in the campaign region.

The limited area simulations are performed with [ICON-MPI](https://gitlab.dkrz.de/icon/icon-mpim) at a horizontal resolution of 1.25km, and cover the (64W-8W,4S-24N)-area. Each daily run is initialized from the (day-7)-00h00 IFS analysis, and marched in times for 48h using the IFS forecast to update the lateral and surface boundary conditions.

For each days, animations of key variables are constructed to showcase the runs. These are available at different "zoom-levels" 1, 2 and 3, which approximately correspond to horizontal resolutions of 5.0, 2.5 and 1.25 kilometers, respectively. All animations are uploaded daily to this [publicly-accessible server](https://swiftbrowser.dkrz.de/public/dkrz_f765c92765f44c068725c0d08cc1e6c5/LAM-ORCESTRA/), and will be regularly added here as well.

The whole dataset is stored on [Levante (DKRZ)](https://docs.dkrz.de/doc/levante/index.html) and accessible on demand. It comprises of high-sampling rate 2D and 3D snapshots of key variables.

## Daily simulations

```{list-videos}
```

<script>
    let today = new Date();
    // HACK: Simulations take a while... should be available with an 8-day offset
    let week = new Date(1979, 1, 9) - new Date(1979, 1, 1);

    document.querySelectorAll("#daily-simulations .reference.external").forEach(function(link) {
        let linkDate = new Date(link.innerText);
        // HACK: This should be replaced by properly checking an index of existing simulations
        if (linkDate > (today - week)) {
            link.parentNode.removeChild(link);
        }
    });
</script>
