# Web Search Playbook

Use this when a web-search agent must cut through marketing noise and decode ambiguous tech product claims.

## Source Priority

Use sources in this order:

1. Official product page for the exact claim and footnotes.
2. Official tech specs, compare pages, PDFs, manuals, support pages, compatibility lists, and configurators.
3. Checkout/configuration flow for what can actually be bought together.
4. Standards bodies, glossary pages, academic/engineering references, regulatory agencies, and component suppliers for term meaning.
5. Independent reviews with measurements, not only impressions.
6. Teardowns, repair databases, FCC/EU/energy filings, benchmark databases, and community reports for hidden hardware or sustained behavior.
7. News, launch coverage, and affiliate pages only for pointers; do not rely on them when they repeat vendor copy.

## Query Progression

Start narrow, then translate:

1. Exact claim query:
   - `"<product>" "<exact marketing phrase>"`
   - `"<product>" "up to" "<number>"`
   - `"<product>" "<feature name>" footnote`

2. Primary-source query:
   - `site:<vendor-domain> "<product>" specifications`
   - `site:<vendor-domain> "<product>" support "<feature>"`
   - `site:<vendor-domain> "<product>" "terms" OR "legal"`
   - `site:<vendor-domain> "<product>" "compare"`
   - `site:<vendor-domain> "<product>" "manual" filetype:pdf`

3. Configuration query:
   - `"<product>" configurator "<claim>"`
   - `"<product>" trim range wheels tires`
   - `"<product>" starting at price configuration`
   - `"<product>" compatibility list "<feature>"`

4. Term meaning query:
   - `"<marketing term>" meaning`
   - `"<marketing term>" vs "<standard term>"`
   - `"<marketing term>" actual refresh rate`
   - `"<marketing term>" panel type`
   - `"<marketing term>" sensor size mm`
   - `"<marketing term>" typical brightness`

5. Independent measurement query:
   - `"<product>" review measured "<metric>"`
   - `"<product>" sustained performance test`
   - `"<product>" battery test "<workload>"`
   - `"<product>" display brightness full screen`
   - `"<product>" camera sensor size teardown`
   - `"<product>" optical zoom focal length`

6. Contradiction query:
   - `"<product>" "<claim>" misleading`
   - `"<product>" "<feature>" not exclusive`
   - `"<product>" "<feature>" older models`
   - `"<product>" "<claim>" reddit`
   - `"<product>" "<claim>" forum`

## Search Tactics By Claim Type

### "Up To" Performance Or Battery

Search for the benchmark name, workload, baseline device, power mode, thermal mode, and exact configuration. If the vendor gives only a multiplier, search for measured tests in the user's workload.

Good searches:
- `"<chip/product>" "up to 2x faster" benchmark baseline`
- `"<product>" performance review previous generation`
- `"<product>" battery test gaming`
- `"<product>" sustained performance throttling`

Reject conclusions that do not identify the baseline and workload.

### Imaginary Spec Or Starting Price

Search the configurator and spec tables. Try to recreate the advertised bundle. Verify whether maximum range, fastest acceleration, largest memory, best screen, and lowest price coexist.

Good searches:
- `"<product>" starting at price max range configuration`
- `"<product>" trims specs price`
- `"<product>" compare configurations`

Report the cheapest configuration that gets the claimed feature and the feature set at the advertised starting price.

### Invented Or Branded Terms

Search the term without the product first. Then search term plus product. This prevents the vendor's page from defining the term in its own interest.

Good searches:
- `"<term>" standard meaning`
- `"<term>" actual specification`
- `"<term>" vs "<standard spec>"`
- `"<term>" marketing term`

Translate the term into a buyer-relevant standard measurement: RAM amount, VRAM amount, panel refresh rate, panel technology, sensor dimensions, optical focal length, full-screen brightness, sustained watts, or real compatibility.

### Software Features

Search whether the feature is exclusive, third-party, region-limited, subscription-gated, cloud-dependent, or coming to older devices.

Good searches:
- `"<feature>" supported devices`
- `"<feature>" older models`
- `"<feature>" Google Samsung Xiaomi`
- `"<feature>" subscription required`
- `"<feature>" region availability`

Do not credit a new hardware product for a software feature unless it is exclusive, preinstalled in the target region, and available at purchase.

### Materials And Durability

Search for exact material grade, test method, and certification. Marketing adjectives are not enough.

Good searches:
- `"<product>" alloy grade`
- `"<product>" MIL-STD test`
- `"<material phrase>" alloy`
- `"<product>" scratch test Mohs`
- `"<product>" drop test independent`

Separate material prestige from user benefit: weight, rigidity, corrosion resistance, repairability, scratch resistance, shatter resistance, or heat dissipation.

### Displays

Search for typical brightness, full-screen brightness, sustained brightness, refresh rate, panel technology, dimming type, resolution in pixels, and color performance.

Good searches:
- `"<product>" typical brightness nits`
- `"<product>" full screen brightness test`
- `"<product>" peak brightness HDR window size`
- `"<TV model>" actual refresh rate motion rate`
- `"<phone>" resolution pixels 1.5K`

Prefer measured full-screen or typical numbers over peak claims.

### Cameras

Search for sensor dimensions, optical focal length, aperture, stabilization, default output resolution, optical zoom, digital zoom, and sample caveats.

Good searches:
- `"<phone>" camera sensor size mm`
- `"<phone>" optical zoom focal length`
- `"<phone>" default photo resolution`
- `"<phone>" digital zoom review samples`
- `"<campaign>" "shot on" behind the scenes`

Do not equate megapixels or maximum digital zoom with image quality.

### Demo Or "Shot On" Claims

Search behind-the-scenes pages, campaign notes, YouTube descriptions, credits, and interviews. Look for rigs, lighting, external lenses, filters, microphones, stabilization, editing, and stock footage.

Good searches:
- `"<campaign>" "shot on" behind the scenes`
- `"<product>" "shot on" rig`
- `"<product>" "shot on" external lens`
- `"<product>" sample photos stock`

Conclude what a normal buyer can reproduce with only the product.

## Term Card Method

When a term is ambiguous:

1. Write the literal assumption a buyer may make.
2. Search the term alone to identify the neutral meaning.
3. Search the term with `actual`, `standard`, `spec`, `measurement`, `vs`, and `marketing`.
4. Search the product plus the term to see the vendor-specific use.
5. Convert the term into a standard, measurable property.
6. State whether the term affects purchase value or only perception.

Example conversions:

- `motion rate` -> actual panel refresh rate in Hz plus motion interpolation.
- `unified memory` -> total shared memory available to CPU/GPU, not equivalent dedicated RAM plus VRAM.
- `QLED/ULED/QNED` -> LCD family unless source confirms OLED or self-emissive panel.
- `1-inch type sensor` -> active sensor dimensions in millimeters.
- `1.5K display` -> actual pixel resolution.
- `peak brightness` -> window size, duration, HDR/SDR mode, and typical full-screen brightness.
- `AI zoom` -> optical focal length, crop, super-resolution processing, and output detail.
- `aerospace/surgical/military grade` -> exact alloy/grade/test standard.

## Evidence Hygiene

- Record the query that found each important source.
- Capture whether a source is primary, independent measurement, user report, or repeated press coverage.
- Use current live sources for current products; include access date.
- Avoid "source laundering": five articles repeating one press release count as one source.
- If a source uses the same ambiguous term without defining it, it does not resolve the ambiguity.
- If the exact SKU or region differs, mark the evidence as partial.
