import math

def draw_heart():
    scale = 10
    heart = ""
    
    for row in range(scale, -scale, -1):
        for col in range(-scale, scale):
            x = col / scale
            y = row / scale
            equation_result = x  2 + y  2 - 1
            
            if (equation_result  3 - x  2 * y ** 3) <= 0:
                heart += "*"
            else:
                heart += " "
        
        heart += "\n"
    
    return heart

heart_shape = draw_heart()
print(heart_shape)
