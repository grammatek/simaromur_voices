This repository contains ressources for the [Símarómur App](https://github.com/grammatek/simaromur) voice assets. These voices are neural network voices produced by the [Reykjavik University Language and Voice Lab](https://lvl.ru.is/) but converted to be usable with PyTorch mobile for inferencing.

## Voices

Two voices are available: Álfur and Díljá. For these a [Fastspeech2](https://github.com/cadia-lvl/fastspeech2) acoustic model is combined with a [WaveGAN]() vocoder model. Each voice needs 2 models. The vocoder model isn't universal.

The voice models are converted to be compatible with PyTorch mobile via these scripts:
- [Fastspeech2 model conversion](https://gitlab.com/tiro-is/tiro-tts/-/blob/7a08c2cb9c2c71678e7736ff4086b11093fdb09d/src/scripts/fastspeech_convert.py)
- [MelGan model conversion](https://gitlab.com/tiro-is/tiro-tts/-/blob/7a08c2cb9c2c71678e7736ff4086b11093fdb09d/src/scripts/melgan_convert.py)

The Fastspeech2 model is quantized for size reduction. Both models only contain the parts necessary for inferencing. The inferencing interfaces of these models are augmented with new  PyTorch mobile compatible interfaces => `runMethod("mobile_inference", ...)` or `runMethod("inference", ...)` but also contain their respective usual inferencing interfaces.

## Voice description file

The file [voice-info.json](voice-info.json) is used to describe the voices and the corresponding voice files. Símarómur parses this file and uses it for applying the appropriate models for inferencing. The exact schema is not yet fixed. It will be developed further according to the needs of newer models we will support in the future.

## License

The repository contents are licensed under the [Apache License](LICENSE).

## Acknowledgements
These resources are developed under the auspices of the Icelandic Government 5-Year Language Technology Program, described
[here](https://www.stjornarradid.is/lisalib/getfile.aspx?itemid=56f6368e-54f0-11e7-941a-005056bc530c) and
[here](https://clarin.is/media/uploads/mlt-en.pdf) (English).