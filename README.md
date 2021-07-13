you should briefly describe your high-level approach: Our high level approach was to simply follow the steps outlined in the "Implementing Your Router" section of the prompt. First we evaluated each test case and dissected what kind of network topologies they created and how the networks/computer interacted with one another. The second step: Implementing Unix Domain Sockets was already accomplished for us in the starter code. We evaluated how packets were stored in the JSON format and learned how to extract and send data in the format using dump and load. Third, we implmented basic support for "update" and "data" messages. This included creating a fowarding table and storing announcements for future sending. Addtionally, when a "data" message was sent, we would forward the message to the appropriate neighbors that we looked up in our forwarding table. Lastly, we implemented support for the "dump" message. This was as simple as forwarding our routing table in the format provided to cross check with the sim to see if it was correct.

any challenges you faced

Most of the challenges we faced were conceptual. We were initally confused how the fowarding table should be stored and the relevant key and value for the map. Implementing "dump" solved a lot of these issues as we could cross reference our forwarding table with the output of "dump" and know if we correctly stored our table.

Our next issue was the format of sending the route update. We initally did not have the ASpath value as the right list. First we did not know that we had to append it onto the new packet, then we appended it the wrong way. Additonally, we had trouble figuring out what the source and dest was on the updated packet to send. Going to office hours and having a TA conceptually explain the issue and process was helpful in understanding how to update the packet.

overview of how you tested your code:

To test our code we examined the tests provided. We attempted to learn and understand what the tests were doing so we could properly cater our code accordingly. Additonally, we also ran the actual test provided on the sim.
