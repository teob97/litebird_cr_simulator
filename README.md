# Generative Adversarial Network for the simulation of cosmic ray glitches in LiteBIRD timelines

## Dependencies
See `env.yml`

The latest version of the program is developed to run on GPU.

## Use the model
To use the trained model:
```
from keras.models import load_model
model = load_model('Saved_models/model_4')
```
N.B. currently model_4 is the latest and best performing version

Then to generate *n_samples*:
```
z = np.random.normal(0.0, 1.0, (n_samples, 500))
TOD = model.predict(z)
```
