package calcimc;

import javax.swing.JOptionPane;
import java.text.DecimalFormat;

/**
 *
{
    public static void main (String[] args)
    {
        String nome;
        float peso, altura;
        float imc;
        String calculado;
        
        nome =    JOptionPane.showInputDialog("Entre com nome?");
        peso =    Float.parseFloat (JOptionPane.showInputDialog("Entre com seu Peso (KG):"));
        altura =  Float.parseFloat (JOptionPane.showInputDialog("Entre com sua Altura em Cm:"));
        
        imc = (float) (peso/Math.pow((altura/100),2));//transforma cm em metros primeiro e depois eleva ao quadrado
        if (imc <= 17)
            Calculo = "Muito abaixo do peso";
        else
        if (imc >= 17 && imc <=18.49)
            Calculo = "Abaixo do Peso";
        else
        if (imc >=18.50 && imc <= 24.99)
             Calculo = "Peso normal";
        else
        if (imc >= 25 && imc <=29.99)
             Calculo = "Acima do Peso";
        else
        if (imc >= 30 && imc <=34.99)
             Calculo = "Obesidade I";
         else
         if (imc >= 35 && imc <=39.99)
            Calculo = "Obesidade II(Severa)";
        else
            Calculo = "Obesidade móbida.";
        DecimalFormat df = new DecimalFormat("##.##");        
        JOptionPane.showMessageDialog(null,"Olá, "+nome+" seu IMC é ="+df.format(imc)+" - "+Calculo);         
    }  
}
