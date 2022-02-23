- Use Python 3.6
- Install requirements
- Copy notebook and run it

- Print/Save to PDF

# Results:

## `torch.nn.LayerNorm`

| LayerNorm (train mode)                        | Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz | AMD EPYC 7V12 64-Core Processor | Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz | Tesla V100-PCIE-16GB, 460.27.04 | Tesla T4, 460.27.04 |
| --------------------------------------------- | ----------------------------------------- | ------------------------------- | ---------------------------------------- | ------------------------------- | ------------------- |
| **Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz** | Exact                                     | -                               | -                                        | -                               | -                   |
| **AMD EPYC 7V12 64-Core Processor**           | Exact                                     | Exact                           | -                                        | -                               | -                   |
| **Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz**  | Exact                                     | Exact                           | Exact                                    | -                               | -                   |
| **Tesla V100-PCIE-16GB, 460.27.04**           | **Close enough**                          | **Close enough**                | **Close enough**                         | Exact                           | -                   |
| **Tesla T4, 460.27.04**                       | **Close enough**                          | **Close enough**                | **Close enough**                         | Exact                           | Exact               |

## `torch.nn.Dropout`

| Dropout (train mode)                          | Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz | AMD EPYC 7V12 64-Core Processor | Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz | Tesla V100-PCIE-16GB, 460.27.04 | Tesla T4, 460.27.04 |
| --------------------------------------------- | ----------------------------------------- | ------------------------------- | ---------------------------------------- | ------------------------------- | ------------------- |
| **Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz** | Exact                                     | -                               | -                                        | -                               | -                   |
| **AMD EPYC 7V12 64-Core Processor**           | **Different**                             | Exact                           | -                                        | -                               | -                   |
| **Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz**  | Exact                                     | **Different**                   | Exact                                    | -                               | -                   |
| **Tesla V100-PCIE-16GB, 460.27.04**           | **Different**                             | **Different**                   | **Different**                            | Exact                           | -                   |
| **Tesla T4, 460.27.04**                       | **Different**                             | **Different**                   | **Different**                            | **Different**                   | Exact               |
