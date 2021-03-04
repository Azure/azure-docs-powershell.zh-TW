---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8e511fa2e83866ac1a0119c410369f7f13705f14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915201"
---
# <span data-ttu-id="5c713-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5c713-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="5c713-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c713-102">SYNOPSIS</span></span>
<span data-ttu-id="5c713-103">修改資料庫的 TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c713-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="5c713-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c713-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c713-105">描述</span><span class="sxs-lookup"><span data-stu-id="5c713-105">DESCRIPTION</span></span>
<span data-ttu-id="5c713-106">**Set-AzSqlDatabaseTransparentDataEncryption** Cmdlet 會修改 Azure SQL 資料庫的透明資料加密 (TDE) 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c713-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="5c713-107">詳細資訊請參閱 Microsoft 開發人員網路庫中的 Azure SQL Database https://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) 透明資料加密。</span><span class="sxs-lookup"><span data-stu-id="5c713-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="5c713-108">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c713-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5c713-109">例子</span><span class="sxs-lookup"><span data-stu-id="5c713-109">EXAMPLES</span></span>

### <span data-ttu-id="5c713-110">範例 1：啟用資料庫的 TDE</span><span class="sxs-lookup"><span data-stu-id="5c713-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="5c713-111">此命令會針對名為 Server01 的伺服器上名為 Database01 的資料庫啟用 TDE。</span><span class="sxs-lookup"><span data-stu-id="5c713-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="5c713-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c713-112">PARAMETERS</span></span>

### <span data-ttu-id="5c713-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c713-113">-DatabaseName</span></span>
<span data-ttu-id="5c713-114">指定此 Cmdlet 修改的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5c713-114">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c713-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c713-115">-DefaultProfile</span></span>
<span data-ttu-id="5c713-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5c713-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c713-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c713-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c713-118">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5c713-118">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c713-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c713-119">-ServerName</span></span>
<span data-ttu-id="5c713-120">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5c713-120">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c713-121">-State</span><span class="sxs-lookup"><span data-stu-id="5c713-121">-State</span></span>
<span data-ttu-id="5c713-122">指定 TDE 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="5c713-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="5c713-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5c713-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c713-124">啟用</span><span class="sxs-lookup"><span data-stu-id="5c713-124">Enabled</span></span> 
- <span data-ttu-id="5c713-125">禁用</span><span class="sxs-lookup"><span data-stu-id="5c713-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c713-126">-確認</span><span class="sxs-lookup"><span data-stu-id="5c713-126">-Confirm</span></span>
<span data-ttu-id="5c713-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c713-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c713-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c713-128">-WhatIf</span></span>
<span data-ttu-id="5c713-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c713-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c713-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c713-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c713-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c713-131">CommonParameters</span></span>
<span data-ttu-id="5c713-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c713-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c713-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c713-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c713-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5c713-134">INPUTS</span></span>

### <span data-ttu-id="5c713-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="5c713-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="5c713-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5c713-136">System.String</span></span>

## <span data-ttu-id="5c713-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5c713-137">OUTPUTS</span></span>

### <span data-ttu-id="5c713-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="5c713-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="5c713-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5c713-139">NOTES</span></span>

## <span data-ttu-id="5c713-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c713-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c713-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5c713-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="5c713-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="5c713-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="5c713-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="5c713-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


