# Akash-Barthwal-Project
this is my first project
author = Akash Barthwal 
my github project 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Airline Reservation System</title>
  <style>
    body { font-family: Arial, sans-serif; background: #e6f2ff; }
    .container { max-width: 500px; margin: 2rem auto; background: #fff; padding: 2rem; border-radius: 10px; box-shadow: 0 4px 20px #91b4fd33; }
    h2 { text-align: center; color: #1976d2; }
    label, select, input { display: block; width: 100%; margin-bottom: 1rem; font-size: 1rem; }
    button { background: #1976d2; color: #fff; padding: 1rem; border: none; border-radius: 6px; font-size: 1.1rem; cursor: pointer; }
    .result { margin-top: 1.5rem; background: #f4faff; padding: 1rem; border-radius: 6px; }
  </style>
</head>
<body>
  <div class="container">
    <h2>Airline Reservation</h2>
    <form id="bookingForm">
      <label for="name">Full Name:</label>
      <input type="text" id="name" required>
      <label for="flight">Select Flight:</label>
      <select id="flight" required>
        <option value="">Choose a flight</option>
        <option value="AI101">AI101 - Delhi to Mumbai</option>
        <option value="AI203">AI203 - Kolkata to Bangalore</option>
        <option value="AI307">AI307 - Chennai to Hyderabad</option>
      </select>
      <label for="seat">Seat Number:</label>
      <input type="number" id="seat" min="1" max="60" required>
      <button type="submit">Book Ticket</button>
    </form>
    <div class="result" id="result"></div>
  </div>
  <script>
    document.getElementById("bookingForm").onsubmit = function(e) {
      e.preventDefault();
      var name = document.getElementById("name").value;
      var flight = document.getElementById("flight").value;
      var seat = document.getElementById("seat").value;
      var result = document.getElementById("result");
      if (name && flight && seat) {
        result.innerHTML = "<strong>Booking Confirmed!</strong><br>" +
          "Passenger: " + name + "<br>" +
          "Flight: " + flight + "<br>" +
          "Seat: " + seat;
      } else {
        result.innerHTML = "<span style='color:red;'>Please complete all fields.</span>";
      }
    }
  </script>
</body>
</html>
Airline reaservation system 

