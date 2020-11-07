---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959133"
---
# <span data-ttu-id="28126-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="28126-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="28126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28126-102">SYNOPSIS</span></span>
<span data-ttu-id="28126-103">移除作業</span><span class="sxs-lookup"><span data-stu-id="28126-103">Removes a job</span></span>

## <span data-ttu-id="28126-104">句法</span><span class="sxs-lookup"><span data-stu-id="28126-104">SYNTAX</span></span>

### <span data-ttu-id="28126-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28126-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28126-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="28126-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28126-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="28126-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28126-108">說明</span><span class="sxs-lookup"><span data-stu-id="28126-108">DESCRIPTION</span></span>
<span data-ttu-id="28126-109">Remove-AzSqlElasticJob Cmdlet 會移除作業</span><span class="sxs-lookup"><span data-stu-id="28126-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="28126-110">示例</span><span class="sxs-lookup"><span data-stu-id="28126-110">EXAMPLES</span></span>

### <span data-ttu-id="28126-111">範例 1-移除作業</span><span class="sxs-lookup"><span data-stu-id="28126-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="28126-112">移除作業</span><span class="sxs-lookup"><span data-stu-id="28126-112">Removes a job</span></span>

## <span data-ttu-id="28126-113">參數</span><span class="sxs-lookup"><span data-stu-id="28126-113">PARAMETERS</span></span>

### <span data-ttu-id="28126-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="28126-114">-AgentName</span></span>
<span data-ttu-id="28126-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="28126-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28126-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28126-116">-DefaultProfile</span></span>
<span data-ttu-id="28126-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28126-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28126-118">-Force</span><span class="sxs-lookup"><span data-stu-id="28126-118">-Force</span></span>
<span data-ttu-id="28126-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="28126-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28126-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28126-120">-InputObject</span></span>
<span data-ttu-id="28126-121">作業輸入物件</span><span class="sxs-lookup"><span data-stu-id="28126-121">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28126-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="28126-122">-Name</span></span>
<span data-ttu-id="28126-123">作業名稱</span><span class="sxs-lookup"><span data-stu-id="28126-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28126-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28126-124">-ResourceGroupName</span></span>
<span data-ttu-id="28126-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="28126-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28126-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28126-126">-ResourceId</span></span>
<span data-ttu-id="28126-127">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="28126-127">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28126-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28126-128">-ServerName</span></span>
<span data-ttu-id="28126-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="28126-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28126-130">-確認</span><span class="sxs-lookup"><span data-stu-id="28126-130">-Confirm</span></span>
<span data-ttu-id="28126-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28126-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28126-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28126-132">-WhatIf</span></span>
<span data-ttu-id="28126-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28126-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28126-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28126-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28126-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28126-135">CommonParameters</span></span>
<span data-ttu-id="28126-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28126-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28126-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="28126-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28126-138">輸入</span><span class="sxs-lookup"><span data-stu-id="28126-138">INPUTS</span></span>

### <span data-ttu-id="28126-139">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="28126-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="28126-140">輸出</span><span class="sxs-lookup"><span data-stu-id="28126-140">OUTPUTS</span></span>

### <span data-ttu-id="28126-141">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="28126-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="28126-142">筆記</span><span class="sxs-lookup"><span data-stu-id="28126-142">NOTES</span></span>

## <span data-ttu-id="28126-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="28126-143">RELATED LINKS</span></span>
