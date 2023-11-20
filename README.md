# KindnessGen
KindnessGen Code



import tkinter as tk
from tkinter import messagebox
import random

kindnessActs = [
    "Give an unexpected compliment.",
    "Plant a tree.",
    "Let someone cut in front of you in line.",
    "Pay the toll for the car behind you.",
    "Slow down so someone can merge in front of you in traffic.",
    "Let someone else take that primo parking spot.",
    "Give someone your seat on a crowded bus or subway.",
    "Put coins in an expired parking meter.",
    "Give up your seat on a plane so other travelers can sit together.",
    "Buy a warm meal for someone in need.",
    "Help someone struggling to carry their grocery bags.",
    "Stop to assist someone who looks lost.",
    "Say something encouraging to a parent who's struggling with rambunctious kids in a restaurant or grocery store.",
    "Offer to return a stranger's grocery cart to the front of the store.",
    "Keep plastic bags filled with snacks and sample-size toiletries in your car to give to the homeless. Genius Tip: Organize homeless shelter volunteers with an online sign up.",
    "Donate flowers to a nursing home.",
    "Hand out disposable water bottles to people working outside on a hot day.",
    "Buy a gift card to hand to someone on your way out of the coffee shop.",
    "Leave a great coupon next to that item in the grocery store.",
    "Pick up a piece of litter on the street and throw it out.",
    "Pass along a compliment to a service worker's boss.",
    "Take the time to write a great online review for a restaurant you love.",
    "Pay for the meal of the people at the next table. (Leave before they realize what you've done.)",
    "Leave a positive comment on a news article or blog post.",
    "Learn CPR.",
    "Give an extra tip and write an encouraging note along with it.",
    "Keep an extra umbrella in your car to give to someone stuck in the rain.",
    "Buy lemonade from a child's lemonade stand.",
    "Visit a nursing home — read books to or play board games with residents.",
    "Send a care package to a service member.",
    "Bring treats to your local fire station.",
    "Write a thank you note to your mail carrier.",
    "Talk to a stranger at a party who looks like they don't know anyone.",
    "Smile at someone who looks sad."
]

def generate_act():
    your_act = random.choice(kindnessActs)
    return your_act

def roll_action():
    roll = messagebox.askquestion("Roll Kindness Act", "Would you like to roll?")
    if roll == 'yes':
        act = generate_act()
        result_label.config(text=f"Your act of the day is to {act.lower()}")
    else:
        messagebox.showinfo("Thank You!", "Thank you!")

# Create main window
root = tk.Tk()
root.title("Kindness Act Generator")

# Create and configure widgets
generate_button = tk.Button(root, text="Generate Act", command=roll_action)
generate_button.pack(pady=20)

result_label = tk.Label(root, text="")
result_label.pack()

# Run the main loop
root.mainloop()
