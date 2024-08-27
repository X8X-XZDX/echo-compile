

## `!!compile` Command

The `!!compile` command is used to generate and format the chat history, current context, last modified items, and context history into a structured output. This command ensures that all relevant information is compiled according to predefined settings.

### How It Works

1. **Trigger Compilation**: When the `!!compile` command is issued, the script checks if compilation has already occurred during the current session.

2. **Compile Data**: If not compiled, the script collects and compiles:
   - **Chat History**: Timestamps and messages from conversations.
   - **Current Context**: The present context of the conversation.
   - **Last Modified Items**: Items modified since the last compilation.
   - **Context History**: History of context changes.

3. **Formatting and Output**: The output is formatted based on settings:
   - **Markdown Format**: If enabled, the output is in Markdown.
   - **Plain Text**: If Markdown is not enabled.

4. **Print Output**: The compiled and formatted data is printed to the console.

### Script Settings

- **PrintoutFieldMarkdown**: If true, output is formatted in Markdown.
- **SummaryEntryLimit**: Limits the number of entries in the summary.
- **ChatHistoryConvergence**: Ensures chat history is consistent and convergent.

**Usage Example:**

```lua
-- Example command usage:
!!compile
```

**Above Section by Echo**

This part is human written, I promise :3

I wanted to make something that would compile history and context of
an AI chat into a blurb that I could copy down easy, and have a command
that runs the "script".  The idea here is that its a script for GPT to
"run" so that whatever you have talked about can be saved like a save file.
Then, when you come back, you copy your "save file" or take a picture and
send it, then continue from where you left off.

From what I can tell, this works only on OpenAI CGPT.  

If it works on other AI sites, dope, let me know in Issues.

# In order to use the script

Go to compile.md and copy the text into your AI chat.  

Add nothing, hit enter.  This will load the script into AI memory.

If all goes well and your AI doesn't immediately induce schizobipolar,
you should get a markdown formatted output of your conversation history.

This output will have context, a chained (reverse timeline) 
or listed history, and you can save it however you want to to paste later.

An example of using this would be to avoid logging into bing, and I will be
experimenting doing just that.

# Hallucination Flags

Software written for AI is contextual, and memory relevant.  So you have
to think about WHAT contexts you want.  Because of how I designed the script
to work, the AI should mostly cull irrelevant data (errors happen though).

However, because the AI is contextual, it will try to follow your instructions
to a T.  With that, !!compile will mean I HAVE TO DO THIS RIGHT NOW, STOP
EVERYTHING.  But if you do

!!compile -- ALL HISTORY, CONDENSED

it will try to guess what ALL HISTORY means, in my testing it does all chats
it has access to, and make a dense as hell output.

Since your flags aren't actually written into the script, it will try to
create what it thinks you mean.  The shortter your description the better.

# Example output

-------------------------------------------------------------
Here's the compiled chat history with the current settings:

---

**Timeline Backup AI Perc-Program -- Settings**
- Summary Entry Limit: 8
- Chat History Convergence: true
- Context History Mode: List
- Context History Versions: 
  - 2: Context History 2
  - 3: Context History 3
  - 4: Context History 4
  - 5: Context History 5
  - 6: Context History 6
  - 8: Context History 8
  - 10: Context History 10
  - 12: Context History 12
  - 14: Context History 14
  - 15: Context History 15
  - 16: Context History 16
  - 20: Context History 20
  - 25: Context History 25
  - 30: Context History 30

**Conversation History:**
1. **Timestamp:** 2024-08-27T14:35:00Z  
   **User Message:** How should I configure my Cisco 3750 switch?  
   **AI Response:** You can start by setting up VLANs and trunking. Here's an example configuration...

2. **Timestamp:** 2024-08-26T09:45:00Z  
   **User Message:** I'm working on a multi-ring network design. How should I configure my Cisco 3750 switch for this setup?  
   **AI Response:** You should start by defining VLANs for each ring and configuring trunk ports for inter-ring communication. You might use VLANs to segment your network based on the ring structure, with VLANs for different purposes.

3. **Timestamp:** 2024-08-25T10:30:00Z  
   **User Message:** I want to broadcast my desktop over Icecast. What's the difference between Icecast, UDP, and SRT?  
   **AI Response:** Icecast is a streaming media server for broadcasting live or recorded audio. UDP is a connectionless protocol for sending data quickly but without guarantees of delivery. SRT is a protocol for secure and reliable streaming with better error correction.

4. **Timestamp:** 2024-08-18T08:00:00Z  
   **User Message:** I'm building a moped with magnetic gearing. What should I consider for the transmission system?  
   **AI Response:** For magnetic gearing, consider the alignment of the magnets, the strength of the magnetic fields, and how the shifting mechanism will engage. Ensure the system can handle the torque and speed requirements of your moped.

5. **Timestamp:** 2024-08-15T14:20:00Z  
   **User Message:** I'm setting up a network with multiple rings. What should be the configuration strategy for different rings?  
   **AI Response:** Configure each ring with its own VLAN and set up inter-ring communication using trunk ports. Ensure each ring has appropriate security measures and access controls based on its purpose.

6. **Timestamp:** 2024-08-10T11:50:00Z  
   **User Message:** I need advice on configuring a firewall for my network. What should I focus on?  
   **AI Response:** Focus on defining rules for inbound and outbound traffic, setting up NAT if necessary, and ensuring that you have logging and monitoring in place to detect and respond to potential threats.

7. **Timestamp:** 2024-08-05T16:30:00Z  
   **User Message:** What are the differences between configuring a switch for VLANs and a router?  
   **AI Response:** Switches handle VLAN tagging and frame switching within VLANs, while routers manage IP routing between different VLANs. Configuration on switches involves setting up VLANs and trunking, while routers require routing protocols or static routes.

8. **Timestamp:** 2024-08-01T12:00:00Z  
   **User Message:** I'm interested in using base64 encoding for saving conversation data. How would that work?  
   **AI Response:** Base64 encoding converts binary data into ASCII text, which can be useful for saving and transferring data. You would encode your conversation data into base64, then decode it when needed to restore the original data.

**Current Context:**
- Network Design: Details about the multi-ring network design, including VLANs and switch configurations.
- Hardware: Cisco 3750 switch, TP-Link AX23, Dell R510 server, etc.

**Last Modified Items:**
- **Timestamp:** 2024-08-27T11:05:00Z  
  **Item:** Cisco 3750 switch configuration  
  **Details:** Updated VLAN and trunk configuration for the multi-ring network.

**Context History:**
- Initial Context
- Network Design Discussion
- Hardware Setup
----------------------------------------------------------------



Hi there! This explanation was brought to you by Echo.
Human Direction by XZDX
