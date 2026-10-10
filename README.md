# OnsiteBIM Revit Toolkit

The **OnsiteBIM Revit Toolkit** provides everything you need to connect your 3D Autodesk Revit models to physical construction sites at true 1:1 life-size scale using the **OnsiteBIM** mobile app.

---

## What’s in This Toolkit?

1. **`OnsiteBIM_Alignment_Target.rfa`**
   * A face-based Revit component family.
   * Snaps directly to any column face, wall, or concrete slab benchmark in your Revit model.
   * Tells OnsiteBIM exactly where the physical paper target is located in the real world.
   * Compatible with **Autodesk Revit 2024, 2025, 2026, and newer**.

2. **`IFC Configuration - OnsiteBIM.json`**
   * A pre-tuned, 1-click Revit export setup file.
   * Automatically sets correct real-world meter scaling, coordinates, element visibility, and property sets.
   * Eliminates common export mistakes so your model appears perfectly oriented and scaled on your first try.

---

## Step-by-Step Guide

### Step 1: Load the Alignment Target into Revit
1. Open your project in Autodesk Revit.
2. Drag and drop **`OnsiteBIM_Alignment_Target.rfa`** into your Revit window (or go to **Insert $\rightarrow$ Load Family** and select the file).

---

### Step 2: Place the Target on a Physical Benchmark
1. In Revit, open a 3D view or elevation/floor plan view.
2. Select the **OnsiteBIM Alignment Target** family from your Component tool (**Architecture $\rightarrow$ Component**).
3. Click to place the target onto a real-world spot on your building that exists (or will exist) on site (e.g. a column face on **Grid Line A-1** or a concrete wall).
4. In the Properties palette, set:
   * **Target ID**: Default is `12`. (Must match the number printed on your paper target).
   * **Target Size**: Default is `150 mm`. (Must match the physical printed black square size).

> [!IMPORTANT]
> **The Golden Rule: The Revit Square Represents the Printed Black Border**
> * The square geometry in the Revit family represents the **exact outer edges of the black square** on the printed paper target.
> * **Vertical Distance**: If you place the bottom edge of the Revit target square exactly **5'-0" (1.50 m)** above the finished slab, you must measure and tape the bottom edge of the physical paper target's black square exactly **5'-0" (1.50 m)** above the real concrete slab on site.
> * **Horizontal Distance**: If you place the side edge of the Revit target square **2'-0" (0.60 m)** away from a column corner or wall edge, you must tape the physical paper target's black square edge **2'-0" (0.60 m)** away from that same corner on site.
> * **Must Be Plumb & Level**: The paper target on site **must be hung completely level**. If the paper target is tilted by even $1^\circ$ or $2^\circ$, the entire virtual building model in your phone will tilt by that same angle! Use a small torpedo level or laser line when taping it up.

---

### Step 3: Prepare Your 3D View (Optional but Recommended)
1. Open your default **{3D}** view.
2. If your building model is very large (e.g., a 40-story tower), turn on the **Section Box** in your 3D view properties and crop the view to the specific floor or area you plan to inspect today.
3. *Note*: The OnsiteBIM export configuration exports whatever elements are currently visible in your active 3D view.

---

### Step 4: 1-Click Export to IFC
1. In Revit, go to **File $\rightarrow$ Export $\rightarrow$ IFC**.
2. In the Export IFC dialog, click the **Modify Setup...** button (top right).
3. In the setup window, look at the bottom left icon bar and click **Import from File...** (the folder icon with an arrow).
4. Select **`IFC Configuration - OnsiteBIM.json`** from this toolkit folder and click **Open**.
5. You will see **"IFC Configuration - OnsiteBIM"** appear in your setup list. Select it and click **OK**.
6. Choose where to save your `.ifc` file on your computer and click **Export**.

---

### Step 5: Print Your Matching Paper Alignment Target
1. Open any web browser on your phone, tablet, or computer and go to:  
   👉 **[https://onsitebim.app/generator.html](https://onsitebim.app/generator.html)**  
2. Select the matching **Target ID** (e.g. `12`) and **Size** (e.g. `150mm`).
3. Download the calibrated PDF and print it on standard office paper.
4. **Printer Setting**: Ensure your printer is set to **"Actual Size"** or **"100% Scale"** (never use "Fit to Page", which shrinks the target).
5. **Physical Scale Verification**: Every printed target includes built-in metric (cm) and imperial (inch) calibration ruler bars along the border. Lay your physical tape measure across the printed bar to confirm your printer printed at 100% true scale before going out to the site.

---

### Step 6: Tape on Site & Inspect in AR
1. **Measure & Tape**: On the jobsite, use a tape measure and level to tape the paper target at the exact vertical elevation and horizontal position matching your Revit model.
2. Transfer your exported `.ifc` file to your mobile device (via **Apple Files, Google Drive, Microsoft OneDrive, Dropbox, or AirDrop**).
3. Open **OnsiteBIM** on your iPhone, iPad, or Android device.
4. Tap **ADD** $\rightarrow$ select your `.ifc` file.
5. Point your camera at the paper Alignment Target taped to the column.
6. **Your 3D building model instantly locks into position at true 1:1 life-size scale!**
7. Walk around the jobsite:
   * Use the **Opacity Slider** to see through physical drywall and concrete to inspect hidden pipes, ducts, and conduits.
   * Use the **Measure Tool** to check real-world clearances against designed dimensions.
   * Use the **Layers Tool** to isolate specific disciplines like **MEP ONLY**.

---

## Frequently Asked Questions

#### Q: Do I need internet access on the construction site?
**A:** No. OnsiteBIM processes 100% of the 3D model locally on your phone or tablet. Once you have copied the `.ifc` file to your device, it works completely offline with zero cell or Wi-Fi signal—ideal for basements, tunnels, and remote sites.

#### Q: What if my Revit version is older than Revit 2024?
**A:** Because Autodesk Revit does not support backward file compatibility, the `.rfa` family requires Revit 2024 or newer. If you are on Revit 2021–2023, you can easily create a simple face-based generic model with an extruded 150mm square and use the same export settings.

#### Q: Can I place multiple Alignment Targets in one building?
**A:** Yes! You can place different targets on different floors or building wings (e.g. Target #12 on Ground Floor Column A-1, Target #13 on Level 2 Column B-4). When you walk up to each target on site, point your camera to instantly re-align.

---

## Support & Resources
* **Official Website**: [https://onsitebim.app](https://onsitebim.app)
* **Alignment Target Generator**: [https://onsitebim.app/generator.html](https://onsitebim.app/generator.html)
* **GitHub Repository**: [https://github.com/onsitebim](https://github.com/onsitebim)
* **Contact & Feedback**: [contact@onsitebim.app](mailto:support@onsitebim.app)
