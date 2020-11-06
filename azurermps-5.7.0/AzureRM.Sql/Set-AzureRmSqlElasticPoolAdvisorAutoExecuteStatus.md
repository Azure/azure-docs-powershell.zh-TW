---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7b4d445ede7bae59431707f3ff6bc587effde21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450427"
---
# <span data-ttu-id="e3b0b-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e3b0b-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="e3b0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b0b-103">更新 Azure SQL 彈性 Pool Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3b0b-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b0b-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b0b-106">**AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** Cmdlet 會為 Azure SQL 彈性 Pool Advisor 設定自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="e3b0b-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b0b-108">範例1：啟用 advisor 的自動執行</span><span class="sxs-lookup"><span data-stu-id="e3b0b-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="e3b0b-109">這個命令會將名為 CreateIndex 的 advisor 的自動執行狀態設為 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="e3b0b-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3b0b-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b0b-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e3b0b-111">-AdvisorName</span></span>
<span data-ttu-id="e3b0b-112">指定此 Cmdlet 更新自動執行狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e3b0b-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="e3b0b-114">指定此 Cmdlet 更新自動執行狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="e3b0b-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e3b0b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3b0b-116">後</span><span class="sxs-lookup"><span data-stu-id="e3b0b-116">Enabled</span></span>
- <span data-ttu-id="e3b0b-117">禁止</span><span class="sxs-lookup"><span data-stu-id="e3b0b-117">Disabled</span></span>
- <span data-ttu-id="e3b0b-118">設置</span><span class="sxs-lookup"><span data-stu-id="e3b0b-118">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b0b-119">-DefaultProfile</span></span>
<span data-ttu-id="e3b0b-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e3b0b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e3b0b-121">-ElasticPoolName</span></span>
<span data-ttu-id="e3b0b-122">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-122">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b0b-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3b0b-124">指定包含此彈性池之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e3b0b-125">-ServerName</span></span>
<span data-ttu-id="e3b0b-126">指定彈性池所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-126">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e3b0b-127">-Confirm</span></span>
<span data-ttu-id="e3b0b-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b0b-129">-WhatIf</span></span>
<span data-ttu-id="e3b0b-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b0b-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b0b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b0b-132">CommonParameters</span></span>
<span data-ttu-id="e3b0b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b0b-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b0b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e3b0b-135">INPUTS</span></span>

### <span data-ttu-id="e3b0b-136">所有</span><span class="sxs-lookup"><span data-stu-id="e3b0b-136">None</span></span>
<span data-ttu-id="e3b0b-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e3b0b-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3b0b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e3b0b-138">OUTPUTS</span></span>

### <span data-ttu-id="e3b0b-139">AzureSqlElasticPoolAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="e3b0b-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="e3b0b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e3b0b-140">NOTES</span></span>
* <span data-ttu-id="e3b0b-141">關鍵字： azure、azurerm、arm、資源、管理、管理員、sql、彈性池、mssql、advisor</span><span class="sxs-lookup"><span data-stu-id="e3b0b-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="e3b0b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3b0b-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3b0b-143">AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e3b0b-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="e3b0b-144">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e3b0b-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
