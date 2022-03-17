#include <stdio.h>
#include <assert.h>


struct max_min_result {
	int max_value;
	int min_value;
	unsigned int max_position;
	unsigned int min_position;
}

struct max_min_result compute_max_min(int array[], unsigned int length){
	struct max_min_result result;
	result.max_value = array[0];
	result.min_value = array[0];
	int i = 0;
	int currentValue;
	assert(length > 0);
	while(i < length){
		currentValue = array[i];
		if(currentValue > result.max_value){
			result.max_value = currentValue;
			result.max_position = i;
		}
		if(currentValue < result.min_value){ 
			result.min_value = currentValue;
			result.min_position = i;
		}
		i = i+1;
	}
	return result;
}

int main(void){
	runTest();
	
	return 0;
}

int runTest(){
	struct max_min_result expected = compute_max_min({1,2,3,-5,6,7,80,79}, 8);
	assert(expected.min_value == -5);
	assert(expected.min_position == 3);
	assert(expected.max_value == 80);
	assert(expected.max_position == 6);
}

