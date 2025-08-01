..... 
.... 
...
/* Global Styles for Body */
body {
    background: linear-gradient(to right, #e0ecf8, #f8fbff); /* Soft blue gradient */
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #1a202c;
    margin: 0;
    padding: 20px;
    background-attachment: fixed;
    background-size: cover;
}

/* Main Container */
.passenger-container {
    max-width: 960px;
    margin: 0 auto;
    padding: 30px;
    background: rgba(255, 255, 255, 0.7);
    border-radius: 20px;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(10px);
}

/* Card Styling */
.passenger-card {
    background-color: #ffffffd9;
    border-radius: 16px;
    box-shadow: 0 6px 18px rgba(0, 0, 0, 0.08);
    padding: 35px;
    margin-bottom: 30px;
    transition: transform 0.3s;
}

.passenger-card:hover {
    transform: scale(1.01);
}

/* Heading Styles */
h2.passenger-title {
    font-weight: 800;
    color: #2a4365;
    text-align: center;
    margin-bottom: 3.5rem;
    font-size: 2rem;
    letter-spacing: 1px;
    position: relative;
}

h2.passenger-title::before {
    content: "✈️ ";
    font-size: 1.5rem;
}

.passenger-card h5 {
    font-weight: 700;
    color: #4a5568;
    font-size: 1.2rem;
    margin-bottom: 18px;
}

.passenger-card h5::before {
    content: "📝 ";
}

/* Column Layout */
.row::after {
    content: "";
    display: table;
    clear: both;
}

.col-md-3, .col-md-4, .col-md-6 {
    float: left;
    padding: 0 15px;
    box-sizing: border-box;
    margin-bottom: 20px;
}

.col-md-3 { width: 25%; }
.col-md-4 { width: 33.3333%; }
.col-md-6 { width: 50%; }

/* Responsive for Mobile */
@media (max-width: 768px) {
    .col-md-3, .col-md-4, .col-md-6 {
        width: 100%;
        float: none;
        padding: 0;
    }
}

/* Labels and Inputs */
.passenger-label {
    display: block;
    font-weight: 600;
    color: #718096;
    margin-bottom: 8px;
}

.passenger-input, .passenger-select {
    width: 100%;
    padding: 14px 16px;
    border: 1px solid #cbd5e0;
    border-radius: 10px;
    background-color: #f7fafc;
    color: #2d3748;
    transition: all 0.3s ease-in-out;
    font-size: 1rem;
    box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.05);
}

.passenger-input:focus, .passenger-select:focus {
    border-color: #4299e1;
    box-shadow: 0 0 0 4px rgba(66, 153, 225, 0.3);
    background-color: #fff;
    outline: none;
}

.passenger-input[readonly], .passenger-select[readonly] {
    background-color: #edf2f7;
    cursor: not-allowed;
}

/* Buttons */
.passenger-btn-primary {
    background: linear-gradient(to right, #4299e1, #3182ce);
    color: white;
    border: none;
    padding: 14px 30px;
    font-size: 16px;
    font-weight: 700;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.3s ease;
}

.passenger-btn-primary:hover {
    background: linear-gradient(to right, #2b6cb0, #2c5282);
}

.passenger-btn-secondary {
    background: #a0aec0;
    color: white;
    border: none;
    padding: 14px 30px;
    font-size: 16px;
    font-weight: 700;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.3s ease;
    margin-right: 10px;
}

.passenger-btn-secondary:hover {
    background-color: #718096;
}

/* Spacing */
.passenger-mb-5 {
    margin-bottom: 5rem !important;
}
