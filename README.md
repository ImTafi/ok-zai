# ok-zai
rita loving
 // Xử lý các sự kiện

                ProcessEvents();

                // Di chuyển Pikachu

                MovePikachu();

                // Kiểm tra xem người chơi có thắng game hay không

                if (IsWin())

                {

                    // Xuất thông báo người chơi thắng game

                    MessageBox.Show(“Bạn đã thắng!”);

                    break;

                }

                // Vẽ lại giao diện người dùng

                gr.Clear(Color.White);

                DrawBoard(gr);

                DrawCells(gr);

                DrawPikachu(gr);

            }

        }

        private static void ProcessEvents()

        {

            // Xử lý các sự kiện bàn phím

            foreach (KeyEventArgs e in Keyboard.GetPressedKeys())

            {

                if (e.KeyCode == Keys.Up)

                {

                    // Di chuyển Pikachu lên

                    Pikachu.Y -= 50;

                }

                else if (e.KeyCode == Keys.Down)

                {

                    // Di chuyển Pikachu xuống

                    Pikachu.Y += 50;

                }

                else if (e.KeyCode == Keys.Left)

                {

                    // Di chuyển Pikachu sang trái
