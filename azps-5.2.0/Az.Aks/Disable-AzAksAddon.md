---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278941"
---
# <span data-ttu-id="04d3a-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="04d3a-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="04d3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="04d3a-103">停用 aks 的 addons。</span><span class="sxs-lookup"><span data-stu-id="04d3a-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="04d3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="04d3a-104">SYNTAX</span></span>

### <span data-ttu-id="04d3a-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="04d3a-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04d3a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04d3a-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d3a-107">說明</span><span class="sxs-lookup"><span data-stu-id="04d3a-107">DESCRIPTION</span></span>
<span data-ttu-id="04d3a-108">停用 aks 的 addons。</span><span class="sxs-lookup"><span data-stu-id="04d3a-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="04d3a-109">示例</span><span class="sxs-lookup"><span data-stu-id="04d3a-109">EXAMPLES</span></span>

### <span data-ttu-id="04d3a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="04d3a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="04d3a-111">停用 [addons]、[] `HttpApplicationRouting` `Monitoring` 及 [aks] `AzurePolicy` `VirtualNode` `KubeDashboard` 。</span><span class="sxs-lookup"><span data-stu-id="04d3a-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="04d3a-112">參數</span><span class="sxs-lookup"><span data-stu-id="04d3a-112">PARAMETERS</span></span>

### <span data-ttu-id="04d3a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="04d3a-113">-ClusterName</span></span>
<span data-ttu-id="04d3a-114">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="04d3a-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d3a-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="04d3a-115">-ClusterObject</span></span>
<span data-ttu-id="04d3a-116">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="04d3a-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04d3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d3a-117">-DefaultProfile</span></span>
<span data-ttu-id="04d3a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04d3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04d3a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="04d3a-119">-Name</span></span>
<span data-ttu-id="04d3a-120">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="04d3a-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="04d3a-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="04d3a-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d3a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="04d3a-123">-Confirm</span></span>
<span data-ttu-id="04d3a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04d3a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d3a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d3a-125">-WhatIf</span></span>
<span data-ttu-id="04d3a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04d3a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d3a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04d3a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d3a-128">CommonParameters</span></span>
<span data-ttu-id="04d3a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04d3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d3a-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04d3a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d3a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="04d3a-131">INPUTS</span></span>

### <span data-ttu-id="04d3a-132">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="04d3a-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="04d3a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="04d3a-133">System.String</span></span>

## <span data-ttu-id="04d3a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="04d3a-134">OUTPUTS</span></span>

### <span data-ttu-id="04d3a-135">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="04d3a-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="04d3a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="04d3a-136">NOTES</span></span>

## <span data-ttu-id="04d3a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="04d3a-137">RELATED LINKS</span></span>
