**70-71-72-异常知识try&expect的讲解**

'''
try--expect的执行步骤
1:try代码执行正确,就不会执行except的内容
2:只有当try代码执行错误的时候,才会支持eccept的内容
'''
02:常见的异常
KeyError
ValueError
ZeroDivisionError
WindowsError
 EOFError
------------------------------------------------------------
03:try-except的案例演示

def div(a,b)
	return a/b

try:
    div(1,0)
except Exception as e:
    print(e.args)
----------------------------------------------------------
'''
try--expect-- else --finalyy:
1:如果try执行通过,就是执行else,finally
2:如果try执行失败,直接执行finally
'''
try:
	div(1,99)
except Exception as e:
	print(e.args)
	print(u'我是执行失败了')
else:
	print('try成成功了就执行这个')
finally:
	print('try执行失败就执行这个')
---------------------------------------------------------------
raise
01-您可以使用 raise 语句引发异常(您需要指定引发的异常的类型)
02-在 except 块下，raise 语句可以在没有参数的情况下使用来重新引发发生的异常
03-引发异常可以提供一些异常的描述 raise NamwType 'xxxxxx'
--------------------------------------------------------------------------
assert:
01-断言是通过使用 assert 语句来执行的
02-如果断言失败，assert 可以接受第二个传递给 AssertionError 的参数  assert 1==2,'断言失败跑出异常'
