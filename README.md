# Dotted Map but I removed alaska.

Adds ``USA-NO-ALASKA`` country thats just the USA but without alaska because I think it looks better. Went out of my way to make this for the [NixLabs](https://nixlabs.dev) website


## How to use
```ts

const map = new DottedMap({
  height: 60,
  grid: "diagonal",
  countries: ["USA-NO-ALASKA"],
});

map.addPin({
  lat: 36.8001514,
  lng: -87.5445827,
  svgOptions: { color: "#9f5afd", radius: 0.4 },
});
map.addPin({
  lat: 48.8534,
  lng: 2.3488,
  svgOptions: { color: "#fffcf2", radius: 0.4 },
});

const svgMap = map.getSVG({
  radius: 0.22,
  color: "#FAFAFA40",
  shape: "circle",
  backgroundColor: "#00000000",
});

// Do whatever you want with the SVG
// For example: Render it in ReactJS

return (
  <div
    className="p-4 rounded-2xl"
    dangerouslySetInnerHTML={{ __html: svgMap }}
  ></div>
);

// Dont actually use that code, its probably dangerous, maybe one day ill come up with a better way to do it (or you can and make a PR)
```


Not my original code, check out the OG author as he's super cool [blog](https://ntag.fr/tron-like-maps/) and [og repo](https://github.com/NTag/dotted-map)
