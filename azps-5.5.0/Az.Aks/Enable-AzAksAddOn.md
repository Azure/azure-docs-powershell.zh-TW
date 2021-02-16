---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 40fb9f328f0f838f5d76de6de5509c74b0002768
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138970"
---
# <span data-ttu-id="3d975-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="3d975-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="3d975-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d975-102">SYNOPSIS</span></span>
<span data-ttu-id="3d975-103">啟用 aks 的 addons。</span><span class="sxs-lookup"><span data-stu-id="3d975-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="3d975-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d975-104">SYNTAX</span></span>

### <span data-ttu-id="3d975-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3d975-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d975-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d975-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d975-107">說明</span><span class="sxs-lookup"><span data-stu-id="3d975-107">DESCRIPTION</span></span>
<span data-ttu-id="3d975-108">啟用 aks 的 addons。</span><span class="sxs-lookup"><span data-stu-id="3d975-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="3d975-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d975-109">EXAMPLES</span></span>

### <span data-ttu-id="3d975-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3d975-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="3d975-111">啟用 [addons]、[] `HttpApplicationRouting` `Monitoring` 及 [aks] `AzurePolicy` `VirtualNode` `KubeDashboard` 。</span><span class="sxs-lookup"><span data-stu-id="3d975-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="3d975-112">參數</span><span class="sxs-lookup"><span data-stu-id="3d975-112">PARAMETERS</span></span>

### <span data-ttu-id="3d975-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3d975-113">-ClusterName</span></span>
<span data-ttu-id="3d975-114">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="3d975-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="3d975-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="3d975-115">-ClusterObject</span></span>
<span data-ttu-id="3d975-116">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="3d975-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3d975-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d975-117">-DefaultProfile</span></span>
<span data-ttu-id="3d975-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d975-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d975-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d975-119">-Name</span></span>
<span data-ttu-id="3d975-120">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="3d975-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="3d975-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d975-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d975-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3d975-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d975-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3d975-123">-SubnetName</span></span>
<span data-ttu-id="3d975-124">VirtualNode 的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="3d975-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="3d975-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3d975-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="3d975-126">監視工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d975-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="3d975-127">-確認</span><span class="sxs-lookup"><span data-stu-id="3d975-127">-Confirm</span></span>
<span data-ttu-id="3d975-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d975-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d975-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d975-129">-WhatIf</span></span>
<span data-ttu-id="3d975-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d975-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d975-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d975-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d975-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d975-132">CommonParameters</span></span>
<span data-ttu-id="3d975-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d975-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d975-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d975-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d975-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3d975-135">INPUTS</span></span>

### <span data-ttu-id="3d975-136">System.object</span><span class="sxs-lookup"><span data-stu-id="3d975-136">System.String</span></span>

### <span data-ttu-id="3d975-137">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="3d975-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="3d975-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3d975-138">OUTPUTS</span></span>

### <span data-ttu-id="3d975-139">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="3d975-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="3d975-140">筆記</span><span class="sxs-lookup"><span data-stu-id="3d975-140">NOTES</span></span>

## <span data-ttu-id="3d975-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d975-141">RELATED LINKS</span></span>
