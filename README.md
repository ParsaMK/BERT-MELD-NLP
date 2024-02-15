# Description
This repository presents our experimentation revolving around the MELD dataset using Bert for emotion recognition and trigger detection. We tried two different architectures:

1) One Bert model with 8 heads coming out. 7 heads for emotion and 1 head for trigger detection (we loop through the dialogue as many times as the number of utterances.)
2) One Bert model for emotions on an utterance level and one Bert model for trigger detection which gets provided the whole dialogue

Our experiments showed us:
- the second model works significantly better and to our surprise emotion detection does not require the whole context as it will only introduce noise to the model (which wouldn't be the case if we use a bigger model for example Llama 2.)
- Although tiny bert is a significantly smaller model it's really stable or resistant to changing hyperparameters as changing the learning rate for normal Bert introduced a lot of instability. Surprisingly it wasn't the case for the frozen bert models as they were quite resistant as well.
