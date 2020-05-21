# myclass
This is a classifier trained over 100 labels of unsplash photos
I trained it with the fast.ai library [fast.ai](https://github.com/fastai/fastai)
The labels are:
```
['andesite', 'sandstone', 'basalt', 'dolomite_limestone', 'carbon', 'chert', 'coquina', 'conglomerate', 'diorite', 'schist', 'gabbro',
           'gneiss', 'granite', 'peridotite', 'shale', 'rhyolite']
```
# Heroku Guide
[Rama Blog](https://blog.ramagg.com)
[Youtube video](https://youtu.be/pjgT0Idv6mk)

# Partialy based on this guide
To port the fastai-Guide:
Follow this guide [fastai-Guide](https://course.fast.ai/deployment_render.html)
add a Procfile and put ```web: python app/server.py serve``` in it
Then in the server.py file 
  * import os library ```import os```
  * Set the variable: ```Port = int(os.environ.get('PORT', 50000))```
  * In uvicorn.run set port to Port ```uvicorn.run(app=app, host='0.0.0.0', port=Port, log_level="info")```
If heroku is not using the correct version of python, add a file runtime.txt with ```python-3.7.3```

# Data extraction and Model training
You can see the process of training and obtaining the data in [this notebook](https://colab.research.google.com/drive/1GP_9go6NqARmDQ7hAYeydKnKpxfhlZ_O),
I use fast.ai library to train it and Unsplash api to get the data.
