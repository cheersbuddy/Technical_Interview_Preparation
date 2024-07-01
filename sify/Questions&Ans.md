
Sure! Here are the answers along with explanations and examples where applicable:

1. **Which type of Ethernet framing is used for TCP/IP based networks?**
   - **Answer:** Ethernet II (or DIX Ethernet).
   - **Explanation:** Ethernet II framing is commonly used for TCP/IP based networks. It includes a type field to indicate the higher-level protocol being used (e.g., IPv4 or IPv6). This makes it different from IEEE 802.3, which originally didn't include this type field.
   - **Example:** When a device sends a packet over an Ethernet network, it typically uses Ethernet II framing, which allows the network layer to recognize the protocol (such as IPv4) being used.

2. **Which is the layer seven of OSI reference model?**
   - **Answer:** Application Layer.
   - **Explanation:** The Application Layer is the topmost layer of the OSI model and provides services directly to the user's applications. It enables communication between software applications and lower layers of the network.
   - **Example:** Web browsers and email clients operate at the Application Layer, using protocols like HTTP and SMTP.

3. **Which protocol uses both TCP and UDP?**
   - **Answer:** DNS (Domain Name System).
   - **Explanation:** DNS uses UDP for most of its queries because it is faster and requires less overhead. However, for tasks requiring reliability, such as zone transfers, DNS uses TCP.
   - **Example:** When you type a URL into your browser, a DNS query is typically sent using UDP. If the response is too large for a single UDP packet, TCP is used instead.

4. **Which protocol uses a three-way handshake before establishing a connection?**
   - **Answer:** TCP (Transmission Control Protocol).
   - **Explanation:** TCP uses a three-way handshake (SYN, SYN-ACK, ACK) to establish a reliable connection between two hosts.
   - **Example:** When you connect to a website, your computer and the web server perform a three-way handshake to establish a TCP connection before data can be exchanged.

5. **Which port number does HTTP use for communication?**
   - **Answer:** Port 80.
   - **Explanation:** HTTP typically uses port 80 for communication. Secure HTTP (HTTPS) uses port 443.
   - **Example:** When you access a website using HTTP, your browser communicates with the web server on port 80.

6. **What is the average waiting time if the processes follow the first come first serve scheduling algorithm?**
   - **Answer:** 18.75 seconds.
   - **Explanation:** First Come First Serve (FCFS) scheduling means processes are executed in the order they arrive. The waiting time is calculated as:
     - P4 (0), P2 (9), P3 (16), P1 (37)
     - Average Waiting Time = (0 + 9 + 16 + 37) / 4 = 62 / 4 = 15.5 seconds.
   - **Example:** This method is simple but can lead to longer waiting times for processes that arrive later (convoy effect).

7. **What is the length of the train moving at 80 km/h?**
   - **Answer:** 230 meters.
   - **Explanation:** The relative speed of the two trains = 120 km/h + 80 km/h = 200 km/h. Convert speed to meters per second: 200 km/h = 200 * 1000 / 3600 = 55.56 m/s. Time = 9 seconds.
     - Distance covered in 9 seconds = 55.56 * 9 = 500 meters.
     - Length of the second train = 500 meters - 270 meters = 230 meters.
   - **Example:** This calculation is based on the principle of relative motion, used in physics and engineering.

8. **What is the expected number of vegetarians if two people are selected at random?**
   - **Answer:** 0.8.
   - **Explanation:** The probability of selecting a vegetarian in one draw = 20/50 = 0.4. For two draws, the expected number is 2 * 0.4 = 0.8.
   - **Example:** This type of probability calculation is used in statistics for predicting outcomes in random sampling.

9. **What is the amount paid after discount and tax on an item priced at 6650?**
   - **Answer:** 6911.30.
   - **Explanation:** The amount after a 6% discount = 6650 - (0.06 * 6650) = 6650 - 399 = 6251. Then, add 10% tax: 6251 + (0.10 * 6251) = 6251 + 625.10 = 6911.10.
   - **Example:** This calculation is used in retail for determining final prices after discounts and taxes.

10. **Which component can be injected as a dependency in AngularJS?**
    - **Answer:** Services, Factories, and Values.
    - **Explanation:** In AngularJS, dependencies such as services, factories, and values can be injected into controllers, services, or other AngularJS components using dependency injection.
    - **Example:** When creating a service in AngularJS, it can be injected into a controller to share data or functionality.

Understanding these concepts with examples will help demonstrate practical knowledge and application during an interview.
