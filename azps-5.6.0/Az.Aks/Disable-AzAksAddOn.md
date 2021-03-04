---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 5d0cc543d5ec893ecb1f83b8fd62f25bcb32f5b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905665"
---
# <span data-ttu-id="aa296-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="aa296-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="aa296-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aa296-102">SYNOPSIS</span></span>
<span data-ttu-id="aa296-103">停用附加元件。</span><span class="sxs-lookup"><span data-stu-id="aa296-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="aa296-104">語法</span><span class="sxs-lookup"><span data-stu-id="aa296-104">SYNTAX</span></span>

### <span data-ttu-id="aa296-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aa296-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa296-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa296-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa296-107">描述</span><span class="sxs-lookup"><span data-stu-id="aa296-107">DESCRIPTION</span></span>
<span data-ttu-id="aa296-108">停用附加元件。</span><span class="sxs-lookup"><span data-stu-id="aa296-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="aa296-109">例子</span><span class="sxs-lookup"><span data-stu-id="aa296-109">EXAMPLES</span></span>

### <span data-ttu-id="aa296-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="aa296-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="aa296-111">停用附加元件 `HttpApplicationRouting` `Monitoring` 、、 `AzurePolicy` 和 `VirtualNode` `KubeDashboard` aks。</span><span class="sxs-lookup"><span data-stu-id="aa296-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="aa296-112">參數</span><span class="sxs-lookup"><span data-stu-id="aa296-112">PARAMETERS</span></span>

### <span data-ttu-id="aa296-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="aa296-113">-ClusterName</span></span>
<span data-ttu-id="aa296-114">Kubernetes managed cluster Name.</span><span class="sxs-lookup"><span data-stu-id="aa296-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="aa296-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="aa296-115">-ClusterObject</span></span>
<span data-ttu-id="aa296-116">PSKubernetesCluster 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="aa296-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="aa296-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa296-117">-DefaultProfile</span></span>
<span data-ttu-id="aa296-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa296-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa296-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa296-119">-Name</span></span>
<span data-ttu-id="aa296-120">Kubernetes managed cluster Name.</span><span class="sxs-lookup"><span data-stu-id="aa296-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="aa296-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa296-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa296-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="aa296-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="aa296-123">-確認</span><span class="sxs-lookup"><span data-stu-id="aa296-123">-Confirm</span></span>
<span data-ttu-id="aa296-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aa296-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa296-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa296-125">-WhatIf</span></span>
<span data-ttu-id="aa296-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa296-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa296-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa296-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa296-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa296-128">CommonParameters</span></span>
<span data-ttu-id="aa296-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aa296-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa296-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa296-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa296-131">輸入</span><span class="sxs-lookup"><span data-stu-id="aa296-131">INPUTS</span></span>

### <span data-ttu-id="aa296-132">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="aa296-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="aa296-133">System.String</span><span class="sxs-lookup"><span data-stu-id="aa296-133">System.String</span></span>

## <span data-ttu-id="aa296-134">輸出</span><span class="sxs-lookup"><span data-stu-id="aa296-134">OUTPUTS</span></span>

### <span data-ttu-id="aa296-135">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="aa296-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="aa296-136">筆記</span><span class="sxs-lookup"><span data-stu-id="aa296-136">NOTES</span></span>

## <span data-ttu-id="aa296-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa296-137">RELATED LINKS</span></span>
