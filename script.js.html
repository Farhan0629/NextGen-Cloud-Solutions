<meta name='viewport' content='width=device-width, initial-scale=1'/>// Mobile Navigation Toggle
document.addEventListener('DOMContentLoaded', function() {
    const hamburger = document.getElementById('hamburger');
    const navMenu = document.getElementById('nav-menu');
    
    if (hamburger && navMenu) {
        hamburger.addEventListener('click', function() {
            navMenu.classList.toggle('active');
            hamburger.classList.toggle('active');
        });
        
        // Close menu when clicking on a link
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
                hamburger.classList.remove('active');
            });
        });
        
        // Close menu when clicking outside
        document.addEventListener('click', function(event) {
            if (!hamburger.contains(event.target) && !navMenu.contains(event.target)) {
                navMenu.classList.remove('active');
                hamburger.classList.remove('active');
            }
        });
    }

    // Smooth scrolling for anchor links
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

    // Contact Form Enhancement
    const contactForm = document.getElementById('contactForm');
    if (contactForm) {
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form data
            const formData = new FormData(contactForm);
            const name = formData.get('name');
            const email = formData.get('email');
            const company = formData.get('company') || 'Not specified';
            const phone = formData.get('phone') || 'Not provided';
            const service = formData.get('service') || 'General inquiry';
            const message = formData.get('message');
            
            // Validate required fields
            if (!name || !email || !message) {
                showNotification('Please fill in all required fields.', 'error');
                return;
            }
            
            // Validate email format
            if (!isValidEmail(email)) {
                showNotification('Please enter a valid email address.', 'error');
                return;
            }
            
            // Create email content
            const emailSubject = `New Consultation Request from ${name}`;
            const emailBody = `
New consultation request from NextGen Cloud Solutions website:

Name: ${name}
Email: ${email}
Company: ${company}
Phone: ${phone}
Service Interest: ${service}

Message:
${message}

---
This message was sent from the NextGen Cloud Solutions contact form.
            `.trim();
            
            // Create mailto link
            const mailtoLink = `mailto:contact@nextgencloud.solutions?subject=${encodeURIComponent(emailSubject)}&body=${encodeURIComponent(emailBody)}`;
            
            // Open email client
            window.location.href = mailtoLink;
            
            // Show success message
            showNotification('Thank you! Your email client should open now. If not, please email us directly at contact@nextgencloud.solutions', 'success');
            
            // Reset form
            contactForm.reset();
            
            // Track form submission
            trackEvent('form_submit', {
                form_name: 'contact_form',
                service_interest: service,
                page_location: window.location.href
            });
        });
    }

    // Form validation
    const requiredFields = document.querySelectorAll('input[required], textarea[required]');
    requiredFields.forEach(field => {
        field.addEventListener('blur', validateField);
        field.addEventListener('input', clearValidation);
    });

    function validateField(e) {
        const field = e.target;
        const value = field.value.trim();
        
        if (!value) {
            showFieldError(field, 'This field is required');
        } else if (field.type === 'email' && !isValidEmail(value)) {
            showFieldError(field, 'Please enter a valid email address');
        } else {
            clearFieldError(field);
        }
    }

    function clearValidation(e) {
        clearFieldError(e.target);
    }

    function showFieldError(field, message) {
        clearFieldError(field);
        field.style.borderColor = '#ef4444';
        
        const errorDiv = document.createElement('div');
        errorDiv.className = 'field-error';
        errorDiv.style.color = '#ef4444';
        errorDiv.style.fontSize = '0.875rem';
        errorDiv.style.marginTop = '0.25rem';
        errorDiv.textContent = message;
        
        field.parentNode.appendChild(errorDiv);
    }

    function clearFieldError(field) {
        field.style.borderColor = '';
        const existingError = field.parentNode.querySelector('.field-error');
        if (existingError) {
            existingError.remove();
        }
    }

    function isValidEmail(email) {
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        return emailRegex.test(email);
    }

    // Notification system
    function showNotification(message, type = 'info') {
        const notification = document.createElement('div');
        notification.className = `notification notification-${type}`;
        notification.style.cssText = `
            position: fixed;
            top: 20px;
            right: 20px;
            background: ${type === 'success' ? '#10b981' : type === 'error' ? '#ef4444' : '#3b82f6'};
            color: white;
            padding: 1rem 1.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 10000;
            max-width: 400px;
            animation: slideInRight 0.3s ease-out;
            font-weight: 500;
        `;
        notification.textContent = message;
        
        document.body.appendChild(notification);
        
        setTimeout(() => {
            notification.style.animation = 'slideOutRight 0.3s ease-in';
            setTimeout(() => {
                if (notification.parentNode) {
                    notification.parentNode.removeChild(notification);
                }
            }, 300);
        }, 5000);
    }

    // Add CSS animations for notifications
    if (!document.querySelector('#notification-styles')) {
        const style = document.createElement('style');
        style.id = 'notification-styles';
        style.textContent = `
            @keyframes slideInRight {
                from { transform: translateX(100%); opacity: 0; }
                to { transform: translateX(0); opacity: 1; }
            }
            @keyframes slideOutRight {
                from { transform: translateX(0); opacity: 1; }
                to { transform: translateX(100%); opacity: 0; }
            }
        `;
        document.head.appendChild(style);
    }

    // Intersection Observer for scroll animations
    if ('IntersectionObserver' in window) {
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                    observer.unobserve(entry.target); // Stop observing once animated
                }
            });
        }, observerOptions);

        // Observe elements that should animate in
        document.querySelectorAll('.service-card, .value-card, .benefit-item, .faq-item, .contact-card, .expectations-card').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease-out, transform 0.6s ease-out';
            observer.observe(el);
        });
    }

    // Service dropdown enhancement
    const serviceSelect = document.getElementById('service');
    if (serviceSelect) {
        serviceSelect.addEventListener('change', function() {
            if (this.value) {
                this.style.borderColor = '#10b981';
                trackEvent('service_selection', {
                    service_selected: this.value,
                    page_location: window.location.href
                });
            }
        });
    }

    // Analytics event tracking
    function trackEvent(eventName, eventData = {}) {
        if (typeof gtag !== 'undefined') {
            gtag('event', eventName, {
                ...eventData,
                event_category: 'website_interaction',
                timestamp: new Date().toISOString()
            });
        }
        
        // Console log for debugging (remove in production)
        console.log('Event tracked:', eventName, eventData);
    }

    // Track CTA button clicks
    document.querySelectorAll('.cta-button').forEach(button => {
        button.addEventListener('click', (e) => {
            trackEvent('cta_click', {
                button_text: button.textContent.trim(),
                button_location: getElementLocation(button),
                page_location: window.location.href
            });
        });
    });

    // Track service link clicks
    document.querySelectorAll('.service-link').forEach(link => {
        link.addEventListener('click', (e) => {
            const serviceCard = link.closest('.service-card');
            const serviceName = serviceCard ? serviceCard.querySelector('h3').textContent : 'Unknown';
            
            trackEvent('service_interest', {
                service_name: serviceName,
                link_destination: link.href,
                page_location: window.location.href
            });
        });
    });

    // Track social media link clicks
    document.querySelectorAll('.social-links a').forEach(link => {
        link.addEventListener('click', (e) => {
            const platform = getSocialPlatform(link.href);
            trackEvent('social_media_click', {
                platform: platform,
                link_url: link.href,
                page_location: window.location.href
            });
        });
    });

    // Helper function to get social media platform name
    function getSocialPlatform(url) {
        if (url.includes('linkedin')) return 'LinkedIn';
        if (url.includes('twitter')) return 'Twitter';
        if (url.includes('github')) return 'GitHub';
        return 'Unknown';
    }

    // Helper function to get element location on page
    function getElementLocation(element) {
        const rect = element.getBoundingClientRect();
        return {
            section: getElementSection(element),
            position_x: Math.round(rect.left),
            position_y: Math.round(rect.top + window.scrollY)
        };
    }

    // Helper function to determine which section an element is in
    function getElementSection(element) {
        const sections = ['hero', 'services-overview', 'why-choose-us', 'cta-section', 'footer'];
        for (let section of sections) {
            if (element.closest(`.${section}`)) {
                return section;
            }
        }
        return 'unknown';
    }

    // Performance optimization: Lazy load background images
    const lazyBackgrounds = document.querySelectorAll('[data-bg]');
    if ('IntersectionObserver' in window && lazyBackgrounds.length) {
        const bgObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const element = entry.target;
                    element.style.backgroundImage = `url(${element.dataset.bg})`;
                    element.removeAttribute('data-bg');
                    bgObserver.unobserve(element);
                }
            });
        });

        lazyBackgrounds.forEach(bg => bgObserver.observe(bg));
    }

    // Handle navbar background on scroll
    const navbar = document.querySelector('.navbar');
    if (navbar) {
        let scrollTimeout;
        
        window.addEventListener('scroll', () => {
            // Throttle scroll events
            if (scrollTimeout) {
                clearTimeout(scrollTimeout);
            }
            
            scrollTimeout = setTimeout(() => {
                if (window.scrollY > 50) {
                    navbar.style.background = 'rgba(255, 255, 255, 0.98)';
                    navbar.style.boxShadow = '0 4px 6px -1px rgba(0, 0, 0, 0.15)';
                } else {
                    navbar.style.background = 'rgba(255, 255, 255, 0.95)';
                    navbar.style.boxShadow = '0 4px 6px -1px rgba(0, 0, 0, 0.1)';
                }
            }, 10);
        });
    }

    // Scroll progress indicator
    function createScrollIndicator() {
        const indicator = document.createElement('div');
        indicator.className = 'scroll-indicator';
        indicator.innerHTML = '<div class="scroll-progress"></div>';
        document.body.appendChild(indicator);
        
        const progress = indicator.querySelector('.scroll-progress');
        
        window.addEventListener('scroll', () => {
            const scrolled = (window.scrollY / (document.documentElement.scrollHeight - window.innerHeight)) * 100;
            progress.style.width = Math.min(scrolled, 100) + '%';
        });
    }

    // Initialize scroll indicator
    createScrollIndicator();

    // FAQ accordion functionality (if needed in future)
    function initFAQAccordion() {
        const faqItems = document.querySelectorAll('.faq-item');
        faqItems.forEach(item => {
            const question = item.querySelector('h4');
            if (question) {
                question.style.cursor = 'pointer';
                question.addEventListener('click', () => {
                    const answer = item.querySelector('p');
                    if (answer) {
                        const isVisible = answer.style.display !== 'none';
                        answer.style.display = isVisible ? 'none' : 'block';
                        question.style.color = isVisible ? '#1f2937' : '#10b981';
                    }
                });
            }
        });
    }

    // Form autosave (saves form data to localStorage)
    function initFormAutosave() {
        const form = document.getElementById('contactForm');
        if (!form) return;

        const formFields = form.querySelectorAll('input, textarea, select');
        const storageKey = 'nextgen-contact-form';

        // Load saved data
        try {
            const savedData = JSON.parse(localStorage.getItem(storageKey) || '{}');
            formFields.forEach(field => {
                if (savedData[field.name] && field.type !== 'submit') {
                    field.value = savedData[field.name];
                }
            });
        } catch (e) {
            console.warn('Failed to load saved form data:', e);
        }

        // Save data on input
        formFields.forEach(field => {
            field.addEventListener('input', () => {
                try {
                    const formData = new FormData(form);
                    const dataObject = {};
                    for (let [key, value] of formData.entries()) {
                        dataObject[key] = value;
                    }
                    localStorage.setItem(storageKey, JSON.stringify(dataObject));
                } catch (e) {
                    console.warn('Failed to save form data:', e);
                }
            });
        });

        // Clear saved data on successful submission
        form.addEventListener('submit', () => {
            setTimeout(() => {
                localStorage.removeItem(storageKey);
            }, 1000);
        });
    }

    // Initialize autosave
    initFormAutosave();

    // Keyboard navigation enhancement
    function enhanceKeyboardNavigation() {
        // Add keyboard support for hamburger menu
        const hamburger = document.getElementById('hamburger');
        if (hamburger) {
            hamburger.setAttribute('tabindex', '0');
            hamburger.setAttribute('role', 'button');
            hamburger.setAttribute('aria-label', 'Toggle navigation menu');
            
            hamburger.addEventListener('keydown', (e) => {
                if (e.key === 'Enter' || e.key === ' ') {
                    e.preventDefault();
                    hamburger.click();
                }
            });
        }

        // Add skip link for accessibility
        const skipLink = document.createElement('a');
        skipLink.href = '#main-content';
        skipLink.className = 'skip-link';
        skipLink.textContent = 'Skip to main content';
        document.body.insertBefore(skipLink, document.body.firstChild);

        // Add main content landmark
        const mainContent = document.querySelector('.hero, .page-header');
        if (mainContent) {
            mainContent.id = 'main-content';
        }
    }

    // Initialize keyboard navigation
    enhanceKeyboardNavigation();

    // Console welcome message
    console.log(`
    %c🚀 NextGen Cloud Solutions
    %cWebsite built with modern web technologies
    Need cloud solutions? Contact us at contact@nextgencloud.solutions
    `, 
    'color: #1e3a8a; font-size: 18px; font-weight: bold;',
    'color: #10b981; font-size: 14px;'
    );

    // Development mode helper
    if (window.location.hostname === 'localhost' || window.location.hostname === '127.0.0.1') {
        console.log('%c🔧 Development Mode Active', 'color: #f59e0b; font-weight: bold;');
        
        // Add development helpers
        window.NextGenUtils = {
            trackEvent,
            showNotification,
            validateEmail: isValidEmail,
            clearFormData: () => localStorage.removeItem('nextgen-contact-form')
        };
    }

    // Page load performance tracking
    window.addEventListener('load', () => {
        const perfData = performance.timing;
        const loadTime = perfData.loadEventEnd - perfData.navigationStart;
        
        trackEvent('page_performance', {
            load_time: loadTime,
            page_url: window.location.href,
            user_agent: navigator.userAgent.substring(0, 100) // Truncate for privacy
        });
        
        console.log(`%cPage loaded in ${loadTime}ms`, 'color: #10b981;');
    });

    // Error tracking
    window.addEventListener('error', (e) => {
        trackEvent('javascript_error', {
            error_message: e.message,
            error_source: e.filename,
            error_line: e.lineno,
            page_url: window.location.href
        });
        
        console.warn('NextGen Cloud Solutions - Error:', e.message);
    });

    // Unhandled promise rejection tracking
    window.addEventListener('unhandledrejection', (e) => {
        trackEvent('promise_rejection', {
            error_message: e.reason?.message || 'Unknown promise rejection',
            page_url: window.location.href
        });
        
        console.warn('NextGen Cloud Solutions - Unhandled Promise Rejection:', e.reason);
    });

    // Online/offline status tracking
    function handleConnectionChange() {
        const isOnline = navigator.onLine;
        
        if (!isOnline) {
            showNotification('You appear to be offline. Some features may not work properly.', 'error');
        }
        
        trackEvent('connection_status', {
            is_online: isOnline,
            page_url: window.location.href
        });
    }

    window.addEventListener('online', handleConnectionChange);
    window.addEventListener('offline', handleConnectionChange);

    // Prevent form submission if offline
    if (contactForm) {
        contactForm.addEventListener('submit', (e) => {
            if (!navigator.onLine) {
                e.preventDefault();
                showNotification('You are currently offline. Please check your connection and try again.', 'error');
                return false;
            }
        });
    }
});

// Service worker registration for PWA capabilities (optional)
if ('serviceWorker' in navigator) {
    window.addEventListener('load', () => {
        // Uncomment when you create a service worker file
        // navigator.serviceWorker.register('/sw.js')
        //     .then(registration => {
        //         console.log('SW registered:', registration);
        //         trackEvent('service_worker_registered', {
        //             scope: registration.scope
        //         });
        //     })
        //     .catch(error => {
        //         console.log('SW registration failed:', error);
        //         trackEvent('service_worker_failed', {
        //             error: error.message
        //         });
        //     });
    });
}

// Utility functions that can be used globally
window.NextGenCloudSolutions = {
    // Public API for external use
    version: '1.0.0',
    
    // Contact form submission (can be called externally)
    submitContactForm: function(formData) {
        const event = new CustomEvent('submit');
        const form = document.getElementById('contactForm');
        if (form) {
            // Populate form with provided data
            Object.keys(formData).forEach(key => {
                const field = form.querySelector(`[name="${key}"]`);
                if (field) {
                    field.value = formData[key];
                }
            });
            
            // Trigger submit
            form.dispatchEvent(event);
        }
    },
    
    // Show notification (can be called externally)
    notify: function(message, type = 'info') {
        if (typeof showNotification === 'function') {
            showNotification(message, type);
        }
    },
    
    // Get form data
    getFormData: function() {
        const form = document.getElementById('contactForm');
        if (form) {
            return new FormData(form);
        }
        return null;
    }
};

// Export for module environments
if (typeof module !== 'undefined' && module.exports) {
    module.exports = window.NextGenCloudSolutions;
}
