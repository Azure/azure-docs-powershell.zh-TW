---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa181dcb171a1842c2b6158078e60b717b33d579
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902169"
---
# <span data-ttu-id="72a2f-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="72a2f-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="72a2f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="72a2f-103">更新 Azure SQL Pool Pool Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="72a2f-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="72a2f-104">語法</span><span class="sxs-lookup"><span data-stu-id="72a2f-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72a2f-105">描述</span><span class="sxs-lookup"><span data-stu-id="72a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="72a2f-106">**Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** Cmdlet 會為 Azure SQL 集中集區建議程式設定自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="72a2f-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="72a2f-107">例子</span><span class="sxs-lookup"><span data-stu-id="72a2f-107">EXAMPLES</span></span>

### <span data-ttu-id="72a2f-108">範例 1：為顧問啟用自動執行</span><span class="sxs-lookup"><span data-stu-id="72a2f-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="72a2f-109">此命令會設定啟用名為 CreateIndex 的顧問的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="72a2f-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="72a2f-110">參數</span><span class="sxs-lookup"><span data-stu-id="72a2f-110">PARAMETERS</span></span>

### <span data-ttu-id="72a2f-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="72a2f-111">-AdvisorName</span></span>
<span data-ttu-id="72a2f-112">指定此 Cmdlet 更新自動執行狀態之建議程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="72a2f-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="72a2f-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="72a2f-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="72a2f-114">指定新值，此 Cmdlet 會更新自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="72a2f-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="72a2f-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="72a2f-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72a2f-116">啟用</span><span class="sxs-lookup"><span data-stu-id="72a2f-116">Enabled</span></span>
- <span data-ttu-id="72a2f-117">禁用</span><span class="sxs-lookup"><span data-stu-id="72a2f-117">Disabled</span></span>
- <span data-ttu-id="72a2f-118">預設</span><span class="sxs-lookup"><span data-stu-id="72a2f-118">Default</span></span>

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

### <span data-ttu-id="72a2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a2f-119">-DefaultProfile</span></span>
<span data-ttu-id="72a2f-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="72a2f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72a2f-121">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="72a2f-121">-ElasticPoolName</span></span>
<span data-ttu-id="72a2f-122">指定泳層資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="72a2f-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="72a2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="72a2f-124">指定包含此集區之伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="72a2f-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="72a2f-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72a2f-125">-ServerName</span></span>
<span data-ttu-id="72a2f-126">指定集中資料庫位於的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="72a2f-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="72a2f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="72a2f-127">-Confirm</span></span>
<span data-ttu-id="72a2f-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="72a2f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72a2f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72a2f-129">-WhatIf</span></span>
<span data-ttu-id="72a2f-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72a2f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72a2f-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72a2f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72a2f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a2f-132">CommonParameters</span></span>
<span data-ttu-id="72a2f-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72a2f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a2f-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72a2f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a2f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="72a2f-135">INPUTS</span></span>

### <span data-ttu-id="72a2f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="72a2f-136">System.String</span></span>

### <span data-ttu-id="72a2f-137">Microsoft.Azure.Commands.sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="72a2f-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="72a2f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="72a2f-138">OUTPUTS</span></span>

### <span data-ttu-id="72a2f-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="72a2f-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="72a2f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="72a2f-140">NOTES</span></span>
* <span data-ttu-id="72a2f-141">關鍵字：azure、azurerm、arm、resource、management、manager、sql、pool pool、mssql、advisor</span><span class="sxs-lookup"><span data-stu-id="72a2f-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="72a2f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="72a2f-142">RELATED LINKS</span></span>

[<span data-ttu-id="72a2f-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="72a2f-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="72a2f-144">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="72a2f-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
