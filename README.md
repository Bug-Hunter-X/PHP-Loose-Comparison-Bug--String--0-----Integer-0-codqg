# PHP Loose Comparison Bug

This repository demonstrates a common, yet subtle, bug in PHP related to loose comparison using the `==` operator.  The issue arises when comparing strings and integers, specifically when comparing the string '0' to the integer 0.  PHP's type juggling behavior leads to unexpected results, making it crucial to use strict comparison (`===`) when type safety is required.

## Bug Description

The `bug.php` file contains code that showcases the problem.  Loose comparison (`==`) evaluates '0' as equal to 0, resulting in an incorrect conditional evaluation.  The `bugSolution.php` demonstrates the correct solution using strict comparison (`===`).

## How to reproduce

1. Clone the repository.
2. Run `php bug.php` to see the incorrect behavior.
3. Run `php bugSolution.php` to see the correct behavior using strict comparison.

## Solution

Always use strict comparison (`===`) when comparing values in PHP to ensure both the value and the type match. This avoids unexpected behavior caused by PHP's type juggling.