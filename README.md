![textcircle-min](https://user-images.githubusercontent.com/83787591/220442759-dea70912-3072-4168-80e1-98febac39b52.jpg)

# Astro Textcircle
If you want to showcase your text in a circular layout, give this Astro component a try.

## [Live Demo](https://www.example.com)


## Instalation
> using npm
```
npm install astro-textcircle
```
> using pnpm
```
pnpm add astro-textcircle
```


## Possible Props 
If Visual Studio Code is your preferred IDE, simply press CRTL+SPACE / CMD+SPACE to reveal the valid properties.
- **text** [sting]
- **class** [sting] 
- **options** [object]
- **animation** [object]
```
text: string;
class?: string;
options?: {
  spacing?: number;
  uppercase?: boolean;
  fontSizeInRem?: number;
  fontWeight?: 'lighter' | 'normal' | 'bold' | 'bolder' | number;
  divider?: string;
  dividerColor?: string;
  rotation?: number;
};
animation?: {
  duration: string;
  timing?: 'ease' | 'ease-in' | 'ease-out' | 'ease-in-out' | 'linear' | string;
  delay?: string;
  direction?: 'normal' | 'reverse';
  count?: 'infinite' | number;
  animateOnHover?: boolean;
  stopAnimateOnHover?: boolean;
};
```
### **divider and dividerColor**
> Give your text a stylish twist with a divider instead of spacing - just use the **divider** property and set a custom color with **dividerColor**.
> 
> Keep in mind that in order to use the **dividerColor** property, the **divider** property must be set beforehand.

### **rotation**
> If the **rotation** of your text isn't to your liking, don't worry - simply adjust it with the rotate property. Just input a number in degrees and watch your text rotate accordingly.


## How to use
```js
---
import { Textcircle } from 'astro-textcircle';
---

<div>

  <!-- basic -->
  <Textcircle text="Display text in a circle"/>

  <!-- using options -->
  <Textcircle 
    text="Display text in a circle"
    options={{ 
      uppercase: true,
      fontSizeInRem: 0.75,
      fontWeight: 'bold',
      divider: '-',
      dividerColor: 'red'
    }}
  />

</div>
```