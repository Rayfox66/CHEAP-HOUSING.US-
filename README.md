# CHEAP-HOUSING.US
HOME RENTAL WEBSITE
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cheap House US - Find Your Dream Home</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body { font-family: Arial, sans-serif; background-color: #f8f9fa; }
        .hero { background: linear-gradient(to right, #007bff, #28a745); color: white; padding: 50px 0; text-align: center; position: relative; overflow: hidden; }
        .carousel { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; }
        .carousel img { width: 100%; height: 100%; object-fit: cover; opacity: 0.3; }
        .hero-content { position: relative; z-index: 2; }
        .listing { margin-bottom: 20px; border: 1px solid #ddd; border-radius: 8px; overflow: hidden; transition: transform 0.2s; }
        .listing:hover { transform: scale(1.02); }
        .listing img { width: 100%; height: 200px; object-fit: cover; }
        footer { background-color: #343a40; color: white; padding: 20px 0; text-align: center; }
        .hidden { display: none; }
    </style>
</head>
<body>
    <!-- Header -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container">
            <a class="navbar-brand" href="#">Cheap House US</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#listings">Listings</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section with Carousel -->
    <section class="hero">
        <div class="carousel" id="heroCarousel">
            <img src="https://images.unsplash.com/photo-1564013799919-ab600027ffc6?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="House Carousel 1" class="active">
            <img src="https://images.unsplash.com/photo-1570129477492-45c003edd2be?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="House Carousel 2">
            <img src="https://images.unsplash.com/photo-1518780664697-55e3ad937233?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="House Carousel 3">
        </div>
        <div class="hero-content">
            <h1>Welcome to Cheap House US</h1>
            <p>Find affordable homes for sale and rent across the US.</p>
            <form class="d-flex justify-content-center mt-3" id="searchForm">
                <input class="form-control me-2" type="search" placeholder="Search by city, ZIP, or address" style="max-width: 400px;" id="searchInput">
                <button class="btn btn-light" type="submit">Search</button>
            </form>
        </div>
    </section>

    <!-- Listings Section -->
    <section id="listings" class="container my-5">
        <h2 class="text-center mb-4">Featured Listings</h2>
        <div class="row" id="listingsContainer">
            <div class="col-md-4 listing-item" data-search="cozy 3-bedroom home anytown main st">
                <div class="listing">
                    <img src="https://images.unsplash.com/photo-1564013799919-ab600027ffc6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="House 1">
                    <div class="p-3">
                        <h5>Cozy 3-Bedroom Home</h5>
                        <p>$250,000 | 2 Baths | 1,500 Sq Ft</p>
                        <p>123 Main St, Anytown, USA</p>
                        <button class="btn btn-primary view-details" data-bs-toggle="modal" data-bs-target="#detailsModal" data-title="Cozy 3-Bedroom Home" data-desc="A charming home with modern amenities." data-price="$250,000" data-img="https://images.unsplash.com/photo-1564013799919-ab600027ffc6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80">View Details</button>
                    </div>
                </div>
            </div>
            <div class="col-md-4 listing-item" data-search="modern apartment somewhere elm st">
                <div class="listing">
                    <img src="https://images.unsplash.com/photo-1570129477492-45c003edd2be?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="House 2">
                    <div class="p-3">
                        <h5>Modern Apartment</h5>
                        <p>$1,200/mo | 1 Bath | 800 Sq Ft</p>
                        <p>456 Elm St, Somewhere, USA</p>
                        <button class="btn btn-primary view-details" data-bs-toggle="modal" data-bs-target="#detailsModal" data-title="Modern Apartment" data-desc="Urban living at its finest." data-price="$1,200/mo" data-img="https://images.unsplash.com/photo-1570129477492-45c003edd2be?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80">View Details</button>
                    </div>
                </div>
            </div>
            <div class="col-md-4 listing-item" data-search="spacious family home elsewhere oak ave">
                <div class="listing">
                    <img src="https://images.unsplash.com/photo-1518780664697-55e3ad937233?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="House 3">
                    <div class="p-3">
                        <h5>Spacious Family Home</h5>
                        <p>$350,000 | 3 Baths | 2,200 Sq Ft</p>
                        <p>789 Oak Ave, Elsewhere, USA</p>
                        <button class="btn btn-primary view-details" data-bs-toggle="modal" data-bs-target="#detailsModal" data-title="Spacious Family Home" data-desc="Perfect for growing families." data-price="$350,000" data-img="https://images.unsplash.com/photo-1518780664697-55e3ad937233?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80">View Details</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Details Modal -->
    <div class="modal fade" id="detailsModal" tabindex="-1">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="modalTitle"></h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
                </div>
                <div class="modal-body">
                    <img id="modalImg" src="" alt="Property" class="img-fluid mb-3">
                    <p id="modalDesc"></p>
                    <p><strong>Price:</strong> <span id="modalPrice"></span></p>
                </div>
            </div>
        </div>
    </div>

    <!-- Contact Section -->
    <section id="contact" class="container my-5">
        <h2 class="text-center mb-4">Contact Us</h2>
        <form id="contactForm">
            <div class="mb-3">
                <label for="name" class="form-label">Name</label>
                <input type="text" class="form-control" id="name" required>
            </div>
            <div class="mb-3">
                <label for="email" class="form-label">Email</label>
                <input type="email" class="form-control" id="email" required>
            </div>
            <div class="mb-3">
                <label for="message" class="form-label">Message</label>
                <textarea class="form-control" id="message" rows="3" required></textarea>
            </div>
            <button type="submit" class="btn btn-success">Send Message</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2023 Cheap House US. All rights reserved.</p>
            <p>Contact: jackgahan11@gmail.com</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Hero Carousel
        let carouselImages = document.querySelectorAll('#heroCarousel img');
        let currentImage = 0;
        setInterval(() => {
            carouselImages[currentImage].classList.remove('active');
            currentImage = (currentImage + 1) % carouselImages.length;
            carouselImages[currentImage].classList.add('active');
        }, 3000);

        // Search Functionality
        document.getElementById('searchForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const query = document.getElementById('searchInput').value.toLowerCase();
            const listings = document.querySelectorAll('.listing-item');
            listings.forEach(listing => {
                const searchText = listing.getAttribute('data-search').toLowerCase();
                if (searchText.includes(query)) {
                    listing.classList.remove('hidden');
                } else {
                    listing.classList.add('hidden');
                }
            });
        });

        // Modal Details
        document.querySelectorAll('.view-details').forEach(button => {
            button.addEventListener('click', function() {
                document.getElementById('modalTitle').textContent = this.getAttribute('data-title');
                document.getElementById('modalDesc').textContent = this.getAttribute('data-desc');
                document.getElementById('modalPrice').textContent = this.getAttribute('data-price');
                document.getElementById('modalImg').src = this.getAttribute('data-img');
            });
        });

        // Contact Form Validation and Submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

            if (!name || !email || !message) {
                alert('Please fill in all fields.');
                return;
            }
            if (!emailRegex.test(email)) {
                alert('Please enter a valid email address.');
                return;
            }
            alert('Thank you for your message! We will get back to you soon.');
            this.reset();
        });
    </script>
</body>
</html>
