# Counter-Strike 2 Map Location Image Dataset (August 2024)

## Overview

This dataset contains 1.7 million images captured from 17 different Counter-Strike 2 maps (version: August 2024). Each map includes 100,000 images, making this a comprehensive collection for various uses, such as machine learning, computer vision, and more.

The images were not taken directly within Counter-Strike 2, but in the Source 2 Viewer, utilizing custom tools and scripts. This leads to certain discrepancies from the in-game visuals, which are detailed below.

## Dataset Samples

Below are sample images included in the dataset. Each image is labeled with the corresponding map name, coordinates, and view angles.

### Sample 2: de_dust2

![de_dust2 -542 2042 108 32 293 -0.558505 5.113815.jpg](dataset_samples/de_dust2%20-542%202042%20108%2032%20293%20-0.558505%205.113815.jpg)

- **Coordinates**: (-542, 2042, 108)
- **Pitch**: 32°
- **Yaw**: 293°

### Sample 3: de_dust2

![de_dust2 5 -522 105 82 53 -1.431170 0.925025.jpg](dataset_samples/de_dust2%205%20-522%20105%2082%2053%20-1.431170%200.925025.jpg)

- **Coordinates**: (5, -522, 105)
- **Pitch**: 82°
- **Yaw**: 53°

### Sample 1: de_anubis

![de_anubis 18 -1409 32 -4 29 0.069813 0.506145.jpg](dataset_samples/de_anubis%2018%20-1409%2032%20-4%2029%200.069813%200.506145.jpg)

- **Coordinates**: (18, -1409, 32)
- **Pitch**: -4°
- **Yaw**: 29°

### Sample 4: de_thera

![de_thera 601 -864 329 12 320 -0.209440 5.585054.jpg](dataset_samples/de_thera%20601%20-864%20329%2012%20320%20-0.209440%205.585054.jpg)

- **Coordinates**: (601, -864, 329)
- **Pitch**: 12°
- **Yaw**: 320°


## Content Description

### Maps Included and Their Bounds

The dataset includes images from the following 17 maps, with specified bounds for each:

- **ar_baggage**:  
  Bounds: xMin: -1000, yMin: -1300, zMin: -150, xMax: 1000, yMax: 1300, zMax: 500

- **ar_pool_day**:  
  Bounds: xMin: -670, yMin: -200, zMin: -30, xMax: 500, yMax: 1200, zMax: 200

- **ar_shoots**:  
  Bounds: xMin: -1000, yMin: -500, zMin: 0, xMax: 1000, yMax: 1600, zMax: 300

- **de_assembly**:  
  Bounds: xMin: 2000, yMin: 1800, zMin: 970, xMax: 4050, yMax: 4300, zMax: 1400

- **de_memento**:  
  Bounds: xMin: -1100, yMin: -1400, zMin: 30, xMax: 1000, yMax: 2400, zMax: 500

- **de_thera**:  
  Bounds: xMin: 600, yMin: -2600, zMin: -200, xMax: 4300, yMax: 2100, zMax: 450

- **de_mills**:  
  Bounds: xMin: -4250, yMin: -5500, zMin: -100, xMax: 0, yMax: 0, zMax: 300

- **de_mirage**:  
  Bounds: xMin: -2700, yMin: -2650, zMin: -350, xMax: 1500, yMax: 900, zMax: 150

- **de_overpass**:  
  Bounds: xMin: -4000, yMin: -3500, zMin: 0, xMax: 0, yMax: 1700, zMax: 750

- **de_vertigo**:  
  Bounds: xMin: -2700, yMin: -1600, zMin: 11500, xMax: 100, yMax: 1150, zMax: 12200

- **de_ancient**:  
  Bounds: xMin: -2300, yMin: -2600, zMin: -150, xMax: 1400, yMax: 1800, zMax: 400

- **de_inferno**:  
  Bounds: xMin: -1800, yMin: -800, zMin: -50, xMax: 2700, yMax: 3500, zMax: 500

- **de_nuke**:  
  Bounds: xMin: -3000, yMin: -2500, zMin: -760, xMax: 3500, yMax: 950, zMax: 150

- **de_anubis**:  
  Bounds: xMin: -2000, yMin: -2400, zMin: -180, xMax: 1800, yMax: 3200, zMax: 300

- **de_dust2**:  
  Bounds: xMin: -2200, yMin: -1100, zMin: -120, xMax: 1800, yMax: 3100, zMax: 450

- **cs_office**:  
  Bounds: xMin: -1600, yMin: -2200, zMin: -400, xMax: 2300, yMax: 1300, zMax: 0

- **cs_italy**:  
  Bounds: xMin: -1500, yMin: -2100, zMin: -200, xMax: 1000, yMax: 2500, zMax: 300

### Image Specifications

- **Resolution**: 1024x1024 pixels
- **Format**: JPG

### Image Naming Convention

Images are named using the following format:

```
mapname x y z pitch yaw pitch_adjusted yaw_adjusted.jpg
```

Where:
- **mapname**: The name of the map (e.g., `cs_italy`)
- **x, y, z**: Coordinates within the map bounds
- **pitch**: Vertical angle (-90°: looking up, 90°: looking down)
- **yaw**: Horizontal angle (0° to 360°)
- **pitch_adjusted**: Adjusted pitch value for alternative representation
- **yaw_adjusted**: Adjusted yaw value for alternative representation

### Dataset Structure

The dataset is organized into three primary folders:
- **train**: 80% of the images
- **validation**: 10% of the images
- **test**: 10% of the images

Each primary folder contains subfolders for each map.

### Image Selection Process

A total of 166,667 images were initially captured per map. To ensure quality, only the top 60% largest images were selected based on file size, as larger images tend to contain more high-frequency details. This method effectively filtered out undesirable images, such as those dominated by a single color or extremely close-up textures lacking detail. This dataset does not include the filtered-out images.

### Known Discrepancies from In-Game Visuals

Due to the images being captured in the Source 2 Viewer rather than the actual game, the following discrepancies may be observed:

- Water rendering may appear incorrect.
- Lighting is inconsistent on some maps, particularly **de_anubis**, which appears overly bright.
- The secondary map version of **ar_pool_day** is visible in the sky, unlike in the actual game.
- Hanging cables or wires, as seen in maps like **de_dust2**, are absent.
- Certain materials appear shinier than they do in-game.
- Some color shades differ, for example, the red and blue sides on **ar_pool_day** appear gray.

### Map Bounds

The map bounds were chosen based on the playable areas—locations that can be reached without cheats (`sv_cheats 1`)—plus a small additional margin. This includes potential positions like boosting on top of one another and jumping at the highest point.

## Usage Notes

This dataset is suitable for various applications including training machine learning models, performing visual analysis, and more. Due to the known discrepancies mentioned above, users should be aware that the images may not perfectly reflect in-game conditions.

For more information on how the images were captured, visit the following resources:
- [Source 2 Viewer](https://valveresourceformat.github.io/)
- [ValveResourceFormat on GitHub](https://github.com/ValveResourceFormat/ValveResourceFormat)

## Credit

This dataset was created for videos on the Youtube Channel [Programming with Julius](https://www.youtube.com/@ProgrammingWithJulius).

If you used it, feel free to visit and let me know :)
