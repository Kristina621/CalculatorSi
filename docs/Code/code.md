# Сайт для приложения Калькуляторр
 ## Код программы

 - код приложения:
 using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Kalkulator
{
        
    public partial class Form1 : Form
        
    {
        double a, b;
        int count;
        bool znak = true;
        public Form1()
        {
            InitializeComponent();
        }

        private void Button13_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 1;//Добавляет 1
        }

        private void Button17_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 0;//Добавляет 0
        }

        private void Button14_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 2;//Добавляет 2
        }

        private void Button15_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 3;//Добавляет 3
        }

        private void Button9_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 4;//Добавляет 4
        }

        private void Button10_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 5;//Добавляет 5
        }

        private void Button11_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 6;//Добавляет 6
        }

        private void Button5_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 7;//Добавляет 7
        }

        private void Button6_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 8;//Добавляет 8
        }

        private void Button7_Click(object sender, EventArgs e)
        {
            textBox1.Text = textBox1.Text + 9;//Добавляет 9
        }

        private void Button4_Click(object sender, EventArgs e)
        {
            a = float.Parse(textBox1.Text);
            textBox1.Clear();//очистка текстбокса
            count = 1;
            label1.Text = a.ToString() + "+";//запись в лейбл знака +
            znak = true;
        }

        private void Button8_Click(object sender, EventArgs e)
        {
            a = float.Parse(textBox1.Text);
            textBox1.Clear();
            count = 2;
            label1.Text = a.ToString() + "-";//запись в лейбл знака -
            znak = true;
        }

        private void Button12_Click(object sender, EventArgs e)
        {
            a = float.Parse(textBox1.Text);
            textBox1.Clear();
            count = 3;
            label1.Text = a.ToString() + "*";//запись в лейбл *
            znak = true;
        }

        private void Button16_Click(object sender, EventArgs e)
        {
            a = float.Parse(textBox1.Text);
            textBox1.Clear();
            count = 4;
            label1.Text = a.ToString() + "/";//записать в лейбл /
            znak = true;
        }

        private void Button19_Click(object sender, EventArgs e)
        {
            calculate();
            label1.Text = "";
        }


        private void Button1_Click(object sender, EventArgs e)
        {
            textBox1.Text = "";
            label1.Text = "";

        }

        private void Button2_Click(object sender, EventArgs e)
        {
            int lenght = textBox1.Text.Length - 1;
            string text = textBox1.Text;
            textBox1.Clear();
            for (int i = 0; 1<lenght; i++)
            {
                textBox1.Text = textBox1.Text + text[i];
            }
        }

        private void Button3_Click(object sender, EventArgs e)
        {
            if (znak == true)
            {
                textBox1.Text = "-" + textBox1.Text;
                znak = false;
            }
            else if (znak == false)
            {
                textBox1.Text = textBox1.Text.Replace("-", "");
                znak = true;
            }
        }

        private void Button20_Click(object sender, EventArgs e)
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Sin(a);
           
            textBox1.Text = b.ToString();
            label1.Text = a.ToString();
            Math.Pow(a, b);




        }

        private void Button21_Click(object sender, EventArgs e)//катангенс
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Tan(a);
            label1.Text = b.ToString();


        }

        private void Button22_Click(object sender, EventArgs e)//экспонента
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Exp(a);
            label1.Text = b.ToString();
        }

        private void Button23_Click(object sender, EventArgs e)//число в квадрат
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Pow(a,2);
            label1.Text = b.ToString();


        }

        private void Button24_Click(object sender, EventArgs e)//косинус
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Cos(a);
           label1.Text = b.ToString();
        }

        private void Button25_Click(object sender, EventArgs e)//модуль числа
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Abs(a);
            label1.Text = b.ToString();
        }
        
        private void Button26_Click(object sender, EventArgs e)//число в степень
           
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Pow(a, 4);
            label1.Text = b.ToString();




        }

        private void Button28_Click(object sender, EventArgs e)//тангенс
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Tan(a);
            label1.Text = b.ToString();
        }

        private void Button29_Click(object sender, EventArgs e)//логорифм
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Log(a);
            label1.Text = b.ToString();
        }

        private void Button30_Click(object sender, EventArgs e)//возвести в квадрат
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Sqrt(a);
            label1.Text = b.ToString();
        }


        private void Button27_Click(object sender, EventArgs e)//разделить на введенное значение
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = 1 / a;
            label1.Text = b.ToString();
        }

        private void Button32_Click(object sender, EventArgs e)//показывает и скрывает доп. функции
        {
            if 
                (button25.Visible == true)
                 
           
            {
                button25.Visible = false;
                button26.Visible = false;
                button22.Visible = false;
                button23.Visible = false;
                button30.Visible = false;
                button27.Visible = false;
                button28.Visible = false;
                button24.Visible = false;
                button20.Visible = false;
                button21.Visible = false;
            }

            else
            {
                button25.Visible = true;
                button26.Visible = true;
                button22.Visible = true;
                button23.Visible = true;
                button30.Visible = true;
                button27.Visible = true;
                button28.Visible = true;
                button24.Visible = true;
                button20.Visible = true;
                button21.Visible = true;
            }
            
        }

        private void TextBox1_KeyPress(object sender, KeyPressEventArgs e)
        {
           
                char ch = e.KeyChar;

                if (!Char.IsDigit(ch) && ch != 8) //Если не цифра (IsDigit)
                {
                    e.Handled = true;//событие не обрабатывается
                }
            if (e.KeyChar == '.')
                e.Handled = ((Control)sender).Text != "0";
        }

        private void Button18_Click(object sender, EventArgs e)
        {

        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        // кнопки 
        private void calculate()
        {
            switch(count)
            {
                case 1:
                    b = a + float.Parse(textBox1.Text);//сложить
                textBox1.Text = b.ToString();
                break;
                case 2:
                    b = a - float.Parse(textBox1.Text);//вычесть
                textBox1.Text = b.ToString();
                break;
                case 3:
                    b = a * float.Parse(textBox1.Text);//умножить
                textBox1.Text = b.ToString();
                break;
                case 4:
                    b = a / float.Parse(textBox1.Text);//разделить
                textBox1.Text = b.ToString();
                break;

                default:
                    break;
            }
        }

    }
}


