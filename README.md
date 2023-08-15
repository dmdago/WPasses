# WPasses

Logic to set font color base on bg color

/** @const {string} The font color used with dark backgrounds. */
const FONT_COLOR_LIGHT = 'white';

/** @const {string} The font color used with light backgrounds. */
const FONT_COLOR_DARK = '#202124';

const fontColor =
          isColorLight(value) ? FONT_COLOR_DARK : FONT_COLOR_LIGHT;
      domElement.style.setProperty('--passview-font-color', fontColor);
      break;


const isColorLight = (color) => {

  const redLumaCoefficient = 299;
  const greenLumaCoefficient = 587;
  const blueLumaCoefficient = 114;
  const lightLumaThreshold = 170;

  const hexRegExp = /#([0-9abcdef]{2})([0-9abcdef]{2})([0-9abcdef]{2})/i;
  const [, r, g, b] = hexRegExp.exec(color);
  const brightness = (
      parseInt(r, 16) * redLumaCoefficient +
      parseInt(g, 16) * greenLumaCoefficient +
      parseInt(b, 16) * blueLumaCoefficient) / 1000;

      return brightness > lightLumaThreshold;
    }![image](https://github.com/dmdago/WPasses/assets/56852037/165705c8-ff5e-444b-bfe2-9ccb316ae9d1)
