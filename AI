import java.util.*;

public class SimpleChatBot {
    private static final Map<String, String> knowledgeBase = new HashMap<>();

    static {
        knowledgeBase.put("hi", "Hello! How can I help you today?");
        knowledgeBase.put("hello", "Hi there! Need any assistance?");
        knowledgeBase.put("how are you", "I'm just a bot, but I'm doing great!");
        knowledgeBase.put("what is your name", "I'm ChatBot, your virtual assistant.");
        knowledgeBase.put("bye", "Goodbye! Have a nice day.");
        knowledgeBase.put("thank you", "You're welcome!");
        knowledgeBase.put("help", "I can help with basic questions. Ask me anything!");
        knowledgeBase.put("what is ai", "AI stands for Artificial Intelligence. It enables machines to mimic human intelligence.");
        knowledgeBase.put("who made you", "I was created by a Java developer!");
    }

    public static String getResponse(String userInput) {
        userInput = userInput.toLowerCase().trim();

        for (String question : knowledgeBase.keySet()) {
            if (userInput.contains(question)) {
                return knowledgeBase.get(question);
            }
        }
        return "I'm not sure how to respond to that. Try asking something else.";
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Welcome to AI ChatBot! Type 'exit' to quit.");
        
        while (true) {
            System.out.print("You: ");
            String input = scanner.nextLine();
            if (input.equalsIgnoreCase("exit")) break;

            String response = getResponse(input);
            System.out.println("Bot: " + response);
        }

        scanner.close();
        System.out.println("Chat ended.");
    }
}
