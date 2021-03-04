---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0bdfa7ddf86beef3b9db26ff36a1953a1b574fd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917601"
---
# <span data-ttu-id="7da3c-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="7da3c-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="7da3c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7da3c-102">SYNOPSIS</span></span>
<span data-ttu-id="7da3c-103">取得資料庫的 TDE 掃描進度。</span><span class="sxs-lookup"><span data-stu-id="7da3c-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="7da3c-104">語法</span><span class="sxs-lookup"><span data-stu-id="7da3c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7da3c-105">描述</span><span class="sxs-lookup"><span data-stu-id="7da3c-105">DESCRIPTION</span></span>
<span data-ttu-id="7da3c-106">**Get-AzSqlDatabaseTransparentDataEncryptionActivity** Cmdlet 取得透明資料加密 (TDE) Azure SQL 資料庫掃描的進度。</span><span class="sxs-lookup"><span data-stu-id="7da3c-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="7da3c-107">如果沒有進行加密範圍，此 Cmdlet 會返回空白清單。</span><span class="sxs-lookup"><span data-stu-id="7da3c-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="7da3c-108">詳細資訊請參閱 Microsoft 開發人員網路庫中的 Azure SQL Database https://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) 透明資料加密。</span><span class="sxs-lookup"><span data-stu-id="7da3c-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="7da3c-109">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7da3c-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7da3c-110">例子</span><span class="sxs-lookup"><span data-stu-id="7da3c-110">EXAMPLES</span></span>

### <span data-ttu-id="7da3c-111">範例 1：取得資料庫的 TDE 活動</span><span class="sxs-lookup"><span data-stu-id="7da3c-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="7da3c-112">此命令會在伺服器上名為 database01 的資料庫上，獲得 TDE 活動。</span><span class="sxs-lookup"><span data-stu-id="7da3c-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="7da3c-113">參數</span><span class="sxs-lookup"><span data-stu-id="7da3c-113">PARAMETERS</span></span>

### <span data-ttu-id="7da3c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7da3c-114">-DatabaseName</span></span>
<span data-ttu-id="7da3c-115">指定此 Cmdlet 可進行 TDE 加密活動的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7da3c-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="7da3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da3c-116">-DefaultProfile</span></span>
<span data-ttu-id="7da3c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7da3c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7da3c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da3c-118">-ResourceGroupName</span></span>
<span data-ttu-id="7da3c-119">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7da3c-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7da3c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7da3c-120">-ServerName</span></span>
<span data-ttu-id="7da3c-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7da3c-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7da3c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="7da3c-122">-Confirm</span></span>
<span data-ttu-id="7da3c-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7da3c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da3c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da3c-124">-WhatIf</span></span>
<span data-ttu-id="7da3c-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7da3c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da3c-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7da3c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da3c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da3c-127">CommonParameters</span></span>
<span data-ttu-id="7da3c-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7da3c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da3c-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7da3c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da3c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7da3c-130">INPUTS</span></span>

### <span data-ttu-id="7da3c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7da3c-131">System.String</span></span>

## <span data-ttu-id="7da3c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7da3c-132">OUTPUTS</span></span>

### <span data-ttu-id="7da3c-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="7da3c-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="7da3c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7da3c-134">NOTES</span></span>

## <span data-ttu-id="7da3c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7da3c-135">RELATED LINKS</span></span>

[<span data-ttu-id="7da3c-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7da3c-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="7da3c-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7da3c-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


