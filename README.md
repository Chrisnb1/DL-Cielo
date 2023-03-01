# Deep Learning Cielo
_Clasificación de distintas condiciones de cielo utilizando diferentes técnicas de Deep Learning._

## Descripción
Se construyó un dataset con la clasificación de diferentes condiciones de cielo:

* Despejado
* Parcialmente nublado
* Totalmente nublado

y se utilizaron tres arquitecturas diferentes de redes neuronales.

* Modelo Denso
* Modelo Convolusional
* Modelo Pre-Entrenada (MobileNet v2)

## Set de datos

![image](https://user-images.githubusercontent.com/63667971/222279001-e654ae5d-32df-439a-b293-fb2e5618e526.png)

## Redes Neuronales

### Modelo Denso

```
Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 flatten (Flatten)           (None, 150528)            0         
                                                                 
 dense (Dense)               (None, 50)                7526450   
                                                                 
 dense_1 (Dense)             (None, 50)                2550      
                                                                 
 dense_2 (Dense)             (None, 3)                 153       
                                                                 
=================================================================
Total params: 7,529,153
Trainable params: 7,529,153
Non-trainable params: 0
_________________________________________________________________
```

### Modelo Convolusional

```
Model: "sequential_1"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 222, 222, 32)      896       
                                                                 
 max_pooling2d (MaxPooling2D  (None, 111, 111, 32)     0         
 )                                                               
                                                                 
 conv2d_1 (Conv2D)           (None, 109, 109, 64)      18496     
                                                                 
 max_pooling2d_1 (MaxPooling  (None, 54, 54, 64)       0         
 2D)                                                             
                                                                 
 conv2d_2 (Conv2D)           (None, 52, 52, 128)       73856     
                                                                 
 max_pooling2d_2 (MaxPooling  (None, 26, 26, 128)      0         
 2D)                                                             
                                                                 
 flatten_1 (Flatten)         (None, 86528)             0         
                                                                 
 dense_3 (Dense)             (None, 100)               8652900   
                                                                 
 dense_4 (Dense)             (None, 3)                 303       
                                                                 
=================================================================
Total params: 8,746,451
Trainable params: 8,746,451
Non-trainable params: 0
_________________________________________________________________
```

### Modelo Convolusional MobileNet v2
```
Model: "sequential_2"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 keras_layer_1 (KerasLayer)  (None, 1280)              2257984   
                                                                 
 dense_5 (Dense)             (None, 3)                 3843      
                                                                 
=================================================================
Total params: 2,261,827
Trainable params: 3,843
Non-trainable params: 2,257,984
_________________________________________________________________
```
