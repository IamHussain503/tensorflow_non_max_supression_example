# tensorflow_non_max_supression_example
this repo contains most basic usage of tensorflow non_max_supression with concrete example


tf.image.non_max_suppression(
    boxes, scores, max_output_size, iou_threshold=0.5,
    score_threshold=float('-inf'), name=None
)

Prunes away boxes that have high intersection-over-union (IOU) overlap with previously selected boxes. Bounding boxes are supplied as [y1, x1, y2, x2], where (y1, x1) and (y2, x2) are the coordinates of any diagonal pair of box corners and the coordinates can be provided as normalized (i.e., lying in the interval [0, 1]) or absolute. Note that this algorithm is agnostic to where the origin is in the coordinate system. Note that this algorithm is invariant to orthogonal transformations and translations of the coordinate system; thus translating or reflections of the coordinate system result in the same boxes being selected by the algorithm. The output of this operation is a set of integers indexing into the input collection of bounding boxes representing the selected boxes. The bounding box coordinates corresponding to the selected indices can then be obtained using the tf.gather operation. For example:

selected_indices = tf.image.non_max_suppression(
      boxes, scores, max_output_size, iou_threshold)
  selected_boxes = tf.gather(boxes, selected_indices)
  
# click the link to access arguments and values
  
  https://www.tensorflow.org/api_docs/python/tf/image/non_max_suppression#args
