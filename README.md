# CleanConnect-Cyprus
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CleanConnect Cyprus - Find Professional Cleaners Easily</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background-color: #f4f7fa;
            color: #333;
        }

        header {
            background-color: #2c3e50;
            color: white;
            padding: 1rem;
            text-align: center;
        }

        header h1 {
            margin-bottom: 0.5rem;
        }

        nav {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 1rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        nav a:hover {
            color: #3498db;
        }

        .language-selector {
            width: 150px; /* Approx. 3.75 cm */
            min-width: 120px; /* Prevent collapse on mobile */
            padding: 0.3rem;
            border-radius: 3px;
            font-size: 0.9rem;
        }

        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        .stats-section {
            display: flex;
            justify-content: space-around;
            background-color: #3498db;
            color: white;
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 2rem;
            text-align: center;
        }

        .stats-section div {
            flex: 1;
        }

        .stats-section h2 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .section {
            background-color: white;
            padding: 2rem;
            margin-bottom: 2rem;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .section h2 {
            color: #2c3e50;
            margin-bottom: 1rem;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .form-group {
            border: 1px solid #eee;
            padding: 1rem;
            border-radius: 4px;
            margin-bottom: 1rem;
        }

        .form-group legend {
            font-weight: bold;
            color: #2c3e50;
            padding: 0 0.5rem;
        }

        label {
            font-weight: bold;
            display: block;
            margin-bottom: 0.25rem;
        }

        input, select, textarea, button {
            padding: 0.5rem;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1rem;
            width: 100%;
        }

        select[multiple] {
            height: 100px;
        }

        .checkbox-group, .radio-group {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 0.75rem;
            margin-bottom: 1rem;
        }

        .checkbox-group label, .radio-group label {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-weight: normal;
            cursor: pointer;
        }

        .checkbox-group input, .radio-group input {
            width: 1.2rem;
            height: 1.2rem;
        }

        button {
            background-color: #3498db;
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #2980b9;
        }

        .admin-action-btn {
            background-color: #e74c3c;
            margin-left: 0.5rem;
        }

        .admin-action-btn:hover {
            background-color: #c0392b;
        }

        .user-list {
            margin-top: 1rem;
        }

        .user-card {
            border: 1px solid #ccc;
            padding: 1rem;
            margin-bottom: 1rem;
            border-radius: 4px;
            display: flex;
            gap: 1rem;
            align-items: center;
            transition: transform 0.2s;
        }

        .user-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .user-card img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
        }

        .user-card .info {
            flex: 1;
        }

        .message-btn {
            background-color: #2ecc71;
            padding: 0.5rem 1rem;
        }

        .message-btn:hover {
            background-color: #27ae60;
        }

        .forgot-password, .change-password {
            color: #3498db;
            text-decoration: none;
            margin-top: 0.5rem;
            display: inline-block;
        }

        .forgot-password:hover, .change-password:hover {
            text-decoration: underline;
        }

        .filter-section {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 1rem;
            align-items: flex-start;
        }

        .filter-section input[type="text"] {
            flex: 1;
            min-width: 200px;
        }

        .filter-section select[multiple] {
            height: 120px;
            padding: 0.5rem;
        }

        .filter-section .checkbox-group {
            border: 1px solid #eee;
            padding: 1rem;
            border-radius: 4px;
        }

        .match-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .match-card {
            background: white;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 1rem;
            transition: transform 0.2s;
        }

        .match-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .match-card img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            margin-bottom: 0.5rem;
        }

        .match-card h4 {
            margin: 0.5rem 0;
            color: #2c3e50;
        }

        .match-card p {
            font-size: 0.9rem;
            color: #555;
        }

        .tooltip {
            position: relative;
            display: inline-block;
        }

        .tooltip .tooltiptext {
            visibility: hidden;
            width: 200px;
            background-color: #555;
            color: #fff;
            text-align: center;
            border-radius: 4px;
            padding: 0.5rem;
            position: absolute;
            z-index: 1;
            bottom: 125%;
            left: 50%;
            transform: translateX(-50%);
            opacity: 0;
            transition: opacity 0.3s;
        }

        .tooltip:hover .tooltiptext {
            visibility: visible;
            opacity: 1;
        }

        .prompt-message {
            background-color: #fff3cd;
            border: 1px solid #ffeeba;
            padding: 1rem;
            border-radius: 4px;
            margin-bottom: 1rem;
            text-align: center;
        }

        .prompt-message a {
            color: #3498db;
            text-decoration: underline;
        }

        .prompt-message a:hover {
            color: #2980b9;
        }

        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 1rem;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        @media (max-width: 768px) {
            .container {
                margin: 1rem;
            }

            .stats-section {
                flex-direction: column;
                gap: 1rem;
            }

            .section {
                padding: 1rem;
            }

            nav {
                flex-direction: column;
            }

            nav a {
                margin: 0.5rem 0;
            }

            .user-card {
                flex-direction: column;
                gap: 0.5rem;
                text-align: center;
            }

            .user-card img {
                width: 60px;
                height: 60px;
            }

            .filter-section {
                flex-direction: column;
                align-items: stretch;
            }

            .match-grid {
                grid-template-columns: 1fr;
            }

            .checkbox-group, .radio-group {
                grid-template-columns: 1fr;
                gap: 0.5rem;
            }

            .form-group {
                padding: 0.75rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1 data-i18n="title">CleanConnect Cyprus</h1>
        <nav>
            <select class="language-selector" id="language-selector" onchange="changeLanguage(this.value)">
                <option value="en">English</option>
                <option value="el">Greek</option>
                <option value="th">Thai</option>
                <option value="ur">Urdu</option>
                <option value="hi">Hindi</option>
            </select>
            <a href="#login" data-i18n="nav-login">Login</a>
            <a href="#register" data-i18n="nav-register">Register</a>
            <a href="#find-match" id="find-match-nav" style="display: none;" data-i18n="nav-find-match">Find a Match</a>
            <a href="#admin" id="admin-nav" style="display: none;" data-i18n="nav-admin">Admin Panel</a>
        </nav>
    </header>

    <div class="container">
        <div class="stats-section">
            <div>
                <h2 id="professional-cleaner-count">0</h2>
                <p data-i18n="stats-professional-cleaners">Available Professional Cleaners in Cyprus</p>
            </div>
            <div>
                <h2 id="client-count">0</h2>
                <p data-i18n="stats-clients">Clients Searching in Cyprus</p>
            </div>
        </div>

        <div class="section" id="login">
            <h2 data-i18n="login-title">Login</h2>
            <form id="login-form" onsubmit="handleLogin(event)">
                <label for="username" data-i18n="login-email">Email:</label>
                <input type="email" id="username" required>

                <label for="password" data-i18n="login-password">Password:</label>
                <input type="password" id="password" required>

                <button type="submit" data-i18n="login-button">Login</button>
                <a href="#" class="forgot-password" onclick="handleForgotPassword()" data-i18n="forgot-password">Forgot Password?</a>
            </form>
            <form id="change-password-form" style="display: none; margin-top: 1rem;" onsubmit="handleChangePassword(event)">
                <h3 data-i18n="change-password-title">Change Password</h3>
                <label for="current-password" data-i18n="current-password">Current Password:</label>
                <input type="password" id="current-password" required>

                <label for="new-password" data-i18n="new-password">New Password:</label>
                <input type="password" id="new-password" required>

                <button type="submit" data-i18n="change-password-button">Change Password</button>
            </form>
            <a href="#" class="change-password" onclick="toggleChangePasswordForm()" data-i18n="change-password-link">Change Password</a>
        </div>

        <div class="section" id="register">
            <h2 data-i18n="register-title">Register on CleanConnect Cyprus</h2>
            <form id="register-form" onsubmit="handleRegister(event)">
                <label for="register-username" data-i18n="register-username">Username:</label>
                <input type="text" id="register-username" required>

                <label for="register-email" data-i18n="register-email">Email:</label>
                <input type="email" id="register-email" required>

                <label for="register-password" data-i18n="register-password">Password:</label>
                <input type="password" id="register-password" required>

                <label for="register-type" data-i18n="register-type">I am a:</label>
                <select id="register-type" required>
                    <option value="" data-i18n="select-role">Select your role</option>
                    <option value="client" data-i18n="role-client">Client (Need a Professional Cleaner, €5/month)</option>
                    <option value="professional-cleaner" data-i18n="role-professional-cleaner">Professional Cleaner (Free)</option>
                </select>

                <button type="submit" data-i18n="register-button">Register</button>
            </form>
        </div>

        <div class="section" id="complete-profile" style="display: none;">
            <h2 data-i18n="complete-profile-title">Complete Your Profile</h2>
            <form id="complete-profile-form" onsubmit="handleCompleteProfile(event)">
                <label for="complete-name" data-i18n="profile-name">Full Name:</label>
                <input type="text" id="complete-name" required>

                <label for="complete-profile-photo" data-i18n="profile-photo">Profile Photo URL:</label>
                <input type="url" id="complete-profile-photo" placeholder="https://example.com/photo.jpg">

                <label for="complete-bio" data-i18n="profile-bio">Short Bio:</label>
                <textarea id="complete-bio" rows="3"></textarea>

                <div class="form-group">
                    <legend data-i18n="profile-districts">Districts and Municipalities in Cyprus</legend>
                    <label for="complete-districts" data-i18n="districts">Districts:</label>
                    <select id="complete-districts" multiple required onchange="updateMunicipalityOptions('complete')">
                        <option value="Nicosia" data-i18n="district-nicosia">Nicosia</option>
                        <option value="Limassol" data-i18n="district-limassol">Limassol</option>
                        <option value="Larnaca" data-i18n="district-larnaca">Larnaca</option>
                        <option value="Paphos" data-i18n="district-paphos">Paphos</option>
                        <option value="Famagusta" data-i18n="district-famagusta">Famagusta</option>
                        <option value="Kyrenia" data-i18n="district-kyrenia">Kyrenia</option>
                    </select>
                    <div id="complete-municipality-container"></div>
                </div>

                <div id="complete-professional-cleaner-details" style="display: none;">
                    <div class="form-group">
                        <legend data-i18n="professional-details">Professional Details</legend>
                        <label for="years-cyprus" data-i18n="years-cyprus">Years in Cyprus:</label>
                        <select id="years-cyprus" required>
                            <option value="" data-i18n="select-years">Select years</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                            <option value="6">6</option>
                            <option value="7">7</option>
                            <option value="8">8</option>
                            <option value="9">9</option>
                            <option value="10">10</option>
                            <option value="11">11</option>
                            <option value="12">12</option>
                            <option value="13">13</option>
                            <option value="14">14</option>
                            <option value="15">15</option>
                            <option value="16">16</option>
                            <option value="17">17</option>
                            <option value="18">18</option>
                            <option value="19">19</option>
                            <option value="20">20</option>
                        </select>

                        <label for="nationality" data-i18n="nationality">Nationality:</label>
                        <select id="nationality" required>
                            <option value="" data-i18n="select-nationality">Select nationality</option>
                            <option value="Cypriot">Cypriot</option>
                            <option value="British">British</option>
                            <option value="Indian">Indian</option>
                            <option value="Filipino">Filipino</option>
                            <option value="Greek">Greek</option>
                            <option value="Russian">Russian</option>
                            <option value="Sri Lankan">Sri Lankan</option>
                            <option value="Other">Other</option>
                        </select>

                        <label for="english-level" data-i18n="english-level">English Level (1–5):</label>
                        <select id="english-level" required>
                            <option value="" data-i18n="select-level">Select level</option>
                            <option value="1">1 (Basic)</option>
                            <option value="2">2</option>
                            <option value="3">3 (Intermediate)</option>
                            <option value="4">4</option>
                            <option value="5">5 (Fluent)</option>
                        </select>

                        <label for="greek-level" data-i18n="greek-level">Greek Level (1–5):</label>
                        <select id="greek-level" required>
                            <option value="" data-i18n="select-level">Select level</option>
                            <option value="1">1 (Basic)</option>
                            <option value="2">2</option>
                            <option value="3">3 (Intermediate)</option>
                            <option value="4">4</option>
                            <option value="5">5 (Fluent)</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <legend data-i18n="services-provided">Services Provided</legend>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="services-provided" value="cleaning"> <span data-i18n="service-cleaning">Cleaning</span></label>
                            <label><input type="checkbox" name="services-provided" value="cooking"> <span data-i18n="service-cooking">Cooking</span></label>
                            <label><input type="checkbox" name="services-provided" value="babysitting"> <span data-i18n="service-babysitting">Babysitting</span></label>
                            <label><input type="checkbox" name="services-provided" value="ironing"> <span data-i18n="service-ironing">Ironing</span></label>
                            <label><input type="checkbox" name="services-provided" value="gardening"> <span data-i18n="service-gardening">Gardening</span></label>
                            <label><input type="checkbox" name="services-provided" value="animal-care"> <span data-i18n="service-animal-care">Animal Care</span></label>
                        </div>
                    </div>

                    <div class="form-group">
                        <legend data-i18n="additional-details">Additional Details</legend>
                        <label for="drivers-license" data-i18n="drivers-license">Driver’s License:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="drivers-license" value="yes" required> <span data-i18n="yes">Yes</span></label>
                            <label><input type="radio" name="drivers-license" value="no"> <span data-i18n="no">No</span></label>
                        </div>

                        <label for="cleaning-experience" data-i18n="cleaning-experience">Years of Cleaning Experience:</label>
                        <select id="cleaning-experience" required>
                            <option value="" data-i18n="select-years">Select years</option>
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                            <option value="6">6</option>
                            <option value="7">7</option>
                            <option value="8">8</option>
                            <option value="9">9</option>
                            <option value="10">10</option>
                            <option value="11">11</option>
                            <option value="12">12</option>
                            <option value="13">13</option>
                            <option value="14">14</option>
                            <option value="15">15</option>
                            <option value="16">16</option>
                            <option value="17">17</option>
                            <option value="18">18</option>
                            <option value="19">19</option>
                            <option value="20">20</option>
                        </select>

                        <label for="recommendations" data-i18n="recommendations">Recommendations Available:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="recommendations" value="yes" required> <span data-i18n="yes">Yes</span></label>
                            <label><input type="radio" name="recommendations" value="no"> <span data-i18n="no">No</span></label>
                        </div>
                    </div>

                    <div class="form-group">
                        <legend data-i18n="rate-details">Rate Details</legend>
                        <label for="hourly-rate" data-i18n="hourly-rate" class="tooltip">
                            Expected Hourly Rate (€):
                            <span class="tooltiptext" data-i18n="hourly-rate-tooltip">Enter your expected pay per hour.</span>
                        </label>
                        <input type="number" id="hourly-rate" min="0" step="0.01" required>

                        <label for="monthly-rate" data-i18n="monthly-rate" class="tooltip">
                            Expected Monthly Rate (Full-Time, 40 hours/week, €):
                            <span class="tooltiptext" data-i18n="monthly-rate-tooltip">Enter your expected pay for a full-time role (40 hours/week).</span>
                        </label>
                        <input type="number" id="monthly-rate" min="0" step="0.01" required>
                    </div>

                    <label for="work-type" data-i18n="work-type">Work Type:</label>
                    <select id="work-type" required onchange="toggleWorkTypeDetails('complete')">
                        <option value="" data-i18n="select-work-type">Select work type</option>
                        <option value="full-time" data-i18n="full-time">Full-time</option>
                        <option value="part-time">Part-time</option>
                    </select>

                    <div id="complete-part-time-details" style="display: none;">
                        <label data-i18n="available-days">Available Days:</label>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="days" value="Monday"> <span data-i18n="day-monday">Monday</span></label>
                            <label><input type="checkbox" name="days" value="Tuesday"> <span data-i18n="day-tuesday">Tuesday</span></label>
                            <label><input type="checkbox" name="days" value="Wednesday"> <span data-i18n="day-wednesday">Wednesday</span></label>
                            <label><input type="checkbox" name="days" value="Thursday"> <span data-i18n="day-thursday">Thursday</span></label>
                            <label><input type="checkbox" name="days" value="Friday"> <span data-i18n="day-friday">Friday</span></label>
                            <label><input type="checkbox" name="days" value="Saturday"> <span data-i18n="day-saturday">Saturday</span></label>
                            <label><input type="checkbox" name="days" value="Sunday"> <span data-i18n="day-sunday">Sunday</span></label>
                        </div>

                        <label for="time-preference" data-i18n="time-preference">Time Preference:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="time" value="morning" required> <span data-i18n="time-morning">Morning</span></label>
                            <label><input type="radio" name="time" value="evening"> <span data-i18n="time-evening">Evening</span></label>
                            <label><input type="radio" name="time" value="both"> <span data-i18n="time-both">Both</span></label>
                        </div>
                    </div>

                    <label for="source-language" data-i18n="source-language">Language of Your Description:</label>
                    <select id="source-language">
                        <option value="en">English</option>
                        <option value="el">Greek</option>
                        <option value="th">Thai</option>
                        <option value="ur">Urdu</option>
                        <option value="hi">Hindi</option>
                    </select>

                    <label for="target-language" data-i18n="target-language">Translate Description To:</label>
                    <select id="target-language">
                        <option value="en">English</option>
                        <option value="el">Greek</option>
                        <option value="th">Thai</option>
                        <option value="ur">Urdu</option>
                        <option value="hi">Hindi</option>
                    </select>
                </div>

                <div id="complete-client-details" style="display: none;">
                    <label for="service-type" data-i18n="service-type">Type of Service Needed:</label>
                    <select id="service-type" required>
                        <option value="" data-i18n="select-service">Select a service</option>
                        <option value="cleaning">Cleaning</option>
                        <option value="cooking">Cooking</option>
                        <option value="babysitting">Babysitting</option>
                        <option value="ironing">Ironing</option>
                        <option value="gardening">Gardening</option>
                        <option value="animal-care">Animal Care</option>
                    </select>

                    <label for="preferred-work-type" data-i18n="preferred-work-type">Preferred Work Type:</label>
                    <select id="preferred-work-type" required onchange="toggleWorkTypeClientDetails('complete')">
                        <option value="" data-i18n="select-work-type">Select preferred work type</option>
                        <option value="any">Any</option>
                        <option value="full-time">Full-time</option>
                        <option value="part-time">Part-time</option>
                    </select>

                    <div id="complete-preferred-part-time-details" style="display: none;">
                        <label data-i18n="preferred-days">Preferred Days:</label>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="preferred-days" value="Monday"> <span data-i18n="day-monday">Monday</span></label>
                            <label><input type="checkbox" name="preferred-days" value="Tuesday"> <span data-i18n="day-tuesday">Tuesday</span></label>
                            <label><input type="checkbox" name="preferred-days" value="Wednesday"> <span data-i18n="day-wednesday">Wednesday</span></label>
                            <label><input type="checkbox" name="preferred-days" value="Thursday"> <span data-i18n="day-thursday">Thursday</span></label>
                            <label><input type="checkbox" name="preferred-days" value="Friday"> <span data-i18n="day-friday">Friday</span></label>
                            <label><input type="checkbox" name="preferred-days" value="Saturday"> <span data-i18n="day-saturday">Saturday</span></label>
                            <label><input type="checkbox" name="preferred-days" value="Sunday"> <span data-i18n="day-sunday">Sunday</span></label>
                        </div>

                        <label for="preferred-time" data-i18n="preferred-time">Preferred Time:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="preferred-time" value="any" required> <span data-i18n="time-any">Any</span></label>
                            <label><input type="radio" name="preferred-time" value="morning"> <span data-i18n="time-morning">Morning</span></label>
                            <label><input type="radio" name="preferred-time" value="evening"> <span data-i18n="time-evening">Evening</span></label>
                        </div>
                    </div>
                </div>

                <button type="submit" data-i18n="submit-profile-button">Submit Profile</button>
            </form>
        </div>

        <div class="section" id="profile" style="display: none;">
            <h2 data-i18n="profile-title">Your Profile</h2>
            <form id="profile-form" onsubmit="handleUpdateProfile(event)">
                <label for="profile-username" data-i18n="profile-username">Username:</label>
                <input type="text" id="profile-username" disabled>

                <label for="profile-email" data-i18n="profile-email">Email:</label>
                <input type="email" id="profile-email" disabled>

                <label for="profile-name" data-i18n="profile-name">Full Name:</label>
                <input type="text" id="profile-name" required>

                <label for="profile-photo" data-i18n="profile-photo">Profile Photo URL:</label>
                <input type="url" id="profile-photo" placeholder="https://example.com/photo.jpg">

                <label for="profile-bio" data-i18n="profile-bio">Short Bio:</label>
                <textarea id="profile-bio" rows="3"></textarea>

                <div class="form-group">
                    <legend data-i18n="profile-districts">Districts and Municipalities in Cyprus</legend>
                    <label for="profile-districts" data-i18n="districts">Districts:</label>
                    <select id="profile-districts" multiple required onchange="updateMunicipalityOptions('profile')">
                        <option value="Nicosia" data-i18n="district-nicosia">Nicosia</option>
                        <option value="Limassol" data-i18n="district-limassol">Limassol</option>
                        <option value="Larnaca" data-i18n="district-larnaca">Larnaca</option>
                        <option value="Paphos" data-i18n="district-paphos">Paphos</option>
                        <option value="Famagusta" data-i18n="district-famagusta">Famagusta</option>
                        <option value="Kyrenia" data-i18n="district-kyrenia">Kyrenia</option>
                    </select>
                    <div id="profile-municipality-container"></div>
                </div>

                <div id="profile-professional-cleaner-details" style="display: none;">
                    <div class="form-group">
                        <legend data-i18n="professional-details">Professional Details</legend>
                        <label for="profile-years-cyprus" data-i18n="years-cyprus">Years in Cyprus:</label>
                        <select id="profile-years-cyprus" required>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                            <option value="6">6</option>
                            <option value="7">7</option>
                            <option value="8">8</option>
                            <option value="9">9</option>
                            <option value="10">10</option>
                            <option value="11">11</option>
                            <option value="12">12</option>
                            <option value="13">13</option>
                            <option value="14">14</option>
                            <option value="15">15</option>
                            <option value="16">16</option>
                            <option value="17">17</option>
                            <option value="18">18</option>
                            <option value="19">19</option>
                            <option value="20">20</option>
                        </select>

                        <label for="profile-nationality" data-i18n="nationality">Nationality:</label>
                        <select id="profile-nationality" required>
                            <option value="Cypriot">Cypriot</option>
                            <option value="British">British</option>
                            <option value="Indian">Indian</option>
                            <option value="Filipino">Filipino</option>
                            <option value="Greek">Greek</option>
                            <option value="Russian">Russian</option>
                            <option value="Sri Lankan">Sri Lankan</option>
                            <option value="Other">Other</option>
                        </select>

                        <label for="profile-english-level" data-i18n="english-level">English Level (1–5):</label>
                        <select id="profile-english-level" required>
                            <option value="1">1 (Basic)</option>
                            <option value="2">2</option>
                            <option value="3">3 (Intermediate)</option>
                            <option value="4">4</option>
                            <option value="5">5 (Fluent)</option>
                        </select>

                        <label for="profile-greek-level" data-i18n="greek-level">Greek Level (1–5):</label>
                        <select id="profile-greek-level" required>
                            <option value="1">1 (Basic)</option>
                            <option value="2">2</option>
                            <option value="3">3 (Intermediate)</option>
                            <option value="4">4</option>
                            <option value="5">5 (Fluent)</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <legend data-i18n="services-provided">Services Provided</legend>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="profile-services-provided" value="cleaning"> <span data-i18n="service-cleaning">Cleaning</span></label>
                            <label><input type="checkbox" name="profile-services-provided" value="cooking"> <span data-i18n="service-cooking">Cooking</span></label>
                            <label><input type="checkbox" name="profile-services-provided" value="babysitting"> <span data-i18n="service-babysitting">Babysitting</span></label>
                            <label><input type="checkbox" name="profile-services-provided" value="ironing"> <span data-i18n="service-ironing">Ironing</span></label>
                            <label><input type="checkbox" name="profile-services-provided" value="gardening"> <span data-i18n="service-gardening">Gardening</span></label>
                            <label><input type="checkbox" name="profile-services-provided" value="animal-care"> <span data-i18n="service-animal-care">Animal Care</span></label>
                        </div>
                    </div>

                    <div class="form-group">
                        <legend data-i18n="additional-details">Additional Details</legend>
                        <label for="profile-drivers-license" data-i18n="drivers-license">Driver’s License:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="profile-drivers-license" value="yes" required> <span data-i18n="yes">Yes</span></label>
                            <label><input type="radio" name="profile-drivers-license" value="no"> <span data-i18n="no">No</span></label>
                        </div>

                        <label for="profile-cleaning-experience" data-i18n="cleaning-experience">Years of Cleaning Experience:</label>
                        <select id="profile-cleaning-experience" required>
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                            <option value="6">6</option>
                            <option value="7">7</option>
                            <option value="8">8</option>
                            <option value="9">9</option>
                            <option value="10">10</option>
                            <option value="11">11</option>
                            <option value="12">12</option>
                            <option value="13">13</option>
                            <option value="14">14</option>
                            <option value="15">15</option>
                            <option value="16">16</option>
                            <option value="17">17</option>
                            <option value="18">18</option>
                            <option value="19">19</option>
                            <option value="20">20</option>
                        </select>

                        <label for="profile-recommendations" data-i18n="recommendations">Recommendations Available:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="profile-recommendations" value="yes" required> <span data-i18n="yes">Yes</span></label>
                            <label><input type="radio" name="profile-recommendations" value="no"> <span data-i18n="no">No</span></label>
                        </div>
                    </div>

                    <div class="form-group">
                        <legend data-i18n="rate-details">Rate Details</legend>
                        <label for="profile-hourly-rate" data-i18n="hourly-rate" class="tooltip">
                            Expected Hourly Rate (€):
                            <span class="tooltiptext" data-i18n="hourly-rate-tooltip">Enter your expected pay per hour.</span>
                        </label>
                        <input type="number" id="profile-hourly-rate" min="0" step="0.01" required>

                        <label for="profile-monthly-rate" data-i18n="monthly-rate" class="tooltip">
                            Expected Monthly Rate (Full-Time, 40 hours/week, €):
                            <span class="tooltiptext" data-i18n="monthly-rate-tooltip">Enter your expected pay for a full-time role (40 hours/week).</span>
                        </label>
                        <input type="number" id="profile-monthly-rate" min="0" step="0.01" required>
                    </div>

                    <label for="profile-work-type" data-i18n="work-type">Work Type:</label>
                    <select id="profile-work-type" required onchange="toggleWorkType('profile')">
                        <option value="full-time" data-i18n="full-time">Full-time</option>
                        <option value="part-time">Part-time</option>
                    </select>

                    <div id="profile-part-time-details" style="display: none;">
                        <label data-i18n="available-days">Available Days:</label>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="profile-days" value="Monday"> <span data-i18n="day-monday">Monday</span></label>
                            <label><input type="checkbox" name="profile-days" value="Tuesday"> <span data-i18n="day-tuesday">Tuesday</span></label>
                            <label><input type="checkbox" name="profile-days" value="Wednesday"> <span data-i18n="day-wednesday">Wednesday</span></label>
                            <label><input type="checkbox" name="profile-days" value="Thursday"> <span data-i18n="day-thursday">Thursday</span></label>
                            <label><input type="checkbox" name="profile-days" value="Friday"> <span data-i18n="day-friday">Friday</span></label>
                            <label><input type="checkbox" name="profile-days" value="Saturday"> <span data-i18n="day-saturday">Saturday</span></label>
                            <label><input type="checkbox" name="profile-days" value="Sunday"> <span data-i18n="day-sunday">Sunday</span></label>
                        </div>

                        <label for="profile-time" data-i18n="time-preference">Time Preference:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="profile-time" value="morning" required> <span data-i18n="time-morning">Morning</span></label>
                            <label><input type="radio" name="profile-time" value="evening"> <span data-i18n="time-evening">Evening</span></label>
                            <label><input type="radio" name="profile-time" value="both"> <span data-i18n="time-both">Both</span></label>
                        </div>
                    </div>

                    <label for="profile-source-language" data-i18n="source-language">Language of Your Description:</label>
                    <select id="profile-source-language">
                        <option value="en">English</option>
                        <option value="el">Greek</option>
                        <option value="th">Thai</option>
                        <option value="ur">Urdu</option>
                        <option value="hi">Hindi</option>
                    </select>

                    <label for="profile-target-language" data-i18n="target-language">Translate Description To:</label>
                    <select id="profile-target-language">
                        <option value="en">English</option>
                        <option value="el">Greek</option>
                        <option value="th">Thai</option>
                        <option value="ur">Urdu</option>
                        <option value="hi">Hindi</option>
                    </select>
                </div>

                <div id="profile-client-details" style="display: none;">
                    <label for="profile-service-type" data-i18n="service-type">Type of Service Needed:</label>
                    <select id="profile-service-type" required>
                        <option value="cleaning">Cleaning</option>
                        <option value="cooking">Cooking</option>
                        <option value="babysitting">Babysitting</option>
                        <option value="ironing">Ironing</option>
                        <option value="gardening">Gardening</option>
                        <option value="animal-care">Animal Care</option>
                    </select>

                    <label for="profile-preferred-work-type" data-i18n="preferred-work-type">Preferred Work Type:</label>
                    <select id="profile-preferred-work-type" required onchange="toggleWorkTypeClientDetails('profile')">
                        <option value="any">Any</option>
                        <option value="full-time">Full-time</option>
                        <option value="part-time">Part-time</option>
                    </select>

                    <div id="profile-preferred-part-time-details" style="display: none;">
                        <label data-i18n="preferred-days">Preferred Days:</label>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="profile-preferred-days" value="Monday"> <span data-i18n="day-monday">Monday</span></label>
                            <label><input type="checkbox" name="profile-preferred-days" value="Tuesday"> <span data-i18n="day-tuesday">Tuesday</span></label>
                            <label><input type="checkbox" name="profile-preferred-days" value="Wednesday"> <span data-i18n="day-wednesday">Wednesday</span></label>
                            <label><input type="checkbox" name="profile-preferred-days" value="Thursday"> <span data-i18n="day-thursday">Thursday</span></label>
                            <label><input type="checkbox" name="profile-preferred-days" value="Friday"> <span data-i18n="day-friday">Friday</span></label>
                            <label><input type="checkbox" name="profile-preferred-days" value="Saturday"> <span data-i18n="day-saturday">Saturday</span></label>
                            <label><input type="checkbox" name="profile-preferred-days" value="Sunday"> <span data-i18n="day-sunday">Sunday</span></label>
                        </div>

                        <label for="profile-preferred-time" data-i18n="preferred-time">Preferred Time:</label>
                        <div class="radio-group">
                            <label><input type="radio" name="profile-preferred-time" value="any" required> <span data-i18n="time-any">Any</span></label>
                            <label><input type="radio" name="profile-preferred-time" value="morning"> <span data-i18n="time-morning">Morning</span></label>
                            <label><input type="radio" name="profile-preferred-time" value="evening"> <span data-i18n="time-evening">Evening</span></label>
                        </div>
                    </div>
                </div>

                <button type="submit" data-i18n="update-profile-button">Update Profile</button>
            </form>
        </div>

        <div class="section" id="admin" style="display: none;">
            <h2 data-i18n="admin-title">Admin Panel</h2>
            <div class="user-list" id="admin-user-list">
                <h3 data-i18n="admin-users">All Users</h3>
                <!-- Admin user list will be dynamically populated here -->
            </div>
        </div>

        <div class="section" id="find-match" style="display: none;">
            <div id="find-match-login-prompt" class="prompt-message">
                <p data-i18n="login-prompt">Please <a href="#login">login</a> or <a href="#register">register</a> to find a match.</p>
            </div>
            <div id="find-match-content" style="display: none;">
                <h2 data-i18n="find-match-title">Find a Match in Cyprus</h2>
                <div class="filter-section">
                    <input type="text" id="search-query" data-i18n-placeholder="search-placeholder" placeholder="Search by name or bio..." oninput="updateMatches()">
                    <select id="filter-type" onchange="updateMatches()">
                        <option value="all" data-i18n="filter-all">All</option>
                        <option value="professional-cleaner" data-i18n="filter-professional-cleaner">Professional Cleaners</option>
                        <option value="client" data-i18n="filter-client">Clients</option>
                    </select>
                    <div class="form-group">
                        <legend data-i18n="filter-districts">Districts and Municipalities</legend>
                        <label for="filter-districts" data-i18n="districts">Districts:</label>
                        <select id="filter-districts" multiple onchange="updateFilterMunicipalityOptions()">
                            <option value="all" data-i18n="filter-all-districts">All Districts</option>
                            <option value="Nicosia" data-i18n="district-nicosia">Nicosia</option>
                            <option value="Limassol" data-i18n="district-limassol">Limassol</option>
                            <option value="Larnaca" data-i18n="district-larnaca">Larnaca</option>
                            <option value="Paphos" data-i18n="district-paphos">Paphos</option>
                            <option value="Famagusta" data-i18n="district-famagusta">Famagusta</option>
                            <option value="Kyrenia" data-i18n="district-kyrenia">Kyrenia</option>
                        </select>
                        <div id="filter-municipality-container"></div>
                    </div>
                    <div class="form-group">
                        <legend data-i18n="filter-services">Services</legend>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="filter-services" value="cleaning"> <span data-i18n="service-cleaning">Cleaning</span></label>
                            <label><input type="checkbox" name="filter-services" value="cooking"> <span data-i18n="service-cooking">Cooking</span></label>
                            <label><input type="checkbox" name="filter-services" value="babysitting"> <span data-i18n="service-babysitting">Babysitting</span></label>
                            <label><input type="checkbox" name="filter-services" value="ironing"> <span data-i18n="service-ironing">Ironing</span></label>
                            <label><input type="checkbox" name="filter-services" value="gardening"> <span data-i18n="service-gardening">Gardening</span></label>
                            <label><input type="checkbox" name="filter-services" value="animal-care"> <span data-i18n="service-animal-care">Animal Care</span></label>
                        </div>
                    </div>
                    <select id="filter-work-type" onchange="updateMatches()">
                        <option value="all" data-i18n="filter-all-work-types">All Work Types</option>
                        <option value="full-time" data-i18n="full-time">Full-Time</option>
                        <option value="part-time" data-i18n="part-time">Part-Time</option>
                    </select>
                    <div class="form-group">
                        <legend data-i18n="filter-days">Available Days</legend>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="filter-days" value="Monday"> <span data-i18n="day-monday">Monday</span></label>
                            <label><input type="checkbox" name="filter-days" value="Tuesday"> <span data-i18n="day-tuesday">Tuesday</span></label>
                            <label><input type="checkbox" name="filter-days" value="Wednesday"> <span data-i18n="day-wednesday">Wednesday</span></label>
                            <label><input type="checkbox" name="filter-days" value="Thursday"> <span data-i18n="day-thursday">Thursday</span></label>
                            <label><input type="checkbox" name="filter-days" value="Friday"> <span data-i18n="day-friday">Friday</span></label>
                            <label><input type="checkbox" name="filter-days" value="Saturday"> <span data-i18n="day-saturday">Saturday</span></label>
                            <label><input type="checkbox" name="filter-days" value="Sunday"> <span data-i18n="day-sunday">Sunday</span></label>
                        </div>
                    </div>
                    <select id="filter-time" onchange="updateMatches()">
                        <option value="all" data-i18n="filter-all-times">All Times</option>
                        <option value="morning" data-i18n="time-morning">Morning</option>
                        <option value="evening" data-i18n="time-evening">Evening</option>
                        <option value="both" data-i18n="time-both">Both</option>
                        <option value="any" data-i18n="time-any">Any</option>
                    </select>
                    <select id="filter-experience" onchange="updateMatches()">
                        <option value="all" data-i18n="filter-all-experience">All Experience</option>
                        <option value="1-5">1–5 Years</option>
                        <option value="6-10">6–10 Years</option>
                        <option value="11-20">11–20 Years</option>
                    </select>
                    <select id="sort-by" onchange="sortBy()">
                        <option value="recent" data-i18n="sort-recent">Sort by Recent</option>
                    </select>
                </div>
                <div class="match-grid" id="match-grid">
                    <!-- Matches will be dynamically added here -->
                </div>
            </div>
        </div>

    <footer>
        <p data-i18n="footer">Contact Us: info@cleanconnectcyprus.com | © 2025 CleanConnect Cyprus</p>
    </footer>

    <script>
        // Translation dictionary
        const translations = {
            en: {
                title: "CleanConnect Cyprus",
                "nav-login": "Login",
                "nav-register": "Register",
                "nav-find-match": "Find a Match",
                "nav-admin": "Admin Panel",
                "stats-professional-cleaners": "Available Professional Cleaners in Cyprus",
                "stats-clients": "Clients Searching in Cyprus",
                "login-title": "Login",
                "login-email": "Email:",
                "login-password": "Password:",
                "login-button": "Login",
                "forgot-password": "Forgot Password?",
                "change-password-title": "Change Password",
                "current-password": "Current Password:",
                "new-password": "New Password:",
                "change-password-button": "Change Password",
                "change-password-link": "Change Password",
                "register-title": "Register on CleanConnect Cyprus",
                "register-username": "Username:",
                "register-email": "Email:",
                "register-password": "Password:",
                "register-type": "I am a:",
                "select-role": "Select your role",
                "role-client": "Client (Need a Professional Cleaner, €5/month)",
                "role-professional-cleaner": "Professional Cleaner (Free)",
                "register-button": "Register",
                "complete-profile-title": "Complete Your Profile",
                "profile-name": "Full Name:",
                "profile-photo": "Profile Photo URL:",
                "profile-bio": "Short Bio:",
                "profile-districts": "Districts and Municipalities in Cyprus",
                "districts": "Districts:",
                "municipalities": "Municipalities for {district}:",
                "district-nicosia": "Nicosia",
                "district-limassol": "Limassol",
                "district-larnaca": "Larnaca",
                "district-paphos": "Paphos",
                "district-famagusta": "Famagusta",
                "district-kyrenia": "Kyrenia",
                "municipality-nicosia-nicosia": "Nicosia",
                "municipality-nicosia-strovolos": "Strovolos",
                "municipality-nicosia-lakatamia": "Lakatamia",
                "municipality-nicosia-engomi": "Engomi",
                "municipality-limassol-limassol": "Limassol",
                "municipality-limassol-ypsonas": "Ypsonas",
                "municipality-limassol-kato-polemidia": "Kato Polemidia",
                "municipality-limassol-mesa": "Mesa Geitonia",
                "municipality-larnaca-larnaca": "Larnaca",
                "municipality-larnaca-aradippou": "Aradippou",
                "municipality-larnaca-livadia": "Livadia",
                "municipality-larnaca-dromolaxia": "Dromolaxia",
                "municipality-paphos-paphos": "Paphos",
                "municipality-paphos-peyia": "Peyia",
                "municipality-paphos-polis": "Polis",
                "municipality-paphos-geroskipou": "Geroskipou",
                "municipality-famagusta-paralimni": "Paralimni",
                "municipality-famagusta-ayia": "Ayia Napa",
                "municipality-famagusta-deryneia": "Deryneia",
                "municipality-famagusta-sotira": "Sotira",
                "municipality-kyrenia-kyrenia": "Kyrenia",
                "municipality-kyrenia-lapithos": "Lapithos",
                "municipality-kyrenia-karavas": "Karavas",
                "municipality-kyrenia-dikomo": "Dikomo",
                "years-cyprus": "Years in Cyprus:",
                "nationality": "Nationality:",
                "english-level": "English Level (1–5):",
                "greek-level": "Greek Level (1–5):",
                "services-provided": "Services Provided",
                "service-cleaning": "Cleaning",
                "service-cooking": "Cooking",
                "service-babysitting": "Babysitting",
                "service-ironing": "Ironing",
                "service-gardening": "Gardening",
                "service-animal-care": "Animal Care",
                "drivers-license": "Driver’s License:",
                "cleaning-experience": "Years of Cleaning Experience:",
                "recommendations": "Recommendations Available:",
                "hourly-rate": "Expected Hourly Rate (€):",
                "monthly-rate": "Expected Monthly Rate (Full-Time, 40 hours/week, €):",
                "hourly-rate-tooltip": "Enter your expected pay per hour.",
                "monthly-rate-tooltip": "Enter your expected pay for a full-time role (40 hours/week).",
                "work-type": "Work Type:",
                "preferred-work-type": "Preferred Work Type:",
                "select-work-type": "Select work type",
                "select-years": "Select years",
                "select-nationality": "Select nationality",
                "select-level": "Select level",
                "full-time": "Full-Time",
                "part-time": "Part-Time",
                "any": "Any",
                "available-days": "Available Days:",
                "preferred-days": "Preferred Days:",
                "day-monday": "Monday",
                "day-tuesday": "Tuesday",
                "day-wednesday": "Wednesday",
                "day-thursday": "Thursday",
                "day-friday": "Friday",
                "day-saturday": "Saturday",
                "day-sunday": "Sunday",
                "time-preference": "Time Preference:",
                "preferred-time": "Preferred Time:",
                "time-morning": "Morning",
                "time-evening": "Evening",
                "time-both": "Both",
                "time-any": "Any",
                "source-language": "Language of Your Description:",
                "target-language": "Translate Description To:",
                "service-type": "Type of Service Needed:",
                "select-service": "Select a service",
                "professional-details": "Professional Details",
                "additional-details": "Additional Details",
                "rate-details": "Rate Details",
                "yes": "Yes",
                "no": "No",
                "submit-profile-button": "Submit Profile",
                "profile-title": "Your Profile",
                "profile-username": "Username:",
                "profile-email": "Email:",
                "update-profile-button": "Update Profile",
                "admin-title": "Admin Panel",
                "admin-users": "All Users",
                "find-match-title": "Find a Match in Cyprus",
                "filter-all": "All",
                "filter-professional-cleaner": "Professional Cleaners",
                "filter-client": "Clients",
                "filter-districts": "Districts and Municipalities",
                "filter-all-districts lngth": "All Districts",
                "filter-services": "Services",
                "filter-all-work-types": "All Work Types",
                "filter-days": "Available Days",
                "filter-all-times": "All Times",
                "filter-all-experience": "All Experience",
                "sort-recent": "Sort by Recent",
                "no-matches": "No matches found",
                "no-bio": "No bio available",
                "edit-button": "Edit",
                "delete-button": "Delete",
                "contact-button": "Contact",
                "send-message": "Send a message to",
                "message-sent": "Message sent to",
                "search-placeholder": "Search by name or bio...",
                "login-prompt": "Please login or register to find a match.",
                footer: "Contact Us: info@cleanconnectcyprus.com | © 2025 CleanConnect Cyprus",
                "error-required": "Please fill in all required fields.",
                "error-email": "Please enter a valid email address.",
                "error-url": "Please enter a valid URL for the profile photo.",
                "error-exists": "Username or email already exists.",
                "error-part-time-days": "Please select at least one available day for part-time work.",
                "error-municipalities": "Please select at least one municipality for each selected district."
            },
            el: {
                title: "CleanConnect Κύπρος",
                "nav-login": "Σύνδεση",
                "nav-register": "Εγγραφή",
                "nav-find-match": "Βρες Αντιστοιχία",
                "nav-admin": "Πίνακας Διαχείρισης",
                "stats-professional-cleaners": "Διαθέσιμοι Επαγγελματίες Καθαριστές στην Κύπρο",
                "stats-clients": "Πελάτες που Αναζητούν στην Κύπρο",
                "login-title": "Σύνδεση",
                "login-email": "Email:",
                "login-password": "Κωδικός:",
                "login-button": "Σύνδεση",
                "forgot-password": "Ξεχάσατε τον Κωδικό;",
                "change-password-title": "Αλλαγή Κωδικού",
                "current-password": "Τρέχων Κωδικός:",
                "new-password": "Νέος Κωδικός:",
                "change-password-button": "Αλλαγή Κωδικού",
                "change-password-link": "Αλλαγή Κωδικού",
                "register-title": "Εγγραφή στο CleanConnect Κύπρος",
                "register-username": "Όνομα Χρήστη:",
                "register-email": "Email:",
                "register-password": "Κωδικός:",
                "register-type": "Είμαι:",
                "select-role": "Επιλέξτε τον ρόλο σας",
                "role-client": "Πελάτης (Χρειάζομαι Επαγγελματία Καθαριστή, €5/μήνα)",
                "role-professional-cleaner": "Επαγγελματίας Καθαριστής (Δωρεάν)",
                "register-button": "Εγγραφή",
                "complete-profile-title": "Ολοκληρώστε το Προφίλ σας",
                "profile-name": "Πλήρες Όνομα:",
                "profile-photo": "URL Φωτογραφίας Προφίλ:",
                "profile-bio": "Σύντομο Βιογραφικό:",
                "profile-districts": "Επαρχίες και Δήμοι στην Κύπρο",
                "districts": "Επαρχίες:",
                "municipalities": "Δήμοι για {district}:",
                "district-nicosia": "Λευκωσία",
                "district-limassol": "Λεμεσός",
                "district-larnaca": "Λάρνακα",
                "district-paphos": "Πάφος",
                "district-famagusta": "Αμμόχωστος",
                "district-kyrenia": "Κερύνεια",
                "municipality-nicosia-nicosia": "Λευκωσία",
                "municipality-nicosia-strovolos": "Στρόβολος",
                "municipality-nicosia-lakatamia": "Λακατάμια",
                "municipality-nicosia-engomi": "Έγκωμη",
                "municipality-limassol-limassol": "Λεμεσός",
                "municipality-limassol-ypsonas": "Ύψωνας",
                "municipality-limassol-kato-polemidia": "Κάτω Πολεμίδια",
                "municipality-limassol-mesa": "Μέσα Γειτονιά",
                "municipality-larnaca-larnaca": "Λάρνακα",
                "municipality-larnaca-aradippou": "Αραδίππου",
                "municipality-larnaca-livadia": "Λιβάδια",
                "municipality-larnaca-dromolaxia": "Δρομολαξιά",
                "municipality-paphos-paphos": "Πάφος",
                "municipality-paphos-peyia": "Πέγεια",
                "municipality-paphos-polis": "Πόλη",
                "municipality-paphos-geroskipou": "Γεροσκήπου",
                "municipality-famagusta-paralimni": "Παραλίμνι",
                "municipality-famagusta-ayia": "Αγία Νάπα",
                "municipality-famagusta-deryneia": "Δερύνεια",
                "municipality-famagusta-sotira": "Σωτήρα",
                "municipality-kyrenia-kyrenia": "Κερύνεια",
                "municipality-kyrenia-lapithos": "Λάπηθος",
                "municipality-kyrenia-karavas": "Καραβάς",
                "municipality-kyrenia-dikomo": "Δίκωμο",
                "years-cyprus": "Χρόνια στην Κύπρο:",
                "nationality": "Εθνικότητα:",
                "english-level": "Επίπεδο Αγγλικών (1–5):",
                "greek-level": "Επίπεδο Ελληνικών (1–5):",
                "services-provided": "Υπηρεσίες που Παρέχονται",
                "service-cleaning": "Καθαρισμός",
                "service-cooking": "Μαγειρική",
                "service-babysitting": "Φύλαξη Παιδιών",
                "service-ironing": "Σιδέρωμα",
                "service-gardening": "Κηπουρική",
                "service-animal-care": "Φροντίδα Ζώων",
                "drivers-license": "Άδεια Οδήγησης:",
                "cleaning-experience": "Χρόνια Εμπειρίας Καθαρισμού:",
                "recommendations": "Διαθέσιμες Συστάσεις:",
                "hourly-rate": "Αναμενόμενος Ωριαίος Μισθός (€):",
                "monthly-rate": "Αναμενόμενος Μηνιαίος Μισθός (Πλήρης Απασχόληση, 40 ώρες/εβδομάδα, €):",
                "hourly-rate-tooltip": "Εισάγετε τον αναμενόμενο μισθό σας ανά ώρα.",
                "monthly-rate-tooltip": "Εισάγετε τον αναμενόμενο μισθό σας για πλήρη απασχόληση (40 ώρες/εβδομάδα).",
                "work-type": "Τύπος Εργασίας:",
                "preferred-work-type": "Προτιμώμενος Τύπος Εργασίας:",
                "select-work-type": "Επιλέξτε τύπο εργασίας",
                "select-years": "Επιλέξτε χρόνια",
                "select-nationality": "Επιλέξτε εθνικότητα",
                "select-level": "Επιλέξτε επίπεδο",
                "full-time": "Πλήρης Απασχόληση",
                "part-time": "Μερική Απασχόληση",
                "any": "Οποιοδήποτε",
                "available-days": "Διαθέσιμες Ημέρες:",
                "preferred-days": "Προτιμώμενες Ημέρες:",
                "day-monday": "Δευτέρα",
                "day-tuesday": "Τρίτη",
                "day-wednesday": "Τετάρτη",
                "day-thursday": "Πέμπτη",
                "day-friday": "Παρασκευή",
                "day-saturday": "Σάββατο",
                "day-sunday": "Κυριακή",
                "time-preference": "Προτιμώμενη Ώρα:",
                "preferred-time": "Προτιμώμενη Ώρα:",
                "time-morning": "Πρωί",
                "time-evening": "Απόγευμα",
                "time-both": "Και τα δύο",
                "time-any": "Οποιαδήποτε",
                "source-language": "Γλώσσα της Περιγραφής σας:",
                "target-language": "Μετάφραση της Περιγραφής σε:",
                "service-type": "Τύπος Υπηρεσίας που Χρειάζεται:",
                "select-service": "Επιλέξτε υπηρεσία",
                "professional-details": "Επαγγελματικές Λεπτομέριες",
                "additional-details": "Πρόσθετες Λεπτομέριες",
                "rate-details": "Λεπτομέριες Μισθού",
                "yes": "Ναι",
                "no": "Όχι",
                "submit-profile-button": "Υποβολή Προφίλ",
                "profile-title": "Το Προφίλ σας",
                "profile-username": "Όνομα Χρήστη:",
                "
