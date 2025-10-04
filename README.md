# 🎨 Frontend Mentor Challenges

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Site-blue?style=for-the-badge&logo=github)](https://ifalfahri.github.io/frontend-mentor-challenges)
[![Frontend Mentor](https://img.shields.io/badge/Frontend%20Mentor-Profile-orange?style=for-the-badge&logo=frontendmentor)](https://www.frontendmentor.io/profile/ifalfahri)
[![License](https://img.shields.io/github/license/ifalfahri/frontend-mentor-challenges?style=for-the-badge)](LICENSE)

Welcome to my collection of **Frontend Mentor** challenge solutions! This repository showcases my journey through various web development challenges, demonstrating skills in HTML, CSS, JavaScript, and responsive design.

## 🌐 Live Site

Visit the live site to explore all completed challenges:
**[https://ifalfahri.github.io/frontend-mentor-challenges](https://ifalfahri.github.io/frontend-mentor-challenges)**

The site automatically detects and lists all challenge folders using GitHub Actions and Jekyll!

## 📋 Challenge List

### Completed Challenges

- **QR Code Component** - [`01-qr-code-component/`](01-qr-code-component/)
  - A simple QR code card component
  - Skills: HTML, CSS, Flexbox, Responsive Design

*More challenges coming soon...*

## 🛠️ Technologies Used

### Core Technologies
- **HTML5** - Semantic markup
- **CSS3** - Modern styling, Flexbox, Grid
- **JavaScript** - Interactive functionality
- **Responsive Design** - Mobile-first approach

### Tools & Workflow
- **Jekyll** - Static site generation
- **GitHub Pages** - Hosting and deployment
- **GitHub Actions** - Automated challenge detection
- **Git** - Version control

## 🚀 Features

### Automated Challenge Detection
This repository uses GitHub Actions to automatically detect new challenge folders and update the website. Simply:

1. Create a new folder for your challenge
2. Add an `index.html` file to the folder
3. Push to the repository
4. The GitHub Action will automatically update the site within minutes!

### Responsive Design
All challenges are built with a mobile-first approach and tested across different devices and screen sizes.


## 🏁 Getting Started

### Prerequisites
- Basic knowledge of HTML, CSS, and JavaScript
- Git installed on your machine
- A code editor (VS Code recommended)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/ifalfahri/frontend-mentor-challenges.git
   cd frontend-mentor-challenges
   ```

2. **Install Jekyll (for local development)**
   ```bash
   # On Arch Linux
   sudo pacman -S ruby base-devel
   gem install jekyll bundler
   
   # On Ubuntu/Debian
   sudo apt install ruby-full build-essential zlib1g-dev
   gem install jekyll bundler
   ```

3. **Run the site locally**
   ```bash
   bundle install
   bundle exec jekyll serve --livereload
   ```

4. **View the site**
   Open [http://localhost:4000](http://localhost:4000) in your browser

### Adding a New Challenge

1. **Create a new folder** with a descriptive name (e.g., `02-profile-card-component`)

2. **Add your solution files**
   ```
   02-profile-card-component/
   ├── index.html          # Your HTML solution
   ├── style.css          # Your CSS (optional if inline)
   ├── script.js          # Your JavaScript (if needed)
   ├── README.md          # Challenge documentation
   ├── design/            # Reference images from Frontend Mentor
   └── images/            # Challenge assets
   ```

3. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Add [Challenge Name] solution"
   git push origin main
   ```

4. **Wait for automation** - GitHub Actions will automatically detect your new challenge and update the website!


## 🤖 Automation Features

This repository includes several automated features:

### GitHub Actions Workflow
- **Automatic Challenge Detection** - Scans for new `index.html` files
- **Data File Generation** - Updates `_data/_challenges.yml` automatically
- **Site Regeneration** - Triggers Jekyll rebuild on GitHub Pages

### Jekyll Integration
- **Dynamic Listing** - Challenges appear automatically on the homepage
- **Responsive Layout** - Beautiful card-based design
- **Fast Loading** - Optimized static site generation

## 📊 Progress Tracking

| Status | Count | Description |
|--------|-------|-------------|
| ✅ Completed | 1 | Fully implemented challenges |
| 🚧 In Progress | 0 | Currently working on |
| 📋 Planned | ∞ | Frontend Mentor has 100+ challenges! |

## 🔗 Links & Resources

### This Project
- **Live Site**: [https://ifalfahri.github.io/frontend-mentor-challenges](https://ifalfahri.github.io/frontend-mentor-challenges)
- **Repository**: [https://github.com/ifalfahri/frontend-mentor-challenges](https://github.com/ifalfahri/frontend-mentor-challenges)

### Frontend Mentor
- **Website**: [https://www.frontendmentor.io](https://www.frontendmentor.io)
- **My Profile**: [https://www.frontendmentor.io/profile/ifalfahri](https://www.frontendmentor.io/profile/ifalfahri)

### Connect With Me
- **GitHub**: [@ifalfahri](https://github.com/ifalfahri)
- **Frontend Mentor**: [@ifalfahri](https://www.frontendmentor.io/profile/ifalfahri)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Frontend Mentor** for providing excellent design challenges
- **GitHub** for free hosting via GitHub Pages
- **Jekyll** for the amazing static site generator
- The **web development community** for inspiration and learning resources

---

⭐ **Star this repository** if you find it helpful or interesting!

🔄 **Follow along** as I continue to solve more Frontend Mentor challenges and improve my skills!

📝 **Feedback welcome** - Feel free to open an issue or reach out with suggestions!