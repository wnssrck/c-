# c-
sifre
void degisken()
        {

            String[] sembol1 = { "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "R", "S", "T", "U", "V", "Y", "Z" };
            String[] sembol2 = { "0", "1", "2", "3", "4", "5", "6", "7", "8", "9" };
            String[] sembol3 = { "!", "-", "+", "%", "?", "*", "=", "&", "/" };
            Random rdn = new Random();
            int s1, s2, s3, s4;
            s1 = rdn.Next(0, 20);
            s2 = rdn.Next(0, sembol1.Length);
            s3 = rdn.Next(0, sembol2.Length);
            s4 = rdn.Next(0, sembol3.Length);
            label1.Text = sembol1[s2].ToString() + s1.ToString() + sembol2[s3].ToString() + sembol3[s4].ToString();


        }

        private void button1_Click(object sender, EventArgs e)
        {
            if (textBox1.Text == label1.Text)
            {
                menü m = new menü();
                m.Show();
                this.Hide();
            }
            else
            {
                MessageBox.Show("hatalı giriş");
                degisken();


            }
        }

        private void robkont_Load(object sender, EventArgs e)
        {
            degisken();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            degisken();
        }
