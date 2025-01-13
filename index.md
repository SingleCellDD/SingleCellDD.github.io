SingleCellDD is a community of scientists in Dresden working on Single-Cell Biology. We organise a monthly discussion round and invite speakers for talks in our single cell seminar series. _Everybody is welcome to join!_

# Mailing List 

Announcements are spread via our [mailing list](https://mailman.zih.tu-dresden.de/groups/listinfo/singlecell), feel free to join!

# Chat room

Outside of meetings, discussions continue in our [Matrix room](https://matrix.to/#/#singlecelldd:tu-dresden.de).

TU Dresden members can join with their ZIH login [here](https://matrix.tu-dresden.de/#/#SingleCellDD:tu-dresden.de). Otherwise, you can create an account [here](https://app.element.io/#/login).

# Meeting dates

We meet on a Wednesday every 4 weeks at 13:00. These are the dates planned for 2024 (location in paranthesis). 

<div id="events-list">
  <!-- Events will be dynamically inserted here -->
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.3.0/papaparse.min.js"></script>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    const currentDate = new Date();

    // Function to display events
    function displayEvents(events) {
      const eventsList = document.getElementById("events-list");
      events.forEach(event => {
        const eventDate = new Date(event.Date);
        if (eventDate >= currentDate) {
          const eventElement = document.createElement("div");
          eventElement.classList.add("event");
          eventElement.innerHTML = `On ${event.Date} at ${event.Location}`;
          eventsList.appendChild(eventElement);
        }
      });
    }

    // Fetch and parse the CSV file
    Papa.parse("assets/events.csv", {
      download: true,
      header: true,
      dynamicTyping: true,
      complete: function(results) {
        displayEvents(results.data);
      }
    });
  });
</script>

<!-- - Jan 15, 2025 (CRTD, SR4, 3.310)
- Feb 12, 2025 (CRTD, SR3, 3.310)
- Mar 12, 2025 (CRTD, SR3, 3.310)
- Apr 9, 2025 (CRTD, SR3, 3.310)
- May 7, 2025 (CRTD, SR3, 3.310)
- Jun 4, 2025 (CRTD, SR3, 3.310)
- Jul 2, 2025 (CRTD, SR3, 3.310)
- Jul 30, 2025 (CRTD, SR3, 3.310)
- Aug 27, 2025 (CRTD, SR3, 3.310)
- Sep 24, 2025 (CSBD, Ground Floor SR)
- Oct 22, 2025 (CRTD, SR3, 3.310)
- Nov 19, 2025 (CRTD, SR3, 3.310)
- Dec 17, 2025 (CRTD, SR3, 3.310) -->


# Organisers

Ulrike Friedrich (Dresden-concept Genome Center)  
[Fabian Rost](https://orcid.org/0000-0001-6466-2589) (MPI-CBG)

Contact us, if you have any questions.
