---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5f0786c180461522d17d2697931f4a9887935f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625657"
---
# <span data-ttu-id="ae6b4-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="ae6b4-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="ae6b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6b4-103">取得 Azure SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae6b4-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae6b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae6b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6b4-106">**AzureRmSqlServerServiceObjective** Cmdlet 會取得 Azure SQL 資料庫伺服器可用的服務目標。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="ae6b4-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae6b4-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6b4-108">範例1：取得服務目標</span><span class="sxs-lookup"><span data-stu-id="ae6b4-108">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="ae6b4-109">這個命令會取得名為 Server01 的伺服器和名為 Database01 的資料庫的服務目標。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="ae6b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="ae6b4-110">PARAMETERS</span></span>

### <span data-ttu-id="ae6b4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae6b4-111">-DatabaseName</span></span>
<span data-ttu-id="ae6b4-112">指定 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-112">Specifies the name of an Azure SQL Database.</span></span>

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

### <span data-ttu-id="ae6b4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6b4-113">-ResourceGroupName</span></span>
<span data-ttu-id="ae6b4-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ae6b4-115">這個 Cmdlet 會取得指派給此資源之 SQL 資料庫伺服器的服務目標。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-115">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="ae6b4-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ae6b4-116">-ServerName</span></span>
<span data-ttu-id="ae6b4-117">指定 SQL 資料庫 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-117">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="ae6b4-118">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ae6b4-118">-ServiceObjectiveName</span></span>
<span data-ttu-id="ae6b4-119">指定 Azure SQL 資料庫伺服器的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-119">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="ae6b4-120">此參數可接受的值為： Basic、S0、S1、S2、P1、P2 及 P3。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-120">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="ae6b4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ae6b4-121">-Confirm</span></span>
<span data-ttu-id="ae6b4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae6b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae6b4-123">-WhatIf</span></span>
<span data-ttu-id="ae6b4-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae6b4-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae6b4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6b4-126">-DefaultProfile</span></span>
<span data-ttu-id="ae6b4-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae6b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6b4-128">CommonParameters</span></span>
<span data-ttu-id="ae6b4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6b4-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae6b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6b4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ae6b4-131">INPUTS</span></span>

## <span data-ttu-id="ae6b4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ae6b4-132">OUTPUTS</span></span>

### <span data-ttu-id="ae6b4-133">AzureSqlServerServiceObjectiveModel 中的 [ServiceObjective]</span><span class="sxs-lookup"><span data-stu-id="ae6b4-133">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="ae6b4-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ae6b4-134">NOTES</span></span>

## <span data-ttu-id="ae6b4-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae6b4-135">RELATED LINKS</span></span>

[<span data-ttu-id="ae6b4-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ae6b4-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


