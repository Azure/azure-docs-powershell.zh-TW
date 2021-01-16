---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285699"
---
# <span data-ttu-id="94097-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="94097-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="94097-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94097-102">SYNOPSIS</span></span>
<span data-ttu-id="94097-103">取得資料庫 TDE 掃描的進度。</span><span class="sxs-lookup"><span data-stu-id="94097-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="94097-104">句法</span><span class="sxs-lookup"><span data-stu-id="94097-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94097-105">說明</span><span class="sxs-lookup"><span data-stu-id="94097-105">DESCRIPTION</span></span>
<span data-ttu-id="94097-106">**AzSqlDatabaseTransparentDataEncryptionActivity** Cmdlet 會取得透明資料加密的進度， (TDE) 掃描 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="94097-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="94097-107">如果沒有執行加密範圍，這個 Cmdlet 會傳回空白清單。</span><span class="sxs-lookup"><span data-stu-id="94097-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="94097-108">如需詳細資訊，請參閱 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 開發人員網路文件庫中與 Azure SQL Database (的透明資料加密。</span><span class="sxs-lookup"><span data-stu-id="94097-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="94097-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94097-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="94097-110">示例</span><span class="sxs-lookup"><span data-stu-id="94097-110">EXAMPLES</span></span>

### <span data-ttu-id="94097-111">範例1：取得資料庫的 TDE 活動</span><span class="sxs-lookup"><span data-stu-id="94097-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="94097-112">這個命令會取得名為 server01 之伺服器上名為 database01 之資料庫的 TDE 活動。</span><span class="sxs-lookup"><span data-stu-id="94097-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="94097-113">參數</span><span class="sxs-lookup"><span data-stu-id="94097-113">PARAMETERS</span></span>

### <span data-ttu-id="94097-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94097-114">-DatabaseName</span></span>
<span data-ttu-id="94097-115">指定此 Cmdlet 取得 TDE 加密活動之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="94097-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="94097-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94097-116">-DefaultProfile</span></span>
<span data-ttu-id="94097-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="94097-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94097-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94097-118">-ResourceGroupName</span></span>
<span data-ttu-id="94097-119">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94097-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="94097-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94097-120">-ServerName</span></span>
<span data-ttu-id="94097-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="94097-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="94097-122">-確認</span><span class="sxs-lookup"><span data-stu-id="94097-122">-Confirm</span></span>
<span data-ttu-id="94097-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94097-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94097-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94097-124">-WhatIf</span></span>
<span data-ttu-id="94097-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94097-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94097-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94097-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94097-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94097-127">CommonParameters</span></span>
<span data-ttu-id="94097-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94097-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94097-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="94097-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94097-130">輸入</span><span class="sxs-lookup"><span data-stu-id="94097-130">INPUTS</span></span>

### <span data-ttu-id="94097-131">System.object</span><span class="sxs-lookup"><span data-stu-id="94097-131">System.String</span></span>

## <span data-ttu-id="94097-132">輸出</span><span class="sxs-lookup"><span data-stu-id="94097-132">OUTPUTS</span></span>

### <span data-ttu-id="94097-133">AzureSqlDatabaseTransparentDataEncryptionActivityModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="94097-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="94097-134">筆記</span><span class="sxs-lookup"><span data-stu-id="94097-134">NOTES</span></span>

## <span data-ttu-id="94097-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="94097-135">RELATED LINKS</span></span>

[<span data-ttu-id="94097-136">AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="94097-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="94097-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="94097-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


