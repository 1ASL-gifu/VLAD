# VLAD
```VLAD: A VLM-Augmented Autonomous Driving Framework with Hierarchical Planning and Interpretable Decision Process.```

## Question-Answer Dataset examples (nuScenes)
The QA Dataset is generated offline with an automatic pipeline and the states of the environment are retrieved from ground-truth labels. This way, we can fine-tune VLAD on accurate data, ensuring the quality of its output when validating its high-level planning abilities and explainability capabilities within nuScenes dataset.

### Perception
We prompt the model to provide scene descriptions for each camera and detect if there are other agents (with a particular focus on pedestrians and cyclists). Moreover, we ask the model to detect if there are any traffic lights, along with their state.

Example 1
![perce](./imgs/2.png)

Example 2
![perce](./imgs/18.png)

Example 3
![perce](./imgs/19.png)

### Prediction
For each detected actor, we prompt the model to predict their future motions for the next few seconds (the prediction is a high-level command).

![pred](./imgs/1.png)

### Planning

Based on the perceived and forecasted environment, we query the model to provide a high-level command that will guide the ego vehicle for the next few seconds, along with an explanation.

![plan](./imgs/20.png)



## Question-Answer Dataset examples (CARLA)
We have also designed the same automatic pipeline to generate QA data within CARLA simulator. This way, we can test the generalization capabilities of our framework and at the same time we prepare an environment for closed-loop evaluations we plan to do in the near future.

### Perception

![perce](./imgs/3.png)
![perce](./imgs/4.png)
![perce](./imgs/5.png)
![perce](./imgs/6.png)
![perce](./imgs/7.png)
![perce](./imgs/8.png)
![perce](./imgs/10.png)
![perce](./imgs/11.png)

### Prediction
![perce](./imgs/12.png)
![perce](./imgs/13.png)
![perce](./imgs/14.png)
![perce](./imgs/15.png)

### Planning
![perce](./imgs/16.png)
![perce](./imgs/17.png)