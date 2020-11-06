---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ec35e0ebd0f674c66b7708289c33253b28219433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454500"
---
# <span data-ttu-id="3ea1c-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3ea1c-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="3ea1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ea1c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea1c-103">修改資料庫的 TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ea1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ea1c-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ea1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ea1c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea1c-106">**AzureRmSqlDatabaseTransparentDataEncryption** Cmdlet 會修改) Azure SQL 資料庫的透明資料加密 (TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="3ea1c-107">如需詳細資訊，請參閱 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 開發人員網路文件庫中與 Azure SQL Database (的透明資料加密。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="3ea1c-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3ea1c-109">示例</span><span class="sxs-lookup"><span data-stu-id="3ea1c-109">EXAMPLES</span></span>

### <span data-ttu-id="3ea1c-110">範例1：為資料庫啟用 TDE</span><span class="sxs-lookup"><span data-stu-id="3ea1c-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="3ea1c-111">這個命令會針對名為 Server01 的伺服器上名為 Database01 的資料庫啟用 TDE。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="3ea1c-112">參數</span><span class="sxs-lookup"><span data-stu-id="3ea1c-112">PARAMETERS</span></span>

### <span data-ttu-id="3ea1c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ea1c-113">-DatabaseName</span></span>
<span data-ttu-id="3ea1c-114">指定此 Cmdlet 所修改之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3ea1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea1c-115">-DefaultProfile</span></span>
<span data-ttu-id="3ea1c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3ea1c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ea1c-118">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3ea1c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ea1c-119">-ServerName</span></span>
<span data-ttu-id="3ea1c-120">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3ea1c-121">-State</span><span class="sxs-lookup"><span data-stu-id="3ea1c-121">-State</span></span>
<span data-ttu-id="3ea1c-122">指定 TDE 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="3ea1c-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3ea1c-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ea1c-124">後</span><span class="sxs-lookup"><span data-stu-id="3ea1c-124">Enabled</span></span> 
- <span data-ttu-id="3ea1c-125">禁止</span><span class="sxs-lookup"><span data-stu-id="3ea1c-125">Disabled</span></span>

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

### <span data-ttu-id="3ea1c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3ea1c-126">-Confirm</span></span>
<span data-ttu-id="3ea1c-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea1c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea1c-128">-WhatIf</span></span>
<span data-ttu-id="3ea1c-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ea1c-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea1c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea1c-131">CommonParameters</span></span>
<span data-ttu-id="3ea1c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea1c-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ea1c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea1c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3ea1c-134">INPUTS</span></span>

### <span data-ttu-id="3ea1c-135">TransparentDataEncryptionStateType 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="3ea1c-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="3ea1c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="3ea1c-136">System.String</span></span>

## <span data-ttu-id="3ea1c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3ea1c-137">OUTPUTS</span></span>

### <span data-ttu-id="3ea1c-138">AzureSqlDatabaseTransparentDataEncryptionModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="3ea1c-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="3ea1c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3ea1c-139">NOTES</span></span>

## <span data-ttu-id="3ea1c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ea1c-140">RELATED LINKS</span></span>

[<span data-ttu-id="3ea1c-141">AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3ea1c-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="3ea1c-142">AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="3ea1c-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="3ea1c-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3ea1c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


