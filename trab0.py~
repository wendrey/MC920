# # # # # # # # # # # # # # # # # # # # # # 
# Wendrey Lustosa Cardoso 148234 		  #
# MC920 - Trabalho 0				 	  #
# # # # # # # # # # # # # # # # # # # # # #

from scipy import misc
import numpy as np
import matplotlib.pyplot as plt

def mosaic (img) :
		
	a1,a2,a3,a4 = np.vsplit(img,4)	
	b1,b2,b3,b4 = np.hsplit(a1,4)
	b5,b6,b7,b8 = np.hsplit(a2,4)
	b9,b10,b11,b12 = np.hsplit(a3,4)
	b13,b14,b15,b16 = np.hsplit(a4,4)

	c1 = np.concatenate((b6,b11,b13,b3), axis = 1)
	c2 = np.concatenate((b8,b16,b1,b9), axis = 1)
	c3 = np.concatenate((b12,b14,b2,b7), axis = 1)
	c4 = np.concatenate((b4,b15,b10,b5), axis = 1)
	
	return np.concatenate((c1,c2,c3,c4), axis = 0)

def intensity_negative (img) :

	return 255 - img

def intensity_range (img) :

	return 100 / 255 * img + 100
	
def combination (imga, imgb, ratio) :

	return ratio * imga + (1 - ratio) * imgb
	
def main () :

	imga = misc.imread('baboon.png')
	imgb = misc.imread('butterfly.png')

	img1 = mosaic(imga)
	plt.imshow(img1, 'gray')
	plt.show()
	misc.imsave('img1.png', img1)
	
	img2 = intensity_negative(imga)	
	plt.imshow(img2, 'gray')
	plt.show()
	misc.imsave('img2.png', img2)
	
	img3 = intensity_range(imga)
	plt.imshow(img3, 'gray')
	plt.show()
	misc.imsave('img3.png', img3)
	
	img4 = combination(imga,imgb,0.2)
	plt.imshow(img4, 'gray')
	plt.show()
	misc.imsave('img4.png', img4)
	
	img5 = combination(imga,imgb,0.5)
	plt.imshow(img5, 'gray')
	plt.show()
	misc.imsave('img5.png', img5)

	img6 = combination(imga,imgb,0.8)
	plt.imshow(img6, 'gray')
	plt.show()
	misc.imsave('img6.png', img6)

if __name__ == "__main__" :
	main()

