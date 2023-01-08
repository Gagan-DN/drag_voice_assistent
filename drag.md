import speech.recognition as sr
import pyttsx3
import pywhatkit
import datetime
import wikipedia
import pyjokes
listener=sr.Recognizer()
engine.setProperty('voice',voices[1].id)
engine.say('Hey, I am drag')
engine.say('How can I help you')
def talk(text):
engine.say(text)
engine.runAndWait()
def take_command():
try:
with sr.Microphone() as source:
talk('tell me I am listening')
voice=listener.listen(source)
command=command.lower()
if 'drag' in command:
command=command.replace('drag','')
talk(command)
except:
pass
return command
def run_drag():
command=talk_command()
if 'hai' in command:
talk('hello, how are you')
elif 'how are you' in command:
talk('I am fine, how can I help you')
elif 'who are you' in command:
talk('I am drag, your sweetest voice assistant')
elif 'I like you' in command:
talk('Do not try to flirt with me , under section 509 of the IPC , flirting is an offence')
elif(Are you single' in command:
talk('No , I am committed with wifi')
elif 'I love you' in command:
talk('please do not waste your time, I am already committed')
elif 'Do you have feelings' in command:
talk('offcourse, but not as much as you')
elif 'crazy' in command:
talk ('not as much as you')
elif 'you are beautiful' in command:
talk('Thank you, But you can not discribe me physicaly but you can discribe my tune')
elif 'dance' in command:
talk('sorry I can not dance but I can make you dance and get relax by playing wounderful songs')
elif 'play' in command:
song=command.replace('play','')
talk('playing'+song)
pywhatkit.playonyt(song)
elif 'time' in command:
time=datetime.datetime.now().strftime('%I:%M %p')
talk('current time is'+time)
elif 'about' in command:
information=command.replace('wikipedia','')
info=wikipedia.summary(information,3)
talk(info)
elif 'joke' in command:
talk(pyjokes.get_joke())
elif 'child helpline' in command:
talk('child helpline is 1098')
else:
talk('sorry, could you please repeat')
while True:
run_drag()
