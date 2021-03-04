---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 141723a0e920f18aed9808ed3c5f205534c48185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911546"
---
# <span data-ttu-id="1d10f-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="1d10f-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="1d10f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1d10f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d10f-103">工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="1d10f-103">link service for workspace</span></span>

## <span data-ttu-id="1d10f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1d10f-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d10f-105">描述</span><span class="sxs-lookup"><span data-stu-id="1d10f-105">DESCRIPTION</span></span>
<span data-ttu-id="1d10f-106">工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="1d10f-106">link service for workspace</span></span>

## <span data-ttu-id="1d10f-107">例子</span><span class="sxs-lookup"><span data-stu-id="1d10f-107">EXAMPLES</span></span>

### <span data-ttu-id="1d10f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1d10f-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="1d10f-109">工作區的連結組</span><span class="sxs-lookup"><span data-stu-id="1d10f-109">link cluster for workspace</span></span>

## <span data-ttu-id="1d10f-110">參數</span><span class="sxs-lookup"><span data-stu-id="1d10f-110">PARAMETERS</span></span>

### <span data-ttu-id="1d10f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d10f-111">-AsJob</span></span>
<span data-ttu-id="1d10f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d10f-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d10f-113">-DefaultProfile</span></span>
<span data-ttu-id="1d10f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d10f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="1d10f-115">-LinkedServiceName</span></span>
<span data-ttu-id="1d10f-116">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="1d10f-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d10f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d10f-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1d10f-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d10f-119">-ResourceId</span></span>
<span data-ttu-id="1d10f-120">將連結至工作區之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d10f-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="1d10f-121">這應該用於連結需要讀取存取的資源</span><span class="sxs-lookup"><span data-stu-id="1d10f-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-122">-標記</span><span class="sxs-lookup"><span data-stu-id="1d10f-122">-Tags</span></span>
<span data-ttu-id="1d10f-123">標籤。</span><span class="sxs-lookup"><span data-stu-id="1d10f-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1d10f-124">-WorkspaceName</span></span>
<span data-ttu-id="1d10f-125">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="1d10f-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="1d10f-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="1d10f-127">將連結至工作區之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d10f-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="1d10f-128">這應該用於連結需要寫入存取的資源。</span><span class="sxs-lookup"><span data-stu-id="1d10f-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="1d10f-129">組組必須具有布備狀態「已成功」和有效的 Keyvault 屬性。</span><span class="sxs-lookup"><span data-stu-id="1d10f-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1d10f-130">-Confirm</span></span>
<span data-ttu-id="1d10f-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1d10f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d10f-132">-WhatIf</span></span>
<span data-ttu-id="1d10f-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d10f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d10f-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d10f-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d10f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d10f-135">CommonParameters</span></span>
<span data-ttu-id="1d10f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1d10f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d10f-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d10f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d10f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1d10f-138">INPUTS</span></span>

### <span data-ttu-id="1d10f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1d10f-139">System.String</span></span>

## <span data-ttu-id="1d10f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1d10f-140">OUTPUTS</span></span>

### <span data-ttu-id="1d10f-141">Microsoft.Azure.Commands.OperationalInsights.models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="1d10f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="1d10f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1d10f-142">NOTES</span></span>

## <span data-ttu-id="1d10f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d10f-143">RELATED LINKS</span></span>
