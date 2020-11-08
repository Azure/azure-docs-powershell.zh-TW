---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970249"
---
# <span data-ttu-id="fb873-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="fb873-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="fb873-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb873-102">SYNOPSIS</span></span>
<span data-ttu-id="fb873-103">工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="fb873-103">link service for workspace</span></span>

## <span data-ttu-id="fb873-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb873-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb873-105">說明</span><span class="sxs-lookup"><span data-stu-id="fb873-105">DESCRIPTION</span></span>
<span data-ttu-id="fb873-106">工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="fb873-106">link service for workspace</span></span>

## <span data-ttu-id="fb873-107">示例</span><span class="sxs-lookup"><span data-stu-id="fb873-107">EXAMPLES</span></span>

### <span data-ttu-id="fb873-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fb873-108">Example 1</span></span>
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

<span data-ttu-id="fb873-109">工作區的連結群集</span><span class="sxs-lookup"><span data-stu-id="fb873-109">link cluster for workspace</span></span>

## <span data-ttu-id="fb873-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb873-110">PARAMETERS</span></span>

### <span data-ttu-id="fb873-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb873-111">-AsJob</span></span>
<span data-ttu-id="fb873-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb873-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb873-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb873-113">-DefaultProfile</span></span>
<span data-ttu-id="fb873-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb873-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb873-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="fb873-115">-LinkedServiceName</span></span>
<span data-ttu-id="fb873-116">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fb873-116">The Workspace name.</span></span>

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

### <span data-ttu-id="fb873-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb873-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb873-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb873-118">The resource group name.</span></span>

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

### <span data-ttu-id="fb873-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb873-119">-ResourceId</span></span>
<span data-ttu-id="fb873-120">將連結至工作區之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb873-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="fb873-121">這應該用於連結需要讀取存取權的資源</span><span class="sxs-lookup"><span data-stu-id="fb873-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="fb873-122">-標記</span><span class="sxs-lookup"><span data-stu-id="fb873-122">-Tags</span></span>
<span data-ttu-id="fb873-123">間.</span><span class="sxs-lookup"><span data-stu-id="fb873-123">Tags.</span></span>

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

### <span data-ttu-id="fb873-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb873-124">-WorkspaceName</span></span>
<span data-ttu-id="fb873-125">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fb873-125">The Workspace name.</span></span>

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

### <span data-ttu-id="fb873-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="fb873-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="fb873-127">將連結至工作區之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb873-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="fb873-128">這應該用於連結需要寫入存取權的資源。</span><span class="sxs-lookup"><span data-stu-id="fb873-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="fb873-129">群集必須具有 [Succeeded] 和有效 keyvault 屬性的 [預配狀態]。</span><span class="sxs-lookup"><span data-stu-id="fb873-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="fb873-130">-確認</span><span class="sxs-lookup"><span data-stu-id="fb873-130">-Confirm</span></span>
<span data-ttu-id="fb873-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb873-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb873-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb873-132">-WhatIf</span></span>
<span data-ttu-id="fb873-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb873-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb873-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb873-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb873-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb873-135">CommonParameters</span></span>
<span data-ttu-id="fb873-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb873-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb873-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb873-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb873-138">輸入</span><span class="sxs-lookup"><span data-stu-id="fb873-138">INPUTS</span></span>

### <span data-ttu-id="fb873-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fb873-139">System.String</span></span>

## <span data-ttu-id="fb873-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fb873-140">OUTPUTS</span></span>

### <span data-ttu-id="fb873-141">PSLinkedService 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="fb873-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="fb873-142">筆記</span><span class="sxs-lookup"><span data-stu-id="fb873-142">NOTES</span></span>

## <span data-ttu-id="fb873-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb873-143">RELATED LINKS</span></span>
