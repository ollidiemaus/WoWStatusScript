on run {input, parameters}
	
	if application "World of Warcraft" is running then
		activate application "iCUE"
		delay 2
		tell application "iCUE" to activate
		tell application "System Events" to set visible of process "iCUE" to false
		
		tell application "System Preferences"
			activate
			set current pane to pane "com.apple.preference.keyboard"
		end tell
		
		
		tell application "System Events"
			tell process "System Preferences"
				delay 0.3
				click button 1 of tab group 1 of window "Tastatur"
				
				try
					# Select keyboard: pop up button
					click pop up button 5 of sheet 1 of window "Tastatur"
					click menu item "Gaming Keyboard G610" of menu 1 of pop up button 5 of sheet 1 of window "Tastatur"
					delay 0.3
					
					# The Option Key pop up
					click pop up button 4 of sheet 1 of window "Tastatur"
					click menu item "⌥ Wahltaste" of menu 1 of pop up button 4 of sheet 1 of window "Tastatur"
					delay 0.3
					
					# The Command Key pop up
					click pop up button 1 of sheet 1 of window "Tastatur"
					click menu item "⌘ Befehlstaste" of menu 1 of pop up button 1 of sheet 1 of window "Tastatur"
					delay 0.3
				end try
				click button "OK" of sheet 1 of window "Tastatur"
			end tell
		end tell
		
		
		if application "System Preferences" is running then
			tell application "System Preferences" to quit
		end if
		
	else
		quit application "iCUE"
		
		tell application "System Preferences"
			activate
			set current pane to pane "com.apple.preference.keyboard"
		end tell
		
		
		tell application "System Events"
			tell process "System Preferences"
				delay 0.3
				click button 1 of tab group 1 of window "Tastatur"
				
				try
					# Select keyboard: pop up button
					click pop up button 5 of sheet 1 of window "Tastatur"
					click menu item "Gaming Keyboard G610" of menu 1 of pop up button 5 of sheet 1 of window "Tastatur"
					delay 0.3
					
					# The Option Key pop up
					click pop up button 4 of sheet 1 of window "Tastatur"
					click menu item "⌘ Befehlstaste" of menu 1 of pop up button 4 of sheet 1 of window "Tastatur"
					delay 0.3
					
					# The Command Key pop up
					click pop up button 1 of sheet 1 of window "Tastatur"
					click menu item "⌥ Wahltaste" of menu 1 of pop up button 1 of sheet 1 of window "Tastatur"
					delay 0.3
				end try
				click button "OK" of sheet 1 of window "Tastatur"
			end tell
		end tell
		
		
		if application "System Preferences" is running then
			tell application "System Preferences" to quit
		end if
		
	end if
	
	return input
end run
