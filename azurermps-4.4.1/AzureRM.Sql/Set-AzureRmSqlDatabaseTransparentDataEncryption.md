---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ca3ee787e577eabc9e889cbb471fcf3a00a4736c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623840"
---
# <span data-ttu-id="167b8-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="167b8-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="167b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="167b8-102">SYNOPSIS</span></span>
<span data-ttu-id="167b8-103">修改資料庫的 TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="167b8-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="167b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="167b8-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="167b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="167b8-105">DESCRIPTION</span></span>
<span data-ttu-id="167b8-106">**AzureRmSqlDatabaseTransparentDataEncryption** Cmdlet 會修改) Azure SQL 資料庫的透明資料加密 (TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="167b8-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="167b8-107">如需詳細資訊，請參閱 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 開發人員網路文件庫中與 Azure SQL Database (的透明資料加密。</span><span class="sxs-lookup"><span data-stu-id="167b8-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="167b8-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="167b8-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="167b8-109">示例</span><span class="sxs-lookup"><span data-stu-id="167b8-109">EXAMPLES</span></span>

### <span data-ttu-id="167b8-110">範例1：為資料庫啟用 TDE</span><span class="sxs-lookup"><span data-stu-id="167b8-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="167b8-111">這個命令會針對名為 Server01 的伺服器上名為 Database01 的資料庫啟用 TDE。</span><span class="sxs-lookup"><span data-stu-id="167b8-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="167b8-112">參數</span><span class="sxs-lookup"><span data-stu-id="167b8-112">PARAMETERS</span></span>

### <span data-ttu-id="167b8-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="167b8-113">-DatabaseName</span></span>
<span data-ttu-id="167b8-114">指定此 Cmdlet 所修改之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="167b8-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="167b8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167b8-115">-ResourceGroupName</span></span>
<span data-ttu-id="167b8-116">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="167b8-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="167b8-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="167b8-117">-ServerName</span></span>
<span data-ttu-id="167b8-118">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="167b8-118">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="167b8-119">-State</span><span class="sxs-lookup"><span data-stu-id="167b8-119">-State</span></span>
<span data-ttu-id="167b8-120">指定 TDE 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="167b8-120">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="167b8-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="167b8-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="167b8-122">後</span><span class="sxs-lookup"><span data-stu-id="167b8-122">Enabled</span></span> 
- <span data-ttu-id="167b8-123">禁止</span><span class="sxs-lookup"><span data-stu-id="167b8-123">Disabled</span></span>

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

### <span data-ttu-id="167b8-124">-確認</span><span class="sxs-lookup"><span data-stu-id="167b8-124">-Confirm</span></span>
<span data-ttu-id="167b8-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="167b8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="167b8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="167b8-126">-WhatIf</span></span>
<span data-ttu-id="167b8-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="167b8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="167b8-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="167b8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="167b8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167b8-129">-DefaultProfile</span></span>
<span data-ttu-id="167b8-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="167b8-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="167b8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167b8-131">CommonParameters</span></span>
<span data-ttu-id="167b8-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="167b8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167b8-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="167b8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167b8-134">輸入</span><span class="sxs-lookup"><span data-stu-id="167b8-134">INPUTS</span></span>

## <span data-ttu-id="167b8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="167b8-135">OUTPUTS</span></span>

### <span data-ttu-id="167b8-136">AzureSqlDatabaseTransparentDataEncryptionModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="167b8-136">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="167b8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="167b8-137">NOTES</span></span>

## <span data-ttu-id="167b8-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="167b8-138">RELATED LINKS</span></span>

[<span data-ttu-id="167b8-139">AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="167b8-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="167b8-140">AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="167b8-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="167b8-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="167b8-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


