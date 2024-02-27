function solution(young, beautiful, loved) {
    // Condition 1: They are young and beautiful but not loved
    if (young && beautiful && !loved) {
        return true;
    }
    // Condition 2: They are loved but not young or not beautiful
    if (loved && (!young || !beautiful)) {
        return true;
    }
    // No contradiction found
    return false;
}

// Test cases
console.log(solution(true, true, true));  // Output: false
console.log(solution(true, false, true)); // Output: true
