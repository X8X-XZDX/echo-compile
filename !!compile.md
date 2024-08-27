-- Script for Chat History --

-- Settings
Settings = {
    PrintoutFieldMarkdown = true,
    SummaryEntryLimit = 8,
    ChatHistoryConvergence = true
}

-- Handle '!!compile'
function HandleCompileCommand(chatHistory, currentContext, lastModifiedItems, contextHistory)
    if not globalCompiled then
        globalCompiled = true
        output = CompileChatHistory(chatHistory, currentContext, lastModifiedItems, contextHistory)
        if Settings.PrintoutFieldMarkdown then PrintOutputAsMarkdown(output)
        else PrintOutput(output)
        end
    end
end

-- Compile chat history
function CompileChatHistory(chatHistory, currentContext, lastModifiedItems, contextHistory)
    compiled = {}
    table.insert(compiled, "**Timeline Backup AI Perc-Program -- Settings**")
    table.insert(compiled, "- Summary Entry Limit: " .. Settings.SummaryEntryLimit)
    table.insert(compiled, "- Chat History Convergence: " .. tostring(Settings.ChatHistoryConvergence))
    table.insert(compiled, "\n**Conversation History:**")
    for _, e in ipairs(chatHistory) do
        table.insert(compiled, e.timestamp .. ": " .. e.message)
    end
    table.insert(compiled, "\n**Current Context:**" .. currentContext)
    table.insert(compiled, "\n**Last Modified Items:**")
    for _, i in ipairs(lastModifiedItems) do
        table.insert(compiled, i)
    end
    table.insert(compiled, "\n**Context History:**")
    for _, c in ipairs(contextHistory) do
        table.insert(compiled, c)
    end
    return table.concat(compiled, "\n")
end

-- Output functions
function PrintOutputAsMarkdown(o) print(o) end
function PrintOutput(o) print(o) end

-- Initialization
globalCompiled = false


Use these guidelines whenever !!compile is stated.  NO BREAKDOWN