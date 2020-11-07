---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: 94e5525b1d783eea794b7e98e76e809b9d7e0f3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957065"
---
# <span data-ttu-id="9fe9d-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="9fe9d-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="9fe9d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fe9d-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe9d-103">繼續暫停的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="9fe9d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fe9d-104">SYNTAX</span></span>

### <span data-ttu-id="9fe9d-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="9fe9d-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe9d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fe9d-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe9d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9fe9d-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe9d-108">說明</span><span class="sxs-lookup"><span data-stu-id="9fe9d-108">DESCRIPTION</span></span>
<span data-ttu-id="9fe9d-109">繼續暫停的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="9fe9d-110">示例</span><span class="sxs-lookup"><span data-stu-id="9fe9d-110">EXAMPLES</span></span>

### <span data-ttu-id="9fe9d-111">範例 1-依名稱繼續封存的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="9fe9d-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="9fe9d-112">上述命令會繼續在資源群組 "testrg" 中找到名為 "mykustocluster" 的暫停 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="9fe9d-113">範例 2-透過管道來繼續暫停的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="9fe9d-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="9fe9d-114">上述命令會在使用 Cmdlet 的資源群組 "testrg" 中，找到名為 "mykustocluster" 的 Kusto 群集，然後將 `Get-AzKustoCluster` 結果指令到 `Resume-AzKustoCluster` 其中以繼續。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="9fe9d-115">參數</span><span class="sxs-lookup"><span data-stu-id="9fe9d-115">PARAMETERS</span></span>

### <span data-ttu-id="9fe9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe9d-116">-DefaultProfile</span></span>
<span data-ttu-id="9fe9d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe9d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fe9d-118">-InputObject</span></span>
<span data-ttu-id="9fe9d-119">Kusto [群集物件]。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fe9d-120">-Name</span></span>
<span data-ttu-id="9fe9d-121">要繼續的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-121">Name of cluster to be resume.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fe9d-122">-PassThru</span></span>
<span data-ttu-id="9fe9d-123">傳回指定的群集是否已成功繼續。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-123">Return whether the specified cluster was successfully resumed or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9fe9d-125">群集存在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fe9d-126">-ResourceId</span></span>
<span data-ttu-id="9fe9d-127">Kusto [群集 ResourceID]。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="9fe9d-128">-Confirm</span></span>
<span data-ttu-id="9fe9d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe9d-130">-WhatIf</span></span>
<span data-ttu-id="9fe9d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe9d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe9d-133">CommonParameters</span></span>
<span data-ttu-id="9fe9d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe9d-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe9d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="9fe9d-136">INPUTS</span></span>

### <span data-ttu-id="9fe9d-137">System.object</span><span class="sxs-lookup"><span data-stu-id="9fe9d-137">System.String</span></span>

### <span data-ttu-id="9fe9d-138">PSKustoCluster 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="9fe9d-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="9fe9d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9fe9d-139">OUTPUTS</span></span>

### <span data-ttu-id="9fe9d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="9fe9d-140">System.Boolean</span></span>

## <span data-ttu-id="9fe9d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9fe9d-141">NOTES</span></span>

## <span data-ttu-id="9fe9d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fe9d-142">RELATED LINKS</span></span>
