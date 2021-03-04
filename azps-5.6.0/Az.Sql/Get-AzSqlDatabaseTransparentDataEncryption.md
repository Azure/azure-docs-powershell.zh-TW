---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 1b045b97df1dbbc704f3288cf2075caa16f30bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917602"
---
# <span data-ttu-id="57455-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="57455-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="57455-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57455-102">SYNOPSIS</span></span>
<span data-ttu-id="57455-103">獲得資料庫的 TDE 狀態。</span><span class="sxs-lookup"><span data-stu-id="57455-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="57455-104">語法</span><span class="sxs-lookup"><span data-stu-id="57455-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57455-105">描述</span><span class="sxs-lookup"><span data-stu-id="57455-105">DESCRIPTION</span></span>
<span data-ttu-id="57455-106">**Get-AzSqlDatabaseTransparentDataEncryption** Cmdlet 會取得 Azure SQL 資料庫的透明資料加密 (TDE) 狀態。</span><span class="sxs-lookup"><span data-stu-id="57455-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="57455-107">詳細資訊請參閱 Microsoft 開發人員網路庫中的 Azure SQL Database https://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) 透明資料加密。</span><span class="sxs-lookup"><span data-stu-id="57455-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="57455-108">此 Cmdlet 會獲得 TDE 的目前狀態，但加密和解密可能是長時間執行的操作。</span><span class="sxs-lookup"><span data-stu-id="57455-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="57455-109">若要查看加密掃描進度，請執行 Get-AzSqlDatabaseTransparentDataEncryptionActivity Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57455-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="57455-110">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57455-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="57455-111">例子</span><span class="sxs-lookup"><span data-stu-id="57455-111">EXAMPLES</span></span>

### <span data-ttu-id="57455-112">範例 1：取得資料庫的 TDE 狀態</span><span class="sxs-lookup"><span data-stu-id="57455-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="57455-113">此命令會在伺服器上名為 Database01 的資料庫，獲得 TDE 的狀態。</span><span class="sxs-lookup"><span data-stu-id="57455-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="57455-114">參數</span><span class="sxs-lookup"><span data-stu-id="57455-114">PARAMETERS</span></span>

### <span data-ttu-id="57455-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57455-115">-DatabaseName</span></span>
<span data-ttu-id="57455-116">指定此 Cmdlet 會獲得 TDE 狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="57455-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="57455-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57455-117">-DefaultProfile</span></span>
<span data-ttu-id="57455-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="57455-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57455-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57455-119">-ResourceGroupName</span></span>
<span data-ttu-id="57455-120">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="57455-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="57455-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57455-121">-ServerName</span></span>
<span data-ttu-id="57455-122">指定主管此 Cmdlet 之資料庫的伺服器名稱，此 Cmdlet 會獲得 TDE 狀態。</span><span class="sxs-lookup"><span data-stu-id="57455-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="57455-123">-確認</span><span class="sxs-lookup"><span data-stu-id="57455-123">-Confirm</span></span>
<span data-ttu-id="57455-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="57455-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57455-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57455-125">-WhatIf</span></span>
<span data-ttu-id="57455-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57455-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57455-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57455-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57455-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57455-128">CommonParameters</span></span>
<span data-ttu-id="57455-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57455-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57455-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57455-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57455-131">輸入</span><span class="sxs-lookup"><span data-stu-id="57455-131">INPUTS</span></span>

### <span data-ttu-id="57455-132">System.String</span><span class="sxs-lookup"><span data-stu-id="57455-132">System.String</span></span>

## <span data-ttu-id="57455-133">輸出</span><span class="sxs-lookup"><span data-stu-id="57455-133">OUTPUTS</span></span>

### <span data-ttu-id="57455-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="57455-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="57455-135">筆記</span><span class="sxs-lookup"><span data-stu-id="57455-135">NOTES</span></span>

## <span data-ttu-id="57455-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="57455-136">RELATED LINKS</span></span>

[<span data-ttu-id="57455-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="57455-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="57455-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="57455-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
