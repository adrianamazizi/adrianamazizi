class FibonacciThread(threading.Thread):
    def __init__(self, n):
        threading.Thread.__init__(self)
        self.n = n

    def run(self):
        sequence = []
        a, b = 0, 1
        while a <= self.n:
            sequence.append(a)
            a, b = b, a + b
        print("Fibonacci Series:", sequence)
