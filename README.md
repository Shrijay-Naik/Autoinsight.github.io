<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AutoInsight - Car Repair Services</title>
    <style>
        /* Basic Styling */
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f9f9f9; color: #333; }
        .header { background-color: #005f73; color: #fff; padding: 1em; text-align: center; }
        .container { padding: 2em; max-width: 1200px; margin: auto; }
        
        /* Logo Styling */
        .logo { max-width: 150px; margin-bottom: 10px; }
        
        /* Service and Customization Cards */
        .card { border: 1px solid #ddd; border-radius: 8px; box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1); margin-bottom: 1em; padding: 1.5em; background-color: #fff; }
        .service-title { color: #005f73; }
        button { background-color: #0a9396; color: white; border: none; padding: 0.5em 1em; border-radius: 5px; cursor: pointer; }
        button:hover { background-color: #007f8c; }
        
        /* Customization Section */
        .customization { margin: 0.5em 0; }
        
        /* Image Gallery */
        .images img { width: 100%; height: auto; margin-top: 10px; border-radius: 8px; }
        
        /* Executive Team Section */
        .executive { display: flex; align-items: center; gap: 20px; margin-top: 1em; }
        .executive img { width: 100px; border-radius: 50%; border: 3px solid #ddd; }
        .executive h3 { margin: 0; color: #005f73; }
        
        /* Footer */
        .footer { background-color: #005f73; color: #fff; padding: 1em; text-align: center; }
    </style>
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
                <h3>CEO: John Doe</h3>
                <p>Email: <a href="mailto:ceo@autoinsight.com">ceo@autoinsight.com</a></p>
                <p>Phone: 123-456-7890</p>
            </div>
        </div>

        <div class="executive">
            <img src="https://via.placeholder.com/100" alt="CFO Image">
            <div>
                <h3>CFO: Jane Smith</h3>
            </div>
        </div>

        <div class="executive">
            <img src="https://via.placeholder.com/100" alt="CTO Image">
            <div>
                <h3>CTO: Alice Johnson</h3>
            </div>
        </div>
    </section>

    <footer class="footer">
        <p>&copy; 2024 AutoInsight. All Rights Reserved.</p>
    </footer>

    <script>
        // JavaScript Functions

        let selectedService = null;
        let totalCost = 0;
        const customizations = [];

        // Function to select a service
        function selectService(serviceName, price) {
            selectedService = { serviceName, price };
            calculateTotal();
            alert(serviceName + " selected for ₹" + price);
        }

        // Function to toggle customizations
        function toggleCustomization(name, price) {
            const index = customizations.findIndex(cust => cust.name === name);
            if (index > -1) {
                customizations.splice(index, 1);
            } else {
                customizations.push({ name, price });
            }
            calculateTotal();
        }

        // Function to calculate total cost
        function calculateTotal() {
            totalCost = selectedService ? selectedService.price : 0;
            customizations.forEach(custom => totalCost += custom.price);
            document.getElementById('totalCost').innerText = totalCost;
        }
    </script>
</body>
</html>

