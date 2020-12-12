 int array[] = new int[]{56, 88, 1, 22, 4, 6};

      public int maximumSumOfArray() {

        int firstNumber, secondNumber, i;
        if (array[0] > array[1]) {
            firstNumber = array[0];
            secondNumber = array[1];
        } else {
            firstNumber = array[1];
            secondNumber = array[0];
        }

        for (i = 2; i < array.length; i++) {
            if (array[i] > firstNumber) {
                secondNumber = firstNumber;
                firstNumber = array[i];
            } else if (array[i] > secondNumber && array[i] != firstNumber)
                secondNumber = array[i];
        }
        return (firstNumber + secondNumber);
    }
