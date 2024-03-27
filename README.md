# -AI-
エモーショナルヘルスは、感情認識AIを活用して、ユーザーの感情状態を継続的にモニタリングし、ストレス管理やメンタルヘルスのアドバイスを提供します。
import random

# A simple emotion recognition function based on keywords. In a real scenario, this would use NLP or an AI model.
def detect_emotion(text):
    text = text.lower()
    if any(word in text for word in ["happy", "joy", "excited"]):
        return "happy"
    elif any(word in text for word in ["sad", "depressed", "unhappy", "gloomy"]):
        return "sad"
    elif any(word in text for word in ["angry", "mad", "furious", "irritated"]):
        return "angry"
    elif any(word in text for word in ["anxious", "nervous", "worried"]):
        return "anxious"
    else:
        return "neutral"

# A simple advice system based on the detected emotion.
def provide_advice(emotion):
    advice = {
        "happy": "It's great to see you happy! Remember what made you feel this way for tougher days.",
        "sad": "It's okay to feel sad. Consider talking to a friend or writing down your feelings.",
        "angry": "Take a deep breath. Try to identify why you feel this way and express it calmly.",
        "anxious": "Anxiety can be overwhelming. Focus on slow, deep breaths and tackle tasks one at a time.",
        "neutral": "Maintaining a balanced emotional state is key. Regular exercise can help improve your mood."
    }
    return advice[emotion]

# Main function to simulate user interaction
def main():
    print("Welcome to Emotional Health Support. Please tell me how you're feeling today.")
    user_input = input("Your feelings: ")
    emotion = detect_emotion(user_input)
    print(f"It sounds like you're feeling {emotion}.")
    advice = provide_advice(emotion)
    print(advice)

if __name__ == "__main__":
    main()
