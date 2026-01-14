<h1>✈️ Airline Reservation System</h1>

<h2>Overview</h2>
<p>
The <strong>Airline Reservation System</strong> is a full-stack application designed to simulate a real-world airline
booking platform. The system enables customers to search for flights, make and manage reservations, while allowing
airlines to manage flight inventory and airports to display real-time arrival and departure information.
</p>

<p>
The project was built collaboratively by a small development team, following modular design principles with a focus on
<strong>data persistence, access control, and user experience</strong>.
</p>

<hr />

<h2>Key Features</h2>
<ul>
  <li>Secure customer accounts with reservation management</li>
  <li>Airline-managed flight inventory and capacity enforcement</li>
  <li>Centralized flight search and booking engine</li>
  <li>Public airport arrival and departure information displays</li>
  <li>Persistent storage across application restarts</li>
  <li>Role-based access control for customers, airline admins, and system admins</li>
</ul>

<hr />

<h2>System Architecture</h2>
<p>The application is composed of the following core components:</p>
<ul>
  <li>Customer Portal</li>
  <li>Airline Management Interface</li>
  <li>Search Engine</li>
  <li>Airport Information Displays</li>
  <li>Persistent Data Layer</li>
</ul>

<p>
Each component is logically separated to reflect real-world airline reservation workflows.
</p>

<hr />

<h2>Core Domain Entities</h2>

<h3>Customers</h3>
<ul>
  <li>Register and authenticate with password-protected accounts</li>
  <li>Search available flights and fares</li>
  <li>Make and cancel reservations</li>
  <li>View all personal reservations in a read-only dashboard</li>
  <li>Customer data is isolated and inaccessible to other users</li>
</ul>

<hr />

<h3>Airlines</h3>
<ul>
  <li>Maintain an airline-specific management interface</li>
  <li>Airline administrators can:
    <ul>
      <li>Create new flights</li>
      <li>Set fares and maximum passenger capacity</li>
      <li>Cancel existing flights</li>
    </ul>
  </li>
  <li>Customers can:
    <ul>
      <li>View airline flight listings</li>
      <li>Book and cancel reservations</li>
    </ul>
  </li>
  <li>Airline administrators have read-only access to all reservations made on their flights</li>
</ul>

<h4>Capacity Enforcement</h4>
<ul>
  <li>Each flight enforces a maximum capacity</li>
  <li>Once capacity is reached, further reservations are blocked</li>
</ul>

<h4>Flight Cancellation Handling</h4>
<ul>
  <li>When a flight is canceled, all affected customer reservations are automatically updated</li>
</ul>

<hr />

<h3>Airports</h3>
<p>
Airports provide <strong>public, real-time information displays</strong> with no authentication required.
</p>

<h4>Arrivals Screen</h4>
<ul>
  <li>Displays all arriving flights for a given airport</li>
  <li>Shows flight status:
    <ul>
      <li>On Time</li>
      <li>Cancelled</li>
    </ul>
  </li>
  <li>Automatically refreshes at regular intervals</li>
</ul>

<h4>Departures Screen</h4>
<ul>
  <li>Displays all departing flights for a given airport</li>
  <li>Shows real-time flight status</li>
  <li>Automatically refreshes to reflect airline updates</li>
</ul>

<p>
There is no airport administrator role; all airport data is read-only and public.
</p>

<hr />

<h3>Search Engine</h3>
<ul>
  <li>Search flights using relevant criteria (e.g., airline, fare, destination)</li>
  <li>Sort results by:
    <ul>
      <li>Fare</li>
      <li>Airline name</li>
    </ul>
  </li>
  <li>Clearly indicates when flights are fully booked</li>
  <li>Allows customers to make reservations directly from search results</li>
</ul>

<h4>Search Engine Administration</h4>
<ul>
  <li>Admins can view all reservations made <strong>through the search engine only</strong></li>
  <li>Airline and customer reservations made outside the search engine are not visible</li>
  <li>Access is read-only and restricted to system administrators</li>
</ul>

<hr />

<h2>User Interface Requirements</h2>
<ul>
  <li>Multi-screen graphical user interface (GUI)</li>
  <li>Separate views tailored to:
    <ul>
      <li>Customers</li>
      <li>Airline administrators</li>
      <li>System administrators</li>
      <li>Public airport displays</li>
    </ul>
  </li>
  <li>Clear role-based access enforcement across all views</li>
</ul>

<hr />

<h2>Data Persistence</h2>
<ul>
  <li>All application data persists across restarts</li>
  <li>Data storage implemented using:
    <ul>
      <li>Database-backed persistence <strong>or</strong></li>
      <li>Structured file-based storage</li>
    </ul>
  </li>
  <li>The persistence strategy is abstracted from the UI layer</li>
</ul>

<hr />

<h2>Technology Stack</h2>
<ul>
  <li><strong>Backend:</strong> Java (architecture-neutral, extensible design)</li>
  <li><strong>Frontend:</strong> GUI-based multi-screen interface</li>
  <li><strong>Persistence:</strong> Database or file-based storage</li>
  <li><strong>Security:</strong> Authentication and authorization enforced per role</li>
</ul>

<hr />

<h2>Engineering Focus</h2>
<ul>
  <li>Clean separation of concerns</li>
  <li>Role-based access control</li>
  <li>Data consistency and integrity</li>
  <li>Real-world business rules (capacity limits, cancellations)</li>
  <li>Collaborative development practices</li>
</ul>

<hr />

<h2>Future Enhancements</h2>
<ul>
  <li>Payment processing integration</li>
  <li>Notification system for flight changes</li>
  <li>REST API exposure for mobile clients</li>
  <li>Audit logging and reporting</li>
  <li>Scalable microservices architecture</li>
</ul>
