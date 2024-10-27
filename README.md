<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AutoInsight - Car Repair Services</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="header">
        <img src="/mnt/data/Autoinsight.jpg" alt="AutoInsight Logo" class="logo">
        <h1>Welcome to AutoInsight</h1>
        <p>Your trusted partner for sustainable car maintenance and repair</p>
    </header>

    <section class="container">
        <h2>Our Services</h2>
        
        <!-- Service Options -->
        <div class="card" id="basicService">
            <h3 class="service-title">Basic Maintenance</h3>
            <p>Price: ₹8000</p>
            <button onclick="selectService('Basic Maintenance', 8000)">Choose Service</button>
        </div>

        <div class="card" id="advancedService">
            <h3 class="service-title">Advanced Repair</h3>
            <p>Price: ₹20000</p>
            <button onclick="selectService('Advanced Repair', 20000)">Choose Service</button>
        </div>

        <div class="card" id="premiumService">
            <h3 class="service-title">Full Sustainability Package</h3>
            <p>Price: ₹40000</p>
            <button onclick="selectService('Full Sustainability Package', 40000)">Choose Service</button>
        </div>

        <!-- Customization Options -->
        <h2>Customization Options</h2>
        <div class="customization">
            <label><input type="checkbox" onchange="toggleCustomization('Eco-Friendly Parts', 3000)"> Eco-Friendly Parts (+₹3000)</label>
        </div>
        <div class="customization">
            <label><input type="checkbox" onchange="toggleCustomization('Extended Warranty', 5000)"> Extended Warranty (+₹5000)</label>
        </div>
        <div class="customization">
            <label><input type="checkbox" onchange="toggleCustomization('Performance Tuning', 7000)"> Performance Tuning (+₹7000)</label>
        </div>

        <!-- Total Cost -->
        <h2>Total Cost: ₹<span id="totalCost">0</span></h2>

        <!-- Car Repair and Development Photos -->
        <h2>Car Repair and Development</h2>
        <div class="images">
            <img src="https://via.placeholder.com/500x300.png?text=Car+Repair+Photo+1" alt="Car Repair Photo 1">
            <img src="https://via.placeholder.com/500x300.png?text=Car+Repair+Photo+2" alt="Car Repair Photo 2">
        </div>

        <!-- Executive Team Section -->
        <h2>Our Executive Team</h2>
        
        <div class="executive">
            <img src="https://via.placeholder.com/100" alt="CEO Image">
            <div>
                <h3>CEO: Shrijay Naik</h3>
                <p>Email: <a href="mailto:naikshrijay719@gmail.com.com">ceo@autoinsight.com</a></p>
                <p>Phone: +91 7620385689</p>
            </div>
        </div>

        <div class="executive">
            <img src="https://via.placeholder.com/100" alt="CFO Image">
            <div>
                <h3>CFO: Potli Cheritha </h3>
            </div>
        </div>

        <div class="executive">
            <img src="https://via.placeholder.com/100" alt="CTO Image">
            <div>
                <h3>CTO: Mothukuri Anwika</h3>
            </div>
        </div>
    </section>

    <footer class="footer">
        <p>&copy; 2024 AutoInsight. All Rights Reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
