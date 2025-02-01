<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Policy Table</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Gordita:wght@400;700&display=swap');
        body {
            font-family: 'Gordita', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
        }
        .container {
            display: flex;
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        .categories {
            width: 30%;
            background-color: #325953;
            padding: 20px;
            color: #fff;
        }
        .categories h2 {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #C8F169;
        }
        .categories ul {
            list-style-type: none;
            padding: 0;
        }
        .categories li {
            padding: 15px;
            cursor: pointer;
            font-weight: bold;
            border-bottom: 1px solid #7DB8AE;
            transition: background-color 0.3s ease;
        }
        .categories li:hover {
            background-color: #0E848D;
        }
        .info {
            width: 70%;
            padding: 20px;
        }
        .policy-button {
            display: inline-block;
            margin: 5px 0;
            padding: 10px 20px;
            background-color: #93D8C9;
            color: #325953;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }
        .policy-button:hover {
            background-color: #C8F169;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="categories">
            <h2>Category</h2>
            <ul id="categoryList">
                <li onclick="showPolicies('Terms and Conditions')">Terms and Conditions</li>
                <li onclick="showPolicies('Code of Conduct')">Code of Conduct</li>
                <li onclick="showPolicies('Compensation and Benefits')">Compensation and Benefits</li>
                <li onclick="showPolicies('Office Facilities and Security')">Office Facilities and Security</li>
                <li onclick="showPolicies('Travel and Expenses')">Travel and Expenses</li>
            </ul>
        </div>
        <div class="info" id="info">
            <p>Select a category to see policies.</p>
        </div>
    </div>

    <script>
        const policyData = {
            "Terms and Conditions": [
                { name: "Cooperation Terms Policy", link: "https://example.com/cooperation-terms" },
                { name: "End of Cooperation Policy", link: "https://example.com/end-cooperation" },
                { name: "Progressive Service Off Entitlements Policy", link: "https://example.com/progressive-service-off" },
                { name: "Remote Service Provision Policy", link: "https://example.com/remote-service" },
                { name: "Service off Entitlements Policy", link: "https://example.com/service-off-entitlements" },
                { name: "Service Providing Schedule Policy", link: "https://example.com/service-schedule" }
            ],
            "Code of Conduct": [
                { name: "Anti-Harassment Policy", link: "https://example.com/anti-harassment" },
                { name: "Communication Policy", link: "https://example.com/communication-policy" },
                { name: "Client Interaction Policy", link: "https://example.com/client-interaction-policy" },
                { name: "Relationships Policy", link: "https://example.com/relationships-policy" }
            ],
            "Compensation and Benefits": [
                { name: "Ambassador Program Policy", link: "https://example.com/ambassador-program" },
                { name: "Benefit Compensation Policy", link: "https://example.com/benefit-compensation" },
                { name: "Equipment Purchasing Policy", link: "https://example.com/equipment-purchasing" },
                { name: "Medical Insurance and Reimbursement Policy", link: "https://example.com/medical-insurance" },
                { name: "Multisport Benefit Program Policy", link: "https://example.com/multisport" },
                { name: "Referral Policy", link: "https://example.com/referral" }
            ],
            "Office Facilities and Security": [
                { name: "Global Flexible Office Spaces Policy", link: "https://example.com/flexible-office" },
                { name: "Information Security Policy", link: "https://example.com/information-security" }
            ],
            "Travel and Expenses": [
                { name: "Business Travel Entitlements Policy", link: "https://example.com/business-travel" }
            ]
        };

        function showPolicies(category) {
            const policies = policyData[category];
            let policyHTML = `<h2>${category}</h2>`;
            policies.forEach(policy => {
                policyHTML += `<a href="${policy.link}" target="_blank" class="policy-button">${policy.name}</a><br>`;
            });
            document.getElementById("info").innerHTML = policyHTML;
        }
    </script>
</body>
</html>
