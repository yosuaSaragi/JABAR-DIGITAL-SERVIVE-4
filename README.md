# JABAR-DIGITAL-SERVIVE-4
jawaban untuk DE-phyton 2


def pipeline(*funcs):
    def helper(arg):
        result = arg
        for f in funcs:
            result = f(result)
        return result
    return helper
            
fun = pipeline(lambda x: x * 3, lambda x: x + 1, lambda x: x / 2)
print(fun(3)) #should print 5.0
