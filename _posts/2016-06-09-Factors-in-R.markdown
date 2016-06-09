## Factor Variables 
 
1.  Are similar to categorical variables
2. Created using the factor function
3. Take a string as input and returns a factor variable with "factor levels" or categories defined

     > gender_vector <- c("Male", "Female", "Female", "Male", "Male")
    
    > \#Convert gender_vector to a factor
    > factor_gender_vector <- factor(gender_vector)
    >   
    > \# Print out factor_gender_vector
    > print(factor_gender_vector)
    > 
    [1] Male   Female Female Male   Male  
    Levels: Female Male
 
There are two ***types of factor variables***

1. **Nominal** - Order does not matter like Gender
2. **Ordinal** - Order matters  like low/high

    > \# Animals
    > animals_vector <- c("Elephant", "Giraffe", "Donkey", "Horse")
    > factor_animals_vector <- factor(animals_vector)
    > factor_animals_vector
    [1] Elephant Giraffe  Donkey   Horse   
    Levels: Donkey Elephant Giraffe Horse
    > 
    > \# Temperature
    > temperature_vector <- c("High", "Low", "High","Low", "Medium")
    > factor_temperature_vector <- factor(temperature_vector, order = TRUE, levels = c("Low", "Medium", "High"))
    > factor_temperature_vector
    [1] High   Low    High   Low    Medium
    Levels: Low < Medium < High

**levels function** can be used to rename the levels of the factor variable.  The order of the factors should not be changed before assigning the values. 

    > levels(factor_survey_vector)
    > # Code to build factor_survey_vector
    > survey_vector <- c("M", "F", "F", "M", "M")
    > factor_survey_vector <- factor(survey_vector)
    > levels(factor_survey_vector)
    [1] "F" "M"
    > # Specify the levels of factor_survey_vector
    > levels(factor_survey_vector) <- c("Female","Male")
    > 
    > factor_survey_vector
    [1] Male   Female Female Male   Male  
    Levels: Female Male
    > 
**Ordered factors** have a implicit ordering of the factors.

    > # Create speed_vector
    > speed_vector <- c("fast", "slow", "slow", "fast", "insane") 
    > 
    > # Convert speed_vector to ordered factor vector
    > factor_speed_vector <-  factor (speed_vector, ordered=TRUE, levels = c("slow","fast","insane"))
    > 
    > # Print factor_speed_vector
    > factor_speed_vector
    [1] fast   slow   slow   fast   insane
    Levels: slow < fast < insane
    > summary(factor_speed_vector) 
      slow   fast insane 
         2      2      1