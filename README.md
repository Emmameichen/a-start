# a-start
import matplotlib.pyplot as plt

def Beta(x, alpha, beta):
		item = []
		for element in x:
			a = factorial(alpha + beta)
			b = factorial(alpha)
			c = factorial(beta)
			d = power(element, alpha-1)
			e = power(1-element, beta - 1)
			result = a/(b*c)*(d*e)
			item.append(result)
		
		return item

def factorial(n):
	#calculate (n-1)!
	result1 = 1.0
	for m in range(1,n):
		result1 = result1 * m
	return result1

def power(x, a):
	#calculate x^a
	result2 = 1.0
	for b in range(0,a):
		result2 = result2 * x
	return result2

if __name__=="__main__":
	x =[]
	y =[]
	for y in range(1, 1000):
		x.append(y/1000.0)
	y = Beta(x, 3, 3)
	plt.plot(x,y)
	plt.show()
