# Make-My-Trip
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Travel Booking</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            min-height: 100vh;
            background: linear-gradient(to bottom, #2563eb, #60a5fa);
        }

        /* Navigation Styles */
        nav {
            padding: 1rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            gap: 1.5rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
        }

        .nav-auth {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .login-btn {
            color: white;
            background: none;
            border: none;
            cursor: pointer;
        }

        .signup-btn {
            background: white;
            color: #2563eb;
            padding: 0.5rem 1rem;
            border: none;
            border-radius: 9999px;
            cursor: pointer;
        }

        /* Special Fares */
        .special-fares {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0;
        }

        .fare-category {
            background: rgba(255, 255, 255, 0.1);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 9999px;
            cursor: pointer;
        }

        .fare-category:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        /* Search Box */
        .search-box {
            background: white;
            max-width: 900px;
            margin: 0 auto;
            padding: 1.5rem;
            border-radius: 0.5rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .trip-types {
            display: flex;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .trip-type {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .search-form {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 1rem;
        }

        .input-group {
            border: 1px solid #e5e7eb;
            padding: 0.75rem;
            border-radius: 0.5rem;
            cursor: pointer;
        }

        .input-group:hover {
            border-color: #2563eb;
        }

        .input-label {
            font-size: 0.75rem;
            color: #6b7280;
            margin-bottom: 0.25rem;
        }

        .input-content {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .input-content i {
            color: #9ca3af;
        }

        .input-content input {
            border: none;
            outline: none;
            width: 100%;
        }

        .search-btn {
            display: block;
            margin: 1.5rem auto 0;
            background: #2563eb;
            color: white;
            padding: 0.75rem 3rem;
            border: none;
            border-radius: 0.5rem;
            font-weight: 600;
            cursor: pointer;
        }

        .search-btn:hover {
            background: #1d4ed8;
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav>
        <div class="container">
            <div class="nav-content">
                <div class="logo">TravelEase</div>
                <div class="nav-links">
                    <a href="#">Flights</a>
                    <a href="#">Hotels</a>
                    <a href="#">Holidays</a>
                    <a href="#">Trains</a>
                    <a href="#">Buses</a>
                </div>
                <div class="nav-auth">
                    <button class="login-btn">Login</button>
                    <button class="signup-btn">Sign Up</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Special Fares -->
    <div class="container">
        <div class="special-fares">
            <div class="fare-category">Student Fares</div>
            <div class="fare-category">Armed Forces</div>
            <div class="fare-category">Senior Citizen</div>
            <div class="fare-category">Special Offers</div>
        </div>

        <!-- Search Box -->
        <div class="search-box">
            <!-- Trip Types -->
            <div class="trip-types">
                <label class="trip-type">
                    <input type="radio" name="tripType" checked>
                    <span>Round Trip</span>
                </label>
                <label class="trip-type">
                    <input type="radio" name="tripType">
                    <span>One Way</span>
                </label>
                <label class="trip-type">
                    <input type="radio" name="tripType">
                    <span>Multi City</span>
                </label>
            </div>

            <!-- Search Form -->
            <div class="search-form">
                <!-- From -->
                <div class="input-group">
                    <div class="input-label">FROM</div>
                    <div class="input-content">
                        <i class="fas fa-map-marker-alt"></i>
                        <input type="text" placeholder="Delhi" readonly>
                    </div>
                </div>

                <!-- To -->
                <div class="input-group">
                    <div class="input-label">TO</div>
                    <div class="input-content">
                        <i class="fas fa-map-marker-alt"></i>
                        <input type="text" placeholder="Mumbai" readonly>
                    </div>
                </div>

                <!-- Departure -->
                <div class="input-group">
                    <div class="input-label">DEPARTURE</div>
                    <div class="input-content">
                        <i class="far fa-calendar"></i>
                        <input type="text" placeholder="30 Jan" readonly>
                    </div>
                </div>

                <!-- Return -->
                <div class="input-group">
                    <div class="input-label">RETURN</div>
                    <div class="input-content">
                        <i class="far fa-calendar"></i>
                        <input type="text" placeholder="31 Jan" readonly>
                    </div>
                </div>

                <!-- Travelers & Class -->
                <div class="input-group">
                    <div class="input-label">TRAVELERS & CLASS</div>
                    <div class="input-content">
                        <i class="fas fa-user"></i>
                        <input type="text" placeholder="1 Adult" readonly>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </div>

            <!-- Search Button -->
            <button class="search-btn">Search Flights</button>
        </div>
    </div>
</body>
</html>
