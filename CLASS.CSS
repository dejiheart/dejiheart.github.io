// Mobile Navigation Toggle
const hamburger = document.getElementById('hamburger');
const navMenu = document.getElementById('nav-menu');

hamburger.addEventListener('click', () => {
    hamburger.classList.toggle('active');
    navMenu.classList.toggle('active');
});

// Close mobile menu when clicking on a link
document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', () => {
        hamburger.classList.remove('active');
        navMenu.classList.remove('active');
    });
});

// Navbar background change on scroll
window.addEventListener('scroll', () => {
    const navbar = document.getElementById('navbar');
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});

// Smooth scrolling for navigation links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});

// Initialize AOS (Animate On Scroll)
AOS.init({
    duration: 1000,
    once: true,
    offset: 100
});

// Contact Form Handling
const contactForm = document.getElementById('contactForm');
if (contactForm) {
    contactForm.addEventListener('submit', function(e) {
        e.preventDefault();
        
        // Get form data
        const formData = new FormData(this);
        const data = Object.fromEntries(formData);
        
        // Here you would typically send the data to your server
        // For now, we'll just show a success message
        alert('Thank you for your message! We\'ll get back to you soon.');
        
        // Reset form
        this.reset();
    });
}

// Play button functionality (for hero video)
const playButton = document.querySelector('.play-button');
if (playButton) {
    playButton.addEventListener('click', function() {
        // Here you would typically open a video modal or start playing a video
        alert('Video player would open here!');
    });
}

// Playlist play buttons
const playOverlays = document.querySelectorAll('.play-overlay');
playOverlays.forEach(overlay => {
    overlay.addEventListener('click', function() {
        const playlistName = this.closest('.playlist-card').querySelector('h4').textContent;
        alert(`Playing: ${playlistName}`);
    });
});

// Service card hover effects
const serviceCards = document.querySelectorAll('.service-card');
serviceCards.forEach(card => {
    card.addEventListener('mouseenter', function() {
        this.style.transform = 'translateY(-10px) scale(1.02)';
    });
    
    card.addEventListener('mouseleave', function() {
        this.style.transform = 'translateY(0) scale(1)';
    });
});

// Travel card interactions
const travelCards = document.querySelectorAll('.travel-card');
travelCards.forEach(card => {
    card.addEventListener('click', function() {
        const destination = this.querySelector('h3').textContent;
        // Simulate navigation to travel guide
        console.log(`Navigating to ${destination} travel guide`);
    });
});

// Gallery lightbox functionality
const galleryItems = document.querySelectorAll('.gallery-item');
galleryItems.forEach(item => {
    item.addEventListener('click', function() {
        const img = this.querySelector('img');
        const imgSrc = img.src;
        const imgAlt = img.alt;
        
        // Create lightbox
        const lightbox = document.createElement('div');
        lightbox.style.cssText = `
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            cursor: pointer;
        `;
        
        const lightboxImg = document.createElement('img');
        lightboxImg.src = imgSrc;
        lightboxImg.alt = imgAlt;
        lightboxImg.style.cssText = `
            max-width: 90%;
            max-height: 90%;
            object-fit: contain;
            border-radius: 10px;
        `;
        
        lightbox.appendChild(lightboxImg);
        document.body.appendChild(lightbox);
        
        // Close lightbox on click
        lightbox.addEventListener('click', function() {
            document.body.removeChild(lightbox);
        });
    });
});

// Newsletter signup (if you add one)
const newsletterForm = document.querySelector('.newsletter-form');
if (newsletterForm) {
    newsletterForm.addEventListener('submit', function(e) {
        e.preventDefault();
        const email = this.querySelector('input[type="email"]').value;
        alert(`Thank you for subscribing with email: ${email}`);
        this.reset();
    });
}

// Affiliate link tracking (example)
const affiliateLinks = document.querySelectorAll('a[href*="affiliate"]');
affiliateLinks.forEach(link => {
    link.addEventListener('click', function(e) {
        // Track affiliate link clicks
        console.log('Affiliate link clicked:', this.href);
        
        // You could send this data to your analytics
        // gtag('event', 'click', {
        //     'event_category': 'Affiliate Link',
        //     'event_label': this.href,
        //     'transport_type': 'beacon'
        // });
    });
});

// Performance optimization - Lazy loading images
const images = document.querySelectorAll('img');
const imageOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px 50px 0px'
};

const imageObserver = new IntersectionObserver((entries, observer) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            const img = entry.target;
            img.style.opacity = '0';
            img.onload = () => {
                img.style.transition = 'opacity 0.5s ease';
                img.style.opacity = '1';
            };
            observer.unobserve(img);
        }
    });
}, imageOptions);

images.forEach(img => imageObserver.observe(img));

// Add loading animation
window.addEventListener('load', () => {
    document.body.classList.add('loaded');
});

// Error handling for images
images.forEach(img => {
    img.addEventListener('error', function() {
        this.src = 'data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 300"><rect width="400" height="300" fill="%23f0f0f0"/><text x="50%" y="50%" text-anchor="middle" dy=".3em" fill="%23999" font-family="Arial" font-size="16">Image not available</text></svg>';
    });
});

// Social media share functionality
const shareButtons = document.querySelectorAll('.share-button');
shareButtons.forEach(button => {
    button.addEventListener('click', function() {
        const platform = this.dataset.platform;
        const url = window.location.href;
        const title = document.title;
        
        let shareUrl = '';
        
        switch(platform) {
            case 'twitter':
                shareUrl = `https://twitter.com/intent/tweet?text=${encodeURIComponent(title)}&url=${encodeURIComponent(url)}`;
                break;
            case 'facebook':
                shareUrl = `https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(url)}`;
                break;
            case 'linkedin':
                shareUrl = `https://www.linkedin.com/sharing/share-offsite/?url=${encodeURIComponent(url)}`;
                break;
        }
        
        if (shareUrl) {
            window.open(shareUrl, '_blank', 'width=600,height=400');
        }
    });
});

// Analytics tracking (example)
function trackEvent(eventName, eventData) {
    // Send to your analytics platform
    console.log('Event tracked:', eventName, eventData);
    
    // Example with gtag (Google Analytics)
    if (typeof gtag !== 'undefined') {
        gtag('event', eventName, eventData);
    }
}

// Track page scroll depth
let maxScroll = 0;
window.addEventListener('scroll', () => {
    const scrollPercentage = (window.scrollY / (document.documentElement.scrollHeight - window.innerHeight)) * 100;
    if (scrollPercentage > maxScroll) {
        maxScroll = scrollPercentage;
        
        // Track scroll milestones
        if (maxScroll >= 25 && maxScroll < 26) {
            trackEvent('scroll_depth', { percent: 25 });
        } else if (maxScroll >= 50 && maxScroll < 51) {
            trackEvent('scroll_depth', { percent: 50 });
        } else if (maxScroll >= 75 && maxScroll < 76) {
            trackEvent('scroll_depth', { percent: 75 });
        } else if (maxScroll >= 90 && maxScroll < 91) {
            trackEvent('scroll_depth', { percent: 90 });
        }
    }
});

// Track time on page
let pageStartTime = Date.now();
window.addEventListener('beforeunload', () => {
    const timeOnPage = (Date.now() - pageStartTime) / 1000;
    trackEvent('time_on_page', { seconds: Math.round(timeOnPage) });
});