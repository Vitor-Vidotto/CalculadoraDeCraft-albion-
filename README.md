Welcome to my craft calculator, lets explain how to instal:

First of all u need to instal the .NET framework, and that is, only open the .exe

the main code is this one below

```using System;
using System.Windows.Forms;

namespace WinFormsApp1
{
    public partial class Form1 : Form
    {
        private double ValorRecursoA;
        private double ValorRecursoB;
        private double QuantiaRecursoA;
        private double QuantiaRecursoB;
        private double RetornoDoHO;
        private double ValorReliquia;
        public Form1()
        {
            InitializeComponent();
        }

        private void textBox1_TextChanged(object sender, EventArgs e)
        {
            if (double.TryParse(textBox1.Text, out double valor))
            {
                ValorRecursoA = valor;
            }
            else
            {
                // Caso o texto não seja um número válido, você pode tratar o erro aqui se necessário
                MessageBox.Show("Valor inválido. Insira um número válido.");
            }
        }

        private void textBox2_TextChanged(object sender, EventArgs e)
        {
            if (double.TryParse(textBox2.Text, out double valor))
            {
                ValorRecursoB = valor;
            }
            else
            {
                // Caso o texto não seja um número válido, você pode tratar o erro aqui se necessário
                MessageBox.Show("Valor inválido. Insira um número válido.");
            }
        }

        private void textBox4_TextChanged(object sender, EventArgs e)
        {
            if (double.TryParse(textBox4.Text, out double valor))
            {
                QuantiaRecursoA = valor;
            }
            else
            {
                // Caso o texto não seja um número válido, você pode tratar o erro aqui se necessário
                MessageBox.Show("Valor inválido. Insira um número válido.");
            }
        }

        private void textBox3_TextChanged(object sender, EventArgs e)
        {
            if (double.TryParse(textBox3.Text, out double valor))
            {
                QuantiaRecursoB = valor;
            }
            else
            {
                // Caso o texto não seja um número válido, você pode tratar o erro aqui se necessário
                MessageBox.Show("Valor inválido. Insira um número válido.");
            }
        }

        private void textBox5_TextChanged(object sender, EventArgs e)
        {
            if (double.TryParse(textBox5.Text, out double valor))
            {
                RetornoDoHO = valor;
            }
            else
            {
                // Caso o texto não seja um número válido, você pode tratar o erro aqui se necessário
                MessageBox.Show("Valor inválido. Insira um número válido.");
            }
        }

        private void textBox6_TextChanged(object sender, EventArgs e)
        {
            if (double.TryParse(textBox6.Text, out double valor))
            {
                ValorReliquia = valor;
            }
            else
            {
                // Caso o texto não seja um número válido, você pode tratar o erro aqui se necessário
                MessageBox.Show("Valor inválido. Insira um número válido.");
            }
        }

        private void button1_Click(object sender, EventArgs e)
        {
            double resultadodosrecursoA = ValorRecursoA * QuantiaRecursoA;
            double resultadodosrecursoB = ValorRecursoB * QuantiaRecursoB;
            double somadosrecursos = resultadodosrecursoA + resultadodosrecursoB;
            double valordosrecursoscomdesconto = somadosrecursos * 0.95;
            double retornoHO = ((RetornoDoHO / 100) - 1) * -1;
            double resultadocomretorno = valordosrecursoscomdesconto * retornoHO;
            double custodecraft = resultadocomretorno + ValorReliquia;
            string valorFormatado = custodecraft.ToString("N0"); // "N0" formata para separador de milhares e sem casas decimais

            // Atribui o valor formatado ao textBox7
            textBox7.Text = valorFormatado;
        }

        private void textBox7_TextChanged(object sender, EventArgs e)
        {

        }
    }
}
 ```