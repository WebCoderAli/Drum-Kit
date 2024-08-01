# Drum Kit

## HTML Structure

- **Heading:** The page features a title (`<h1>`) labeled "Drum 🥁 Kit".
- **Drum Buttons:** A container (`<div class="set">`) holds seven buttons (`<button class="drum">`) corresponding to different drum sounds, labeled with the letters `w`, `a`, `s`, `d`, `j`, `k`, and `l`.
- **Footer:** A footer element displays the text "Made with ❤️ in Pakistan."

## CSS Styling

- **Background and Text:** 
  - The body has a dark blue background color (`#283149`).
  - The title is styled with a large font size, a light color (`#DBEDF3`), and a text shadow in pink (`#DA0463`). The font family used is "Arvo".
- **Footer Styling:** The footer text is colored light blue (`#DBEDF3`) and uses a sans-serif font.
- **Button Styling:** 
  - Each button has a background image corresponding to its sound (e.g., `tom1.png` for the `w` button).
  - Buttons have a consistent style with no outline, a solid border, and rounded corners. They display in a large font size with bold styling, using the "Arvo" font.
  - A `.pressed` class applies a visual effect when buttons are clicked, reducing opacity and adding a shadow.
- **Layout:** The buttons are centered within the container, which is itself centered on the page.

## JavaScript Functionality

### Button Event Listeners

- **Click Events:** An event listener is added to each button. When a button is clicked, it:
  - Retrieves the innerHTML of the button (which corresponds to a specific drum sound).
  - Calls the `makeSound` function to play the appropriate sound.
  - Calls the `buttonAnimation` function to animate the button.

- **Keypress Events:** An event listener is added to the document to listen for keypresses. When a key corresponding to a drum sound is pressed, it:
  - Calls the `makeSound` function to play the appropriate sound.
  - Calls the `buttonAnimation` function to animate the button.

### Sound Playback

- `makeSound(key)`: This function plays the corresponding sound for each key. It uses a switch statement to determine which sound file to play based on the key pressed or button clicked.

### Button Animation

- `buttonAnimation(currentKey)`: This function adds the `.pressed` class to the button corresponding to `currentKey`, which adds a visual effect. The class is removed after a short delay (100ms).

## User Interaction

- **Clicking Buttons:** Users can click on the displayed buttons to play different drum sounds.
- **Keypress Events:** Users can also press the corresponding keys on the keyboard (`w`, `a`, `s`, `d`, `j`, `k`, `l`) to trigger the sounds and animations.
