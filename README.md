# l0
// click the <icon src="AllIcons.Actions.Execute"/> icon in the gutter.
public class Main {
    public static void main(String[] args) {


        QuizGame quizGame=new QuizGame();
        quizGame.startQuiz();

        quizGame.askQuestion("40", "12", "10");

        quizGame.endQuiz();

    }
}


import java.util.Objects;
import java.util.Scanner;

public class QuizGame {

    String q1="If a rectangle has a length of 8 meters and a width of 5 meters, what is the area of the rectangle?";
    String q2="What is the square root of 144?";
    String q3="Solve for x: 2(x−4)=12?";


    int score=0;


    public void startQuiz(){
        System.out.println("\nWelcome! Here's your quiz.\nLet's get started!");
    }

    public void askQuestion(String a, String b, String c){
        System.out.println("\n"+q1+"\nYour answer: "+a);
        if (Objects.equals(a, "40")){
            score++;
        }
        System.out.println("\n"+q2+"\nYour answer: "+b);
        if (Objects.equals(b, "12")){
            score++;
        }
        System.out.println("\n"+q3+"\nYour answer: "+c);
        if (Objects.equals(c, "10")){
            score++;
        }
    }

    public void endQuiz(){
        System.out.println("\nYour result: "+score);
    }

}



