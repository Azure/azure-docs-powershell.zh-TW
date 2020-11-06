---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 13ce7a2410f8231d4c5194fbd57d41074d0ca892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445443"
---
# <span data-ttu-id="e1862-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="e1862-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="e1862-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1862-102">SYNOPSIS</span></span>
<span data-ttu-id="e1862-103">取得 Azure SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="e1862-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1862-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1862-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1862-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1862-105">DESCRIPTION</span></span>
<span data-ttu-id="e1862-106">**AzureRmSqlServerServiceObjective** Cmdlet 會取得 Azure SQL 資料庫伺服器可用的服務目標。</span><span class="sxs-lookup"><span data-stu-id="e1862-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="e1862-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1862-107">EXAMPLES</span></span>

### <span data-ttu-id="e1862-108">範例1：取得服務目標</span><span class="sxs-lookup"><span data-stu-id="e1862-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="e1862-109">這個命令會取得名為 Server01 的伺服器和名為 Database01 的資料庫的服務目標。</span><span class="sxs-lookup"><span data-stu-id="e1862-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="e1862-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1862-110">PARAMETERS</span></span>

### <span data-ttu-id="e1862-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1862-111">-DatabaseName</span></span>
<span data-ttu-id="e1862-112">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e1862-112">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1862-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1862-113">-DefaultProfile</span></span>
<span data-ttu-id="e1862-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e1862-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1862-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1862-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1862-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1862-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e1862-117">這個 Cmdlet 會取得指派給此資源之 SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="e1862-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="e1862-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1862-118">-ServerName</span></span>
<span data-ttu-id="e1862-119">指定 SQL 資料庫 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1862-119">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="e1862-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e1862-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="e1862-121">指定 Azure SQL 資料庫伺服器的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="e1862-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="e1862-122">此參數可接受的值為： Basic、S0、S1、S2、P1、P2 及 P3。</span><span class="sxs-lookup"><span data-stu-id="e1862-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1862-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e1862-123">-Confirm</span></span>
<span data-ttu-id="e1862-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1862-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1862-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1862-125">-WhatIf</span></span>
<span data-ttu-id="e1862-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1862-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1862-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1862-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1862-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1862-128">CommonParameters</span></span>
<span data-ttu-id="e1862-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1862-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1862-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1862-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1862-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e1862-131">INPUTS</span></span>

### <span data-ttu-id="e1862-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e1862-132">System.String</span></span>

## <span data-ttu-id="e1862-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e1862-133">OUTPUTS</span></span>

### <span data-ttu-id="e1862-134">AzureSqlServerServiceObjectiveModel 中的 [ServiceObjective]</span><span class="sxs-lookup"><span data-stu-id="e1862-134">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="e1862-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e1862-135">NOTES</span></span>

## <span data-ttu-id="e1862-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1862-136">RELATED LINKS</span></span>

[<span data-ttu-id="e1862-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e1862-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


