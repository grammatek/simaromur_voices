This repository contains resources for the [Símarómur App](https://github.com/grammatek/simaromur) voice assets. These voices are neural network voices produced by [Grammatek ehf](https://grammatek.is/).

## Voices

This repository contains the voice `Steinn`. It is based on the neural network model [VITS](https://github.com/jaywalnut310/vits) and trained via
[Piper TTS](https://github.com/rhasspy/piper), as well as converted to ONNX for inferencing.

### Audio Samples

*Chelsea hefur gengið allt á afturfótunum að undanförnu og í raun alveg síðan Roman Abramovich seldi félagið eftir innrás Rússa í Úkraínu.*

[Chelsea.webm](https://github.com/grammatek/simaromur_voices/assets/734966/7ff78d95-aa90-44de-af97-13fa82112223)

*Jürgen Klopp, knattspyrnustjóri Liverpool, beið í tvo mánuði með að tilkynna ákvörðun sína um að hann hygðist láta af störfum sem stjóri félagsins eftir tímabilið.*

[Jürgen.webm](https://github.com/grammatek/simaromur_voices/assets/734966/27b4784c-96c3-45f4-823d-140933fef6b3)

*Greiningardeild Íslandsbanka segir að meðvindur á hlutabréfamörkuðum bæði hér á landi og erlendis hafi gert gæfumuninn á að raunávöxtun íslenskra lífeyrissjóða var jákvæð á lokaársfjórðungi síðasta árs.*

[Íslandsbanka.webm](https://github.com/grammatek/simaromur_voices/assets/734966/db341da6-286e-43db-bbc7-502fabd9f267)

### Training
*Steinn* has been trained for ~750.000 steps on the Talromur1 [H dataset](https://repository.clarin.is/repository/xmlui/handle/20.500.12537/104).
All normalized text was transcribed to IPA phonemes in combination with primary and secondary syllable stresses. You need to use the voice
together with the [Símarómur App](https://github.com/grammatek/simaromur), starting from version 2. Earlier versions of the app do not support ONNX models and IPA phoneme input.

## Voice description files

The [voice configuration](is-steinn-xs-ipa.onnx.json) file is used to describe the voice settings and IPA/ model symbol mappings.
The file [voice-info.json](voice-info.json) is used as meta-data for the corresponding voice files.

## License

The repository contents are licensed under the [Apache License](LICENSE).

## Acknowledgements
These resources are developed under the auspices of the Icelandic Government 5-Year Language Technology Program, described
[here](https://www.stjornarradid.is/lisalib/getfile.aspx?itemid=56f6368e-54f0-11e7-941a-005056bc530c) and
[here](https://clarin.is/media/uploads/mlt-en.pdf) (English).
