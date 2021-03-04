---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: 0f0a1c530e4f02e031307006c0e6bf994f9a7c5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904758"
---
# <span data-ttu-id="32f88-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="32f88-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="32f88-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32f88-102">SYNOPSIS</span></span>
<span data-ttu-id="32f88-103">刪除受管理的Kubernetes 集區。</span><span class="sxs-lookup"><span data-stu-id="32f88-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="32f88-104">語法</span><span class="sxs-lookup"><span data-stu-id="32f88-104">SYNTAX</span></span>

### <span data-ttu-id="32f88-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="32f88-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f88-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32f88-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f88-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32f88-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32f88-108">描述</span><span class="sxs-lookup"><span data-stu-id="32f88-108">DESCRIPTION</span></span>
<span data-ttu-id="32f88-109">刪除受管理的Kubernetes 集區。</span><span class="sxs-lookup"><span data-stu-id="32f88-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="32f88-110">例子</span><span class="sxs-lookup"><span data-stu-id="32f88-110">EXAMPLES</span></span>

### <span data-ttu-id="32f88-111">刪除現有的受管理的Kubernetes 集區</span><span class="sxs-lookup"><span data-stu-id="32f88-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="32f88-112">參數</span><span class="sxs-lookup"><span data-stu-id="32f88-112">PARAMETERS</span></span>

### <span data-ttu-id="32f88-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32f88-113">-AsJob</span></span>
<span data-ttu-id="32f88-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="32f88-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32f88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f88-115">-DefaultProfile</span></span>
<span data-ttu-id="32f88-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32f88-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32f88-117">-強制</span><span class="sxs-lookup"><span data-stu-id="32f88-117">-Force</span></span>
<span data-ttu-id="32f88-118">移除受管理的 Kubernetes 集區，而不提示</span><span class="sxs-lookup"><span data-stu-id="32f88-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="32f88-119">-Id</span><span class="sxs-lookup"><span data-stu-id="32f88-119">-Id</span></span>
<span data-ttu-id="32f88-120">受管理的Kubernetes 集的識別碼</span><span class="sxs-lookup"><span data-stu-id="32f88-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32f88-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32f88-121">-InputObject</span></span>
<span data-ttu-id="32f88-122">PSKubernetesCluster 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="32f88-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="32f88-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="32f88-123">-Name</span></span>
<span data-ttu-id="32f88-124">受管理的Kubernetes 組名</span><span class="sxs-lookup"><span data-stu-id="32f88-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f88-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32f88-125">-PassThru</span></span>
<span data-ttu-id="32f88-126">如果刪除成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="32f88-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="32f88-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f88-127">-ResourceGroupName</span></span>
<span data-ttu-id="32f88-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="32f88-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f88-129">-確認</span><span class="sxs-lookup"><span data-stu-id="32f88-129">-Confirm</span></span>
<span data-ttu-id="32f88-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32f88-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f88-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f88-131">-WhatIf</span></span>
<span data-ttu-id="32f88-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32f88-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32f88-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32f88-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f88-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f88-134">CommonParameters</span></span>
<span data-ttu-id="32f88-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32f88-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f88-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32f88-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f88-137">輸入</span><span class="sxs-lookup"><span data-stu-id="32f88-137">INPUTS</span></span>

### <span data-ttu-id="32f88-138">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="32f88-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="32f88-139">System.String</span><span class="sxs-lookup"><span data-stu-id="32f88-139">System.String</span></span>

## <span data-ttu-id="32f88-140">輸出</span><span class="sxs-lookup"><span data-stu-id="32f88-140">OUTPUTS</span></span>

### <span data-ttu-id="32f88-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32f88-141">System.Boolean</span></span>

## <span data-ttu-id="32f88-142">筆記</span><span class="sxs-lookup"><span data-stu-id="32f88-142">NOTES</span></span>

## <span data-ttu-id="32f88-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="32f88-143">RELATED LINKS</span></span>
