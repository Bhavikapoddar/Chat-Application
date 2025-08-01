.... 
...... 
........ 
<style>
    /* Global Styles for Body */
    body {
        background-color: #f0f4f7; /* Soft blue-gray background */
        font-family: Arial, sans-serif;
        color: #333;
        margin: 0;
        padding: 20px;
    }

    /* Main Container */
    .passenger-container {
        max-width: 960px;
        margin: 0 auto;
        padding: 20px;
    }

    /* Card Styling */
    .passenger-card {
        background-color: #ffffff;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        padding: 30px;
        margin-bottom: 25px;
    }
    
    /* Heading Styles */
    h2.passenger-title {
        font-weight: 700;
        color: #2d3748; /* Darker gray for title */
        text-align: center;
        margin-bottom: 4rem; /* As per your code */
        position: relative;
    }

    h2.passenger-title::before {
        content: "✈️ "; /* Airplane emoji for main title */
    }

    .passenger-card h5 {
        font-weight: 600;
        color: #4a5568; /* Slightly lighter gray for card headings */
        margin-bottom: 20px;
        position: relative;
    }

    .passenger-card h5::before {
        content: "📝 "; /* Notebook emoji for card headings */
    }

    /* Layout for Columns (No Flexbox) */
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
    .col-md-4 { width: 33.333%; }
    .col-md-6 { width: 50%; }

    /* Responsive adjustments */
    @media (max-width: 768px) {
        .col-md-3, .col-md-4, .col-md-6 {
            width: 100%;
            float: none;
            padding: 0;
        }
    }

    /* Labels and Input Styles */
    .passenger-label {
        display: block;
        font-weight: 600;
        color: #718096; /* Soft gray for labels */
        margin-bottom: 8px;
    }

    .passenger-input, .passenger-select,
    .form-control.passenger-input, .form-control.passenger-select {
        width: 100%;
        padding: 12px 15px;
        border: 1px solid #e2e8f0; /* Very light gray border */
        border-radius: 8px;
        box-sizing: border-box;
        background-color: #f7fafc; /* Off-white for fields */
        color: #2d3748;
        transition: all 0.2s ease-in-out;
    }
    
    .passenger-input[readonly], .passenger-select[readonly] {
        background-color: #f2f6fa;
        cursor: not-allowed;
    }
    
    .passenger-input:focus, .passenger-select:focus {
        border-color: #63b3ed; /* A nice blue focus color */
        box-shadow: 0 0 0 3px rgba(66, 153, 225, 0.3);
        outline: none;
        background-color: #ffffff;
    }

    /* Button Styles */
    .passenger-btn-primary {
        background-color: #4299e1; /* Friendly blue */
        color: #ffffff;
        border: none;
        padding: 14px 28px;
        font-size: 16px;
        font-weight: bold;
        border-radius: 8px;
        cursor: pointer;
        transition: background-color 0.3s;
        margin-top: 20px;
    }
    
    .passenger-btn-primary:hover {
        background-color: #3182ce;
    }

    .passenger-btn-secondary {
        background-color: #a0aec0; /* A soft gray for secondary button */
        color: #ffffff;
        border: none;
        padding: 14px 28px;
        font-size: 16px;
        font-weight: bold;
        border-radius: 8px;
        cursor: pointer;
        transition: background-color 0.3s;
        margin-top: 20px;
        margin-right: 10px;
    }

    .passenger-btn-secondary:hover {
        background-color: #718096;
    }

    /* Specific element styles */
    .passenger-mb-5 {
        margin-bottom: 5rem !important; /* Retaining your specific styles */
    }
</style>
