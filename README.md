# Estudo de comandos NASM
## Primeros comandos

* Progama hello worl
```Assembly
global _start

    section .text
    _start:
        mov rax,1               ;prepara o sistema para fazer a escrita de um texto
        mov rdi,1               ;prepara a saída do texto na tela
        mov rsi,message        ;imprimir a mensagem na tela
        mov rdx,13              ;quantidade de caracteres 
        syscall                 ;chama o sistema para preparar a saída
        mov rax,60              ;chamada para saída do sistema
        xor rdi,rdi             ;executar a saída do sistema
        syscall                 ;invocar o sistema operacional para fechar 



        section .data
        message:db 'Hello World',10        ; o valor 10 representa a quebra de linha 



```