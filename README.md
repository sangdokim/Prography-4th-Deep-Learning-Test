# Prography-4th-Deep-Learning-Test

1. open terminal in your directory
2. 
<pre><code>IMAGE_SIZE=224</code></pre>
3. 
<pre><code>ARCHITECTURE="mobilenet_0.50_${IMAGE_SIZE}"</code></pre>
4. 
<pre><code>python3 -m train   --bottleneck_dir=files/bottlenecks   --how_many_training_steps=500   --model_dir=files/models/   --summaries_dir=files/training_summaries/"${ARCHITECTURE}"   --output_graph=files/retrained_graph.pb   --output_labels=files/retrained_labels.txt   --architecture="${ARCHITECTURE}"   --image_dir=train/</code></pre>
5. 
<pre><code>python3 -m test     --graph=files/retrained_graph.pb      --image=test/ANY_DIRECTORY/ANY_FILE</code></pre>
