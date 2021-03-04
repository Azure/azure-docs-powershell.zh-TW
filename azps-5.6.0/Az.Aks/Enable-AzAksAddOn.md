---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 1280f65659f986d0fd8402da0d3db5b1c5a92b58
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905661"
---
# <span data-ttu-id="70526-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="70526-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="70526-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70526-102">SYNOPSIS</span></span>
<span data-ttu-id="70526-103">啟用 aks 的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="70526-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="70526-104">語法</span><span class="sxs-lookup"><span data-stu-id="70526-104">SYNTAX</span></span>

### <span data-ttu-id="70526-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="70526-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70526-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70526-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70526-107">描述</span><span class="sxs-lookup"><span data-stu-id="70526-107">DESCRIPTION</span></span>
<span data-ttu-id="70526-108">啟用 aks 的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="70526-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="70526-109">例子</span><span class="sxs-lookup"><span data-stu-id="70526-109">EXAMPLES</span></span>

### <span data-ttu-id="70526-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="70526-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="70526-111">啟用附加元件 `HttpApplicationRouting` `Monitoring` 、、和 `AzurePolicy` `VirtualNode` `KubeDashboard` aks。</span><span class="sxs-lookup"><span data-stu-id="70526-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="70526-112">參數</span><span class="sxs-lookup"><span data-stu-id="70526-112">PARAMETERS</span></span>

### <span data-ttu-id="70526-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="70526-113">-ClusterName</span></span>
<span data-ttu-id="70526-114">Kubernetes managed cluster Name.</span><span class="sxs-lookup"><span data-stu-id="70526-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="70526-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="70526-115">-ClusterObject</span></span>
<span data-ttu-id="70526-116">PSKubernetesCluster 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="70526-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="70526-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70526-117">-DefaultProfile</span></span>
<span data-ttu-id="70526-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="70526-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70526-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="70526-119">-Name</span></span>
<span data-ttu-id="70526-120">Kubernetes managed cluster Name.</span><span class="sxs-lookup"><span data-stu-id="70526-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="70526-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70526-121">-ResourceGroupName</span></span>
<span data-ttu-id="70526-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="70526-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="70526-123">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="70526-123">-SubnetName</span></span>
<span data-ttu-id="70526-124">VirtualNode 的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="70526-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70526-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="70526-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="70526-126">監控工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="70526-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70526-127">-確認</span><span class="sxs-lookup"><span data-stu-id="70526-127">-Confirm</span></span>
<span data-ttu-id="70526-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="70526-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70526-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70526-129">-WhatIf</span></span>
<span data-ttu-id="70526-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70526-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70526-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70526-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70526-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70526-132">CommonParameters</span></span>
<span data-ttu-id="70526-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70526-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70526-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70526-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70526-135">輸入</span><span class="sxs-lookup"><span data-stu-id="70526-135">INPUTS</span></span>

### <span data-ttu-id="70526-136">System.String</span><span class="sxs-lookup"><span data-stu-id="70526-136">System.String</span></span>

### <span data-ttu-id="70526-137">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="70526-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="70526-138">輸出</span><span class="sxs-lookup"><span data-stu-id="70526-138">OUTPUTS</span></span>

### <span data-ttu-id="70526-139">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="70526-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="70526-140">筆記</span><span class="sxs-lookup"><span data-stu-id="70526-140">NOTES</span></span>

## <span data-ttu-id="70526-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="70526-141">RELATED LINKS</span></span>
