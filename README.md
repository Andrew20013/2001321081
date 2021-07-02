# 2001321081
OOП
using System;

namespace kss
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
    public class Character
    {
        protected int hp, dp, ap;
        public Character(int hp, int dp, int ap)
        {
            this.hp = hp;
            this.dp = dp;
            this.ap = ap;
        }
       public int Attack()
        {
            return this.dp;
        }
        public void Defend(int damage)
        {
            this.hp -= damage;
        }

    }
     class Hero : Character
    {

        public Hero(int hp, int dp, int ap) : base(hp, dp, ap)
        {
            
        }
    }
    }
    
    
    
    
    
    
   ВТОРАТА  И  ТРЕТАТА  ЗАДАЧИ
    
    
   using System;

namespace kss
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
    public class Character
    {
        protected int hp, dp, ap;
        public Character(int hp, int dp, int ap)
        {
            this.hp = hp;
            this.dp = dp;
            this.ap = ap;
        }
        public int Attack()
        {
            return this.dp;
        }
        public void Defend(int damage)
        {
            this.hp -= damage;
        }

    }
     class Hero : Character
    {

        public Hero(int hp, int dp, int ap) : base(hp, dp, ap)
        {
            
        }
       
    }
    class Knight : Character
    {

        public Knight(int hp, int dp, int ap) : base(hp, dp, ap)
        {

        }
        public void Defend(int damage)
        {
            
            var rand = new Random();

            int answer = rand.Next(1, 100);

            if (answer >= 20)
            {
                this.hp -= damage;
            }
        }
    }
    class Ninja : Character
    {

        public Ninja(int hp, int dp, int ap) : base(hp, dp, ap)
        {

        }
        public void Attack(int damage)
        {
            var rand = new Random();

            int answer = rand.Next(1, 100);

            if (answer >= 20)
            {
                this.dp = damage * 3;
            }
        }
    }
}
