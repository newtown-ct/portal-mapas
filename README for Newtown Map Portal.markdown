# Newtown Map Portal

The Newtown Map Portal is a web application for residents and visitors of Newtown, Connecticut, to access Geographic Information System (GIS) resources, submit public works requests, and download town maps in PDF format. Built with HTML, Tailwind CSS, and JavaScript, it provides a user-friendly interface for exploring cadastral data, GIS datasets, and contacting town staff.

## Features

- **Public Works Service Request**: Submit and monitor service requests via an external portal.
- **GIS Town Maps**: Explore interactive cadastral and address point data through WestCOG’s MapGeo.
- **Town Map Gallery**: Download PDF maps (Open Space, Street Index, Zip Codes, Zoning).
- **GIS Data Downloads**: Links to external GIS resources (UConn, CT DEEP, etc.).
- **Staff Contact**: Contact details for the Technology and GIS Department and Assessor’s Office.
- **Responsive Design**: Optimized for desktop and mobile devices.

## Recent Updates

- **Fixed PDF Downloads (May 2025)**:
  - Corrected `href` attributes in the "Town Map Gallery" section to point to the correct PDF files (`maps/Newtown_Open_Space.pdf`, `maps/Newtown_Street_Index.pdf`, `maps/Newtown_Zip_Codes.pdf`, `maps/Newtown_Zoning.pdf`).
  - Resolved 404 errors causing `.htm` file downloads by ensuring accurate file paths.
  - Tested successfully with relative paths for GitHub Pages and local hosting.

## Project Structure

```
newtown-map-portal/
├── index.html              # Main HTML file for the portal
├── images/
│   └── town_logo.jpg       # Town of Newtown logo
└── maps/
    ├── Newtown_Open_Space.pdf    # Open Space map PDF
    ├── Newtown_Street_Index.pdf  # Street Index map PDF
    ├── Newtown_Zip_Codes.pdf     # Zip Codes map PDF
    └── Newtown_Zoning.pdf        # Zoning map PDF
```

- **index.html**: Contains the portal’s structure, styled with Tailwind CSS and interactive toggles via JavaScript.
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
2. Navigate the grid to:
   - Submit a **Public Works Service Request** via the external link.
   - Explore **GIS Town Maps** on WestCOG’s MapGeo.
   - Download PDFs from the **Town Map Gallery** (click to toggle, then click "Download").
   - Access external **GIS Data Downloads**.
   - View **Staff Contact** details (click to toggle).
3. Use the toggle functionality: clicking an open section closes it, and only one section is open at a time.

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit changes (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

Please ensure file paths (e.g., `maps/Newtown_Open_Space.pdf`) are consistent and test downloads before submitting.

## Contact

For questions or support, refer to the "Staff Contact" section in the portal:
- **Technology and GIS Dept.**: technology.gis@newtown-ct.gov, (203) 270-4270
- **Assessor’s Office**: sarah.carey@newtown-ct.gov, (203) 270-4240

## License

MIT License (update as needed).