1. Setup is to import all the libraries that will or might be used in the following codes execution.

2. There are 5 functions:
	i) "hsv_blur(img)" function is to get the original image and convert it into HSV
	   before performing the Gaussian Blurring and lastly return the result

	ii) "segmentation(img, img_hsv)" function is to get the original image and the hsv
	    image in order to perform the color space segmentation and return the segmented
	    results
	
	iii) "flood_fill(closing)" function is to filling up the segmented area and return
	     the flood filled result

	iv) "draw_contour_bounding_box(mask, result)" function is to use the segmented mask
	    and the result from the segmentation function to get the traffic sign contour
	    before drawing a bounding box on it

	v) "confusing_matrix" function is to compare the ground truth and the segmented
	   bounding box pixel by pixel to get the TP, TN, FP, and FN for the confusion
	   matrix calculation

3. The purpose of reading annotation file is to get the images name for looping and ground truth

4. determine the annotation values for knowing which one is x1, x2, y1, y2 for ground truth ROI

5. Perform Segmentation is to run the whole segmentation process by calling the functions and the segmented bounding box x1, x2, y1, y2 are saved in the arrays

6. Calculate Confusion Matrix and Result is to call the confusion_matrix function for the accuracy, IOU, precision, recall and F-score calculation

7. Final Results will be going to sum up the results got from the 6. and get the average