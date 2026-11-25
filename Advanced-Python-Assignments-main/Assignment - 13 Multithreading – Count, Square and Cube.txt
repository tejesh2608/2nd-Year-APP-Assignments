import threading

# Thread 1: Count numbers
def count():
    for i in range(1, 6):
        print("Count:", i)

# Thread 2: Calculate square
def square():
    for i in range(1, 6):
        print("Square of", i, "=", i*i)

# Thread 3: Calculate cube
def cube():
    for i in range(1, 6):
        print("Cube of", i, "=", i*i*i)

# Create threads
t1 = threading.Thread(target=count)
t2 = threading.Thread(target=square)
t3 = threading.Thread(target=cube)

# Start threads
t1.start()
t2.start()
t3.start()

# Wait for completion
t1.join()
t2.join()
t3.join()

print("All threads completed!")
