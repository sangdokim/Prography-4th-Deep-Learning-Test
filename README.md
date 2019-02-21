# Prography-4th-Deep-Learning-Test

I used tensorflow transfer learning with mobilenet_0.50v.

open terminal in your directory
1. First, set the variable
<pre><code>$ IMAGE_SIZE=224</code></pre>
<pre><code>$ ARCHITECTURE="mobilenet_0.50_${IMAGE_SIZE}"</code></pre>

2. Following code will train model with transfer learning and save the result in "files" category  
also, it will automatically download mobilenet_0.50v, the model I used.
<pre><code>$ python3 -m train
  --bottleneck_dir=files/bottlenecks
  --how_many_training_steps=500
  --model_dir=files/models/
  --summaries_dir=files/training_summaries/"${ARCHITECTURE}"
  --output_graph=files/retrained_graph.pb
  --output_labels=files/retrained_labels.txt
  --architecture="${ARCHITECTURE}"
  --image_dir=train/</code></pre>
  
3. Following code can classify the image which you want to check
<pre><code>$ python3 -m test
  --graph=files/retrained_graph.pb
  --image=test/ANY_DIRECTORY/ANY_FILE</code></pre>
