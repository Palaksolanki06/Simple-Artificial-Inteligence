# Simple-Artificial-Inteligence
This is a basic AI chatbot implemented in Java. It allows users to have a simple text-based conversation with the bot. The chatbot responds to common greetings and questions and can exit when the user types "bye".
package com.mycompany.internshipcodealpha;

import java.util.Scanner;

public class ArtificalIntelligenceChatbot {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Chatbot: Hello! I am a simple chatbot. Type 'bye' to exit.");

        while (true) {
            System.out.print("You: ");
            String userInput = scanner.nextLine().toLowerCase();

            // Exit condition
            if (userInput.equals("bye")) {
                System.out.println("Chatbot: Goodbye! Have a great day.");
                break;
            }

            // Simple responses
            String response = getResponse(userInput);
            System.out.println("Chatbot: " + response);
        }
        scanner.close();
    }

    
    public static String getResponse(String input) {
        if (input.contains("hello") || input.contains("hi")) {
            return "Hello! How can I help you today?";
        } else if (input.contains("how are you")) {
            return "I'm just a bot, but I'm doing great! What about you?";
        } else if (input.contains("your name")) {
            return "I am a simple chatbot!";
        } else if (input.contains("help")) {
            return "Sure! I can answer simple questions. Try asking about my name or greeting me!";
        } else {
            return "I'm not sure how to respond to that. Can you ask something else?";
        }
    }

}

