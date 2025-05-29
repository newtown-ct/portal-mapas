# Newtown Map Portal

The Newtown Map Portal is a web application for residents and visitors of Newtown, Connecticut, to access Geographic Information System (GIS) resources, submit public works requests, download town maps in PDF format, and explore external GIS data. Built with HTML, Tailwind CSS, and JavaScript, it offers a responsive, user-friendly interface for accessing cadastral data, interactive maps, and town contact information.

## Features

- **Public Works Service Request**: Submit and monitor service requests via an external portal.
- **New GIS Town Maps**: Explore interactive cadastral and address point data through WestCOG’s MapGeo, with an access counter.
- **Town Map Gallery**: Download PDF maps (Open Space, Street Index, Zip Codes, Zoning) with a disclaimer on accuracy.
- **Download Others GIS Sources**: Access external GIS data resources (UConn, CT DEEP, etc.), with an access counter.
- **Staff Contact**: Contact details for the Technology and GIS Department and Assessor’s Office.
- **Legacy GIS Website**: Access the old GIS interface (available until August 31, 2025), with an access counter.
- **Responsive Design**: Optimized for desktop and mobile devices with a 2x3 grid layout on larger screens.
- **Access Counters**: Track clicks on "New GIS Town Maps," "Download Others GIS Sources," and "Legacy GIS Website," displayed inside their respective boxes.

## Recent Updates

- **May 2025**:
  - Fixed PDF download links in "Town Map Gallery" to use relative paths (`maps/Newtown_Open_Space.pdf`, etc.), resolving 404 errors.
  - Added "Legacy GIS Website" box linking to `https://newtown.mapxpress.net/`, available until August 31, 2025.
  - Renamed "GIS Data Downloads" to "Download Others GIS Sources" with updated toggle section.
  - Added access counters for "New GIS Town Maps," "Download Others GIS Sources," and "Legacy GIS Website," displayed inside boxes below descriptions, persisting via `localStorage`.
  - Adjusted grid layout: "Staff Contact" bottom-left, "Legacy GIS Website" bottom-right on larger screens.
  - Updated "Town Map Gallery" with revised dates (February-May 2011) and a disclaimer on map accuracy.

## Project Structure

```
newtown-map-portal/
├── index.html              # Main HTML file for the portal
├── images/
│   └── town_logo.jpg       # Town of Newtown logo
└── maps/
    ├── Newtown_Open_Space.pdf    # Open Space map PDF (1.2 MB)
    ├── Newtown_Street_Index.pdf  # Street Index map PDF (1.5 MB)
    ├── Newtown_Zip_Codes.pdf     # Zip Codes map PDF (1.0 MB)
    └── Newtown_Zoning.pdf        # Zoning map PDF (1.3 MB)
```

- **index.html**: Portal structure, styled with Tailwind CSS, with toggle sections and access counters via JavaScript.
- **images/town_logo.jpg**: Logo displayed at the top of the portal.
- **maps/**: Directory containing downloadable PDF maps.

## Setup Instructions

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, etc.).
- (Optional) Python 3.x for local testing.
- A GitHub account for hosting on GitHub Pages.

### Local Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/username/repository.git
   cd repository
   ```
2. Ensure the `maps` folder contains all PDFs and `images` contains `town_logo.jpg`.
3. Start a local server:
   ```bash
   python -m http.server 8000
   ```
4. Open `http://localhost:8000` in your browser.

### GitHub Pages Deployment
1. Push the repository to GitHub:
   ```bash
   git push origin main
   ```
2. Enable GitHub Pages in repository settings:
   - Go to Settings > Pages.
   - Set Source to `main` branch, `/root` directory.
3. Access the portal at `https://username.github.io/repository`.

## Usage

1. Open the portal in a browser.
2. Navigate the 2x3 grid (single column on small screens):
   - **Public Works Service Request**: Submit requests via the external link.
   - **New GIS Town Maps**: Explore interactive GIS maps; counter increments on click.
   - **Town Map Gallery**: Toggle to download PDF maps (Open Space, Street Index, Zip Codes, Zoning).
   - **Download Others GIS Sources**: Toggle to access external GIS data; counter increments on toggle.
   - **Staff Contact**: Toggle to view contact details for Technology and GIS Dept. and Assessor’s Office.
   - **Legacy GIS Website**: Access the old interface; counter increments on click.
3. **Toggle Functionality**: Click a section to open it, click again to close, or open another section to switch (only one section open at a time).
4. **Access Counters**: Visible inside "New GIS Town Maps," "Download Others GIS Sources," and "Legacy GIS Website" boxes after clicking, showing access counts.
5. **PDF Downloads**: Available in "Town Map Gallery" with file sizes and revision dates.

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit changes (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

Please ensure file paths (e.g., `maps/Newtown_Open_Space.pdf`), counter logic, and toggle functionality remain consistent. Test all downloads and links before submitting.

## Contact

For questions or support, refer to the "Staff Contact" section in the portal:
- **Technology and GIS Dept.**: technology.gis@newtown-ct.gov, (203) 270-4270
- **Assessor’s Office**: sarah.carey@newtown-ct.gov, (203) 270-4240

## License

MIT License (update as needed).
