        for (int i = 0; i < num_1.Length; i++)           //проверка первого числа
        {
            for (int j = 0; j < num_1.Length; j++)
            {
                if (num_1[i] == num_1[j])
                {
                    b++;
                }
            }
            if (b == 1)
            {
                arr3[n] = num_1[i];                  //новый массив без повторяющихся элементов
                n++;
            }
            b = 0;
        }

        for (int i = 0; i < arr3.Length; i++)      //сверяем новый массив со вторым на уникальные элементы
        {
            for (int j = 0; j < num_2.Length; j++)
            {
                if (arr3[i] == num_2[j])
                {
                    a++;
                    break;
                }
            }
            if (a == 0)
            {
                count = arr3[i];        //записываем уникальные значения
            }
            a = 0;
        }
        Console.WriteLine($"Уникально число {count}");
    }
}  
