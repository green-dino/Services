# Contact Us
Contact us via e-mail by submitting this form.
All fields are required 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Email Communication</title>
</head>
<body>
    <h1>Send us an e-mail</h1>
    <form id="contactForm">
        <label for="clientName">Name:</label>
        <input type="text" id="clientName" name="clientName" required><br><br>
        
        <label for="clientEmail">Email:</label>
        <input type="email" id="clientEmail" name="clientEmail" required><br><br>
        
        <label for="clientPhone">Phone Number:</label>
        <input type="tel" id="clientPhone" name="clientPhone" required><br><br>
        
        <label for="clientMessage">Message:</label><br>
        <textarea id="clientMessage" name="clientMessage" rows="4" cols="50" required></textarea><br><br>
        
        <button type="button" onclick="sendEmail()">Send Email</button>
    </form>

    <p id="feedback" style="color: green; display: none;">Preparing your email...</p>

    <script>
        function sendEmail() {
            const feedback = document.getElementById('feedback');
            feedback.style.display = 'block';
            
            const name = document.getElementById('clientName').value;
            const email = document.getElementById('clientEmail').value;
            const phone = document.getElementById('clientPhone').value;
            const message = document.getElementById('clientMessage').value;
            
            const subject = encodeURIComponent(`Information Request from ${name}`);
            const body = encodeURIComponent(`Name: ${name}\nEmail: ${email}\nPhone Number: ${phone}\n\nMessage:\n${message}`);
            
            const mailtoLink = `mailto:rye@grcand.me?subject=${subject}&body=${body}`;
            window.location.href = mailtoLink;
            
            setTimeout(() => {
                feedback.style.display = 'none';
            }, 3000);
        }
    </script>
</body>
</html>
