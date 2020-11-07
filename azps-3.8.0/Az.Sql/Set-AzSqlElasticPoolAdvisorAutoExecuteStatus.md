---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798393"
---
# <span data-ttu-id="107fe-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="107fe-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="107fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="107fe-102">SYNOPSIS</span></span>
<span data-ttu-id="107fe-103">更新 Azure SQL 彈性 Pool Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="107fe-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="107fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="107fe-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="107fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="107fe-105">DESCRIPTION</span></span>
<span data-ttu-id="107fe-106">**AzSqlElasticPoolAdvisorAutoExecuteStatus** Cmdlet 會為 Azure SQL 彈性 Pool Advisor 設定自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="107fe-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="107fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="107fe-107">EXAMPLES</span></span>

### <span data-ttu-id="107fe-108">範例1：啟用 advisor 的自動執行</span><span class="sxs-lookup"><span data-stu-id="107fe-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="107fe-109">這個命令會將名為 CreateIndex 的 advisor 的自動執行狀態設為 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="107fe-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="107fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="107fe-110">PARAMETERS</span></span>

### <span data-ttu-id="107fe-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="107fe-111">-AdvisorName</span></span>
<span data-ttu-id="107fe-112">指定此 Cmdlet 更新自動執行狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="107fe-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107fe-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="107fe-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="107fe-114">指定此 Cmdlet 更新自動執行狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="107fe-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="107fe-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="107fe-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="107fe-116">後</span><span class="sxs-lookup"><span data-stu-id="107fe-116">Enabled</span></span>
- <span data-ttu-id="107fe-117">禁止</span><span class="sxs-lookup"><span data-stu-id="107fe-117">Disabled</span></span>
- <span data-ttu-id="107fe-118">設置</span><span class="sxs-lookup"><span data-stu-id="107fe-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107fe-119">-DefaultProfile</span></span>
<span data-ttu-id="107fe-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="107fe-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="107fe-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="107fe-121">-ElasticPoolName</span></span>
<span data-ttu-id="107fe-122">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="107fe-122">Specifies the name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="107fe-124">指定包含此彈性池之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="107fe-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="107fe-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="107fe-125">-ServerName</span></span>
<span data-ttu-id="107fe-126">指定彈性池所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="107fe-126">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107fe-127">-確認</span><span class="sxs-lookup"><span data-stu-id="107fe-127">-Confirm</span></span>
<span data-ttu-id="107fe-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="107fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107fe-129">-WhatIf</span></span>
<span data-ttu-id="107fe-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="107fe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107fe-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="107fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107fe-132">CommonParameters</span></span>
<span data-ttu-id="107fe-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="107fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107fe-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="107fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107fe-135">輸入</span><span class="sxs-lookup"><span data-stu-id="107fe-135">INPUTS</span></span>

### <span data-ttu-id="107fe-136">System.object</span><span class="sxs-lookup"><span data-stu-id="107fe-136">System.String</span></span>

### <span data-ttu-id="107fe-137">AdvisorAutoExecuteStatus 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="107fe-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="107fe-138">輸出</span><span class="sxs-lookup"><span data-stu-id="107fe-138">OUTPUTS</span></span>

### <span data-ttu-id="107fe-139">AzureSqlElasticPoolAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="107fe-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="107fe-140">筆記</span><span class="sxs-lookup"><span data-stu-id="107fe-140">NOTES</span></span>
* <span data-ttu-id="107fe-141">關鍵字： azure、azurerm、arm、資源、管理、管理員、sql、彈性池、mssql、advisor</span><span class="sxs-lookup"><span data-stu-id="107fe-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="107fe-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="107fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="107fe-143">AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="107fe-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="107fe-144">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="107fe-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
