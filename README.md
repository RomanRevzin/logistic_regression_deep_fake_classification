# Logistic regression deep fake classification
A Logistic regression model built from scratch that classifies input images as real/fake with high accuracy
<h2>Readme</h2>
The following project is our implementation of the Logistic Regression classification with Gradient Descent model.</br>
The used dataset contains 1000 images sized 1024X1024, divided to 500 'Real' and 500 'Fake' images </br>
and labled accordingly. The goal of the project is to be able to classify new images as real or fake using</br>
the properties achieved during the learning process.</br>
The model was built from scratch and the code contains the implementation of all the used calculations,</br>
without any ML/AI external libraries. We used Open-CV to process the dataset images, Pandas and Numpy for</br>
convenient storage and usage of data structures, seaborn and matplotlib.pyplot for the plots and graphical endpoints</br>
and os for operaing system related actions.</br>
The notebook contains different sections, each has a header that describes the following cells and their responesbility</br>
and inside comments that describe the micro responsebilities and implementations.</br>
The first few cells contain different utilities for plotting and data handling.</br>
The following cells contain the Logistic Regression model's different functions and utilities, including</br>
algorithms and optimization functions.</br>
The last cells contain the concrete model's implementation and import/export functions to fasten and ease the</br>
model's handling.</br>
</br>
<b>Regarding the data processing, we performed the following actions (in order):</b></br>
read and input data using open-cv <b>-></b> activate fft, fftshift on each image <b>-></b> calculate the azimuthal average of each image <b>-></b> normalize</br>
</br>
<b>Regarding the model itself and the ways to initialize the model, we suggest 4 options:</b></br>
1. Complete learning using pre-defined (optimal and efficient values we found) learning rate and iterations.</br>
2. Complete learning with an algorithm to find the optimal learning rate and iterations.</br>
3. Initialization through import - importing our existing model, attached in the 'model.npy' file.</br>
4. Initialization of an empty model.</br>
</br>
Each initialization/creation method will affect the time to it takes to initialize, the amount of resources</br>
the project will use in the process and the accuracy.</br>
</br>
The data is tagged as 'Real'=0, 'Fake'=1 and located inside matching folders in a './data' folder in the root of the</br>
notebook (watch the matching functions' documentaion for more information).</br>
</br>
The calculated coefficients are found at model.w_vector for the coefficients vector (sorted by iterations)</br>
or model.wm for the last iteration's coefficients, those to whom the model has converged. Use the import/export</br>
functions to import/export the coefficients for later usage.</br>
</br>
To run a test on new data, place the data in a './data/FutureData' folder in the root of the notebook (watch the matching</br> functions' documentaion for more information).</br>
After placing the data, activate model.test() method to view the classification results.</br>
The results will be written to a 'FutureDataEstimatedLabels.csv' file in the root of the notebook (watch the matching</br> functions' documentaion for more information).</br>
