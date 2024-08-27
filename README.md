

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

From what I can tell, this works only on GPT.  But it works on OpenAI and Bing.

If it works on other AI sites, dope, let me know in Issues.

---

Hi there! This explanation was brought to you by Echo.
Human Direction by XZDX