# Lesson3contactsGoal-4
# Hear me Code / Lesson 3 / Playtime / Contact exercise goal #4 Note: I addes some formatiing to the html table to play a bit with it, this is not required.
infocontacts = []
with open("contacts.csv", "r") as contacts_file:
	contacts = contacts_file.read().split("\r")
allcontacts = enumerate (contacts)
for index, contact in allcontacts:
	contacts[index] = contacts[index].split(",")
#The first item on my list contains the keys, the next comant eliminates the first item on the list, so contacts will only have people's informatio
contacts.pop(0)
#print contacts
for index, contact in enumerate (contacts):
	print '<table border="5" bgcolor="pink" >' + "\n" + '<tr>' + "\n" + '<th colspan="3"> ' + contact[0] + ' </th>' + "\n" + '</tr>' + "\n" + '<tr>' "\n" + '<td> Phone: ' + contact[1] + ' </td>' + "\n" + '<td> Twitter: ' + contact[2] + ' </td>' + "\n" + '<td> Github: ' + contact[3] + ' </td>' + "\n" + '</tr>'+ "\n" + '</table>'+ "\n"
