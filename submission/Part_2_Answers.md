# Part 2 – Reasoning-Based Questions

## Q1: Choosing the Right Approach
I would use an object detection approach to identify whether the product has a label or not. Detection is suitable because we need to both locate the label and verify its presence on visually similar products. A simple classification model may fail because it does not consider where the label should appear. Segmentation would be more detailed than required and may increase complexity without much benefit. If detection does not work well, my fallback approach would be a binary classification model combined with region cropping around the expected label area.

## Q2: Debugging a Poorly Performing Model
First, I would compare training and test images to check for differences in lighting, background, or camera angle. I would visualize predictions on new factory images to see where the model is failing. Next, I would check for class imbalance or incorrect labels in the training data. I would also evaluate whether the model is overfitting by comparing training and validation metrics. Finally, I would test performance after adding a small set of new factory images to the training data.

## Q3: Accuracy vs Real Risk
Accuracy is not the right metric in this case because missing defective products has a high real-world cost. I would focus more on recall, especially for the defective class, to ensure fewer missed defects. Precision–recall metrics provide better insight into false negatives. I would also analyze the confusion matrix to understand error types. In such safety-critical systems, minimizing false negatives is more important than overall accuracy.

## Q4: Annotation Edge Cases
Blurry or partially visible objects can be kept in the dataset if they realistically occur in real-world conditions. Including them helps the model become more robust to noise and imperfect data. However, these samples should be labeled carefully to avoid confusing the model. If the object is too unclear, it may introduce label noise and hurt performance. The trade-off is between dataset realism and annotation quality.
