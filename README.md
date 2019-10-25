# Transactive-Energy-with-Reinforcment-Learning-Deep-Q-Network

* The script is coded in Google Colab, thus there exist commands to retrieve files from and store files to google drive. Modification is required for any personal use.

* The data used in the project is modified from GEFCom2014 (load & real time pricing) and Energy Market Authority (solar). The energy storage system used in the project is rated 1000kW and 5000kWh.

* In this project, a model free value based reinforcement learning method - deep-q-network is trained to execute energy trading decision using energy storage system according to real time pricing, load, solar and etc. To facilitate the training, prioritized experience replay is employed to utilize the experience (state, action, reward, next_state) stored in the memory. 

* The model is trained in both with and without solar. For environment without solar, the energy storage system is to react to the real time price and store energy and release energy at the appropriate timing to reduce overall cost (energy gain, trading cost and wear cost of energy storage system). For environment with solar, the energy storage system not only needs to reduce the overall cost but also requires to contain solar within the building (as not to affect the grid system stability)

* From the training result, it is found that the model is able to react to real time pricing and solar penetration accordingly and achieve significant return as compared to the case without energy storage system.

* On top of energy trading, the ability of ESS providing contingency resource is explored and a piecewise reward function is formulated to trade off monetary benefit and contigency resource. The behaviour of ESS operator, risk seeking or risk adverse, can be studied by adjusting the parameter of reward function.
