# stm32-template

Project template for STM32 using [stm-idf.](https://github.com/phonght32/stm-idf)

### 1. How to install

```
git clone https://github.com/phonght32/stm32-template
cd stm32-template
git submodule update --init --recuresive
```

### 2. Configuring the project

- STM-IDF search in many folders: (project_path)/main, (project_path)/components to get **component.mk** file. Any folder contains component.mk file will become source directory, header directory in include folder by default.
- To configure source path and header path, modify **SOURCE_PATHS** and **INCLUDE_PATHS** in component.mk file.
- To add user components, modify **EXTRA_COMPONENT_DIRS** in Makefile.

### 3. Use STM-IDF

Visit this [link](https://github.com/phonght32/stm-idf) to get instruction to use stm-idf.

### 4. Build project

```
make build all
```

### 5. Flash to target

Flash over USART:

```
make flash_usart
```

Flash over ST-LinkV2:

```
make flash_stlink
```

### 6. View log output

```
make monitor
```