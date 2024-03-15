---

---

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Event Display</title>
<style>
  .event-container {
    display: flex;
    flex-wrap: wrap;
    padding: 20px;
    justify-content: space-between;
  }
  .event {
    display: flex;
    margin-bottom: 20px;
    border: 1px solid #ddd;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  .event > div {
    padding: 20px;
  }
  .year, .text-info {
    flex: 1;
  }
  .photo {
    flex: 2;
  }
  .photo img {
    width: 100%;
    height: auto;
  }
</style>
</head>
<body>

<div class="event-container">
  <div class="event">
    <div class="year">
      <h3>2022</h3>
    </div>
    <div class="text-info">
      <p>This event marked a significant milestone in our journey.</p>
    </div>
    <div class="photo">
      <img src="event-photo1.jpg" alt="Event Photo">
    </div>
  </div>

  <div class="event">
    <div class="year">
      <h3>2023</h3>
    </div>
    <div class="text-info">
      <p>An unforgettable experience that brought us all closer together.</p>
    </div>
    <div class="photo">
      <img src="tn.png" alt="Event Photo">
    </div>
  </div>

  <!-- Add more events here -->
</div>

</body>
</html>
