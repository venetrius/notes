# Creational patterns

## Singleton pattern

### point:
- Having only one object of a class
- Globally accessible
- (Lazy creation ~ only when instance needed)

### how to?
- Private constructor
- Private variable to hold the single instance
- Function (getInstance) to return instance of exist or create store and return a new one if not

### cons:
- issue if using multiple threads

