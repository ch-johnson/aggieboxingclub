# Aggie Boxing Club Website

Welcome to the repository for the Aggie Boxing Club (ABC) website at Texas A&M University. This project is designed to be a "High Energy, High Performance" representation of the club, aligning with its core values: Honor in the Fight, Tenacity in the Face of Hardship, and Virtue as an Ultimatum.

## Architecture and Design

The website currently uses a dual-approach to layout and functionality:
1. **The Main Entrypoint (`index.html`)**: The core landing page has been redesigned as a single-page scrolling experience emphasizing a dark mode aesthetic, aggressive contrast, and bold, performance-focused typography (Oswald and Montserrat). It uses plain HTML/CSS with Bootstrap 5 and Javascript `IntersectionObserver` for smooth fade-in animations.
2. **Subpages (`about.html`, `class.html`, `contact.html`, `ffn.html`, `sponsors.html`, `usiba.html`)**: The subpages maintain a legacy structure utilizing Tailwind CSS. These pages dynamically inject navigation and footer components via `iframe` script injections (e.g., `<iframe src="header.html" onload="...">`).

### Brand Guidelines
- **Primary Color:** Aggie Maroon (`#500000`)
- **Secondary Color:** White (`#FFFFFF`) and Dark Shades (e.g., `#0a0a0a`)
- **Typography:**
  - **Display/Headings:** 'Oswald', sans-serif (Bold, commanding)
  - **Body text:** 'Montserrat', sans-serif (Clean, readable)
- **Tone:** High performance, unyielding discipline, and institutional credibility.

## File Structure & Functionality

### Core Pages
- **`index.html`**: The main landing page. It features:
  - **Navigation**: A fixed-top Bootstrap navbar with anchor links mapping to sections.
  - **Hero Section (`#home`)**: High-impact introduction with a call to action.
  - **Manifesto Section (`#manifesto`)**: A sequential fade-in display of the club's core values.
  - **Get Involved (`#get-involved`)**: A modular grid detailing paths for prospective members, attendees, volunteers, and sponsors to interact with the club.
  - **Programs Section (`#programs`)**: Distinct blocks highlighting University Boxing, Farmer’s Fight Night, and the USIBA National Champions team.

### Components
- **`header.html`**: A reusable Tailwind CSS navigation bar containing links to all subpages. Injected into subpages.
- **`footer.html`**: A reusable Tailwind CSS footer containing contact information and social media links. Injected into subpages.

### Subpages
*Note: These files currently serve as skeleton pages styled with Tailwind CSS that load the `header.html` and `footer.html` components.*
- **`about.html`**: Intended for detailed information about the club's history and mission.
- **`class.html`**: Intended for information regarding Boxing Fundamentals classes.
- **`contact.html`**: Intended for communication details.
- **`ffn.html`**: Intended for details about the premier charity exhibition, Farmer's Fight Night.
- **`sponsors.html`**: Intended for sponsor information and outreach.
- **`usiba.html`**: Intended for information regarding the collegiate competitive team.

## Getting Started / Local Development

Since the subpages rely on `iframe` onload events to inject components, you must run this site through a local web server to avoid CORS (Cross-Origin Resource Sharing) restrictions that occur when opening `file://` URLs directly in a browser.

1. **Start a local server**:
   - Using Python: `python3 -m http.server 8000`
   - Using Node (http-server): `npx http-server`
2. **Access the site**: Navigate to `http://localhost:8000` in your web browser.

## Contributing
When making changes, please ensure that new additions respect the "High Energy, High Performance" brand identity. For `index.html`, ensure any new CSS follows the existing custom styling block and that animations continue to utilize the `IntersectionObserver` logic provided at the bottom of the document.