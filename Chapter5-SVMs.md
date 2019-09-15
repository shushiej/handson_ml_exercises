1. **What is the fundamental idea behind SVMs?**
SVMs attempt to transform polynomial data into linearly seperable, but using kernel methods. The process of SVMs are to use margins as a way of distinguishing true data from it's outliers. 

2. **What is a support Vector?**
Support vectors are instances that lie on the decision boundary of the margin to dictate whether an instance is an outlier or not. 

3. **Why is it important to scale the inputs when using SVMs?**
Having unscaled data results in inaccurate margins because it is unable to plot a reasonable decision boundary, which will lead to incorrect outlier detections. Using something like `StandardScalers` are essential with SVMs. 

4. **Can an SVM classifier output a confidence score when it classifies an instance? What about a probability?**
SVMs only output confidence scores, they do not output probablities.

5. **Should you use the primal or the dual form of the SVM problem to train a model on a training set with millions of instances and hundreds of features?**
The dual form doesn't work well when the number of instances is smaller that the number of features, so in this case the dual form will be the appropriate method. 

6. **Say you trained an SV< classifier with an RBF kernel. It seems to underfit the training set: should you increase of decrease the gamma? what about C?**
you should both increase gamma and C. Increasing gamma makes the bell curve narrower and may fit the data strictly, and increasing C will have a wider margin so it doesn't underfit.

7. **How should you set the QP Parameters (H,f,A,B) to solve the soft margin linear SV< classifir problem using an off-the-shelf QP Solver?**
------
