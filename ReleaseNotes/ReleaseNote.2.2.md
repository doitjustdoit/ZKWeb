﻿### 2.2 Release Note

### Changes

- Refactory Container
	- Make it lock free
	- (Break Change) Use ContainerFactoryData to create instance
	- (Break Change) Remove static ContainerFactoryCache to simplify code
	- (Break Change) Update interface IMultiConstructorResolver
	- (Break Change) Update interface IRegistrator
- Update Web Server
	- (Break Change) Avoid use exception to indicates response end
		- There no guarantee that `HttpManager.CurrentContext.Response.End` will throw an exception
		- To check response is ended, read property `HttpManager.CurrentContext.Response.IsEnded`
- Update Tests
	- Add more assertion type to Assert class
	- Move test cases under ZKWeb and ZKWebStandard project to standalone assembly
	- Improve error message for test failure
	- Add Scenario class for BDD
	- Rewrite some tests in BDD style for readability
- Update Utilities
	- Use thread local random generator in RandomUtils class
	- Use concurrent dictionary and remove rwlock form MemoryCache class
	- Use memory barrier in LazyCache class
	- Remove finalizer from SimpleDisposable class to make it really simple
- Update Project Templates
	- Make project templates support inplace upgrade
	- Make ASP.NET Core startup projects require .NET Core 2.2
- Update ORM
	- Use offical System.Data.SQLite again for NHibernate because the new version supports netstandard
- Update Packages
	- Microsoft.CodeAnalysis.CSharp 2.10.0
	- Newtonsoft.Json 12.0.1
	- System.Drawing.Common 4.5.1
	- Microsoft.DiaSymReader.PortablePdb 1.5.0
	- Microsoft.AspNetCore.Hosting.Abstractions 2.2.0
	- Microsoft.AspNetCore.Http.Abstractions 2.2.0
	- Microsoft.Extensions.DependencyInjection 2.2.0
	- Microsoft.Extensions.DependencyInjection.Abstractions 2.2.0
	- System.Net.Http 4.3.4
	- Dapper.FluentMap 1.7.0
	- Dapper.FluentMap.Dommel 1.6.0
	- Microsoft.Data.Sqlite 2.2.0
	- Npgsql 4.0.3
	- MySqlConnector 0.47.1
	- Microsoft.EntityFrameworkCore 2.2.0
	- Microsoft.EntityFrameworkCore.Design 2.2.0
	- Microsoft.EntityFrameworkCore.InMemory 2.2.0
	- Microsoft.EntityFrameworkCore.Sqlite 2.2.0
	- Microsoft.EntityFrameworkCore.SqlServer 2.2.0
	- Npgsql.EntityFrameworkCore.PostgreSQL 2.1.2
	- Pomelo.EntityFrameworkCore.MySql 2.1.4
	- MongoDB.Driver 2.7.2
	- NHibernate 5.2.0
	- MySql.Data 6.10.8
	- System.Data.SQLite 1.0.109.2