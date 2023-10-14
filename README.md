# Estrutura-Multi-Tenancy

Foi díficil encontrar um tutorial capaz de me dar o que eu queria, mas, contudo encontrei, este é uma estrutura Mult-Database, mais da para configurar para que ela seja single-Database.
Utilizei o:

``
php artisan tinker
``
para poder criar os tenant de forma mais rápida, apenas para testar! Veja asseguir como fazer:

# CRINADO O PRIMEIRO

lebrando que também tens de fazer a migrations, então execute:

``
php artisan migrate
``
depois, temos que criar o tenancy, podes usar o `` tinker ``, rode desta forma:

```sh
php artisan tinker
```
Depois de rodar o que temos acima, coloque o temos abaixo para criar um tenant

```sh
 $tenant = \App\Models\Tenant::create(['tenant_id' => 'astros', 'plan' => 'Free']);
```

depois de criar um tenant é necessario criar o seu domain, então rode o

```sh
$tenant->domains()->create(['domain' => 'astros.localhost']);
```

com isso você poderá a colocar a rodar o server utilizando o:

```sh
php artisan serve
```

# VEJA COMO FICA
![Imagem](https://raw.githubusercontent.com/Mario-Coxe/Estrutura-Multi-Tenancy/main/image/c2.png)

# DOMAIN
![Imagem](https://raw.githubusercontent.com/Mario-Coxe/Estrutura-Multi-Tenancy/main/image/d2.png)


# A ideia é a mesma, veja outros tenant que eu criei:

# TENAT
![Imagem](https://raw.githubusercontent.com/Mario-Coxe/Estrutura-Multi-Tenancy/main/image/c1.png)
![Imagem](https://raw.githubusercontent.com/Mario-Coxe/Estrutura-Multi-Tenancy/main/image/c3.png)

# DOMAIN
![Imagem](https://raw.githubusercontent.com/Mario-Coxe/Estrutura-Multi-Tenancy/main/image/d1.png)
![Imagem](https://raw.githubusercontent.com/Mario-Coxe/Estrutura-Multi-Tenancy/main/image/d3.png)
