atividade da aula dia 02/04 algoriitmo cadastro salarial
















using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            string nome, rg, cpf, sexo, ec;
            int idade;
            double sb = 0, sl, inss, vt, cm;
            Console.WriteLine("Cadastro Salarial");
            Console.WriteLine("------------------");
            Console.Write("Nome: ");
            nome = Console.ReadLine();
            Console.Write("R.G: ");
            rg = Console.ReadLine();
            Console.Write("C.P.F: ");
            cpf = Console.ReadLine();
            Console.Write("Sexo (M/F): ");
            sexo = Console.ReadLine();
            Console.Write("E.C: ");
            ec = Console.ReadLine();

            Console.WriteLine("-------------------");

            Console.Write("Salário Bruto R$: ");
            sb = double.Parse(Console.ReadLine());
            inss = sb * 0.11;
            Console.WriteLine("Desconto de 11% de Inss R$ {0:0.00}" , inss);
            cm = sb * 0.05;
            Console.WriteLine("Desconto de 5% de Conv.Médico R$ {0:0.00}" , cm);
            vt = sb * 0.06;
            Console.WriteLine("Desconto de 6% de Vale Transporte R$ {0:0.00}" , vt);
            sl = sb - (inss + cm + vt);
            Console.WriteLine("Salário Líquido R$ {0:0.00}" , sl);

            if (sexo == "M" || sexo == "m")
            {
                sl = sl + 1000;

            }

            else if (sexo == "F" || sexo == "f")
            {
                sl = sl + 800;
            }
            else
                Console.WriteLine("Sexo não fornecido");
                Console.WriteLine("Salário Líquido com bônus R$ {0:0.00}" , sl);
            Console.ReadKey();



        }
    }
}
