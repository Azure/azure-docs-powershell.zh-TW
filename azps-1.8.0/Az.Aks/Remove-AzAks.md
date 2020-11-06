---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: dc8b22697d606e827a0855a446d969ff2c90edc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611689"
---
# <span data-ttu-id="3ca0a-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="3ca0a-101">Remove-AzAks</span></span>

## <span data-ttu-id="3ca0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ca0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca0a-103">刪除受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3ca0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ca0a-104">SYNTAX</span></span>

### <span data-ttu-id="3ca0a-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3ca0a-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca0a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca0a-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca0a-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca0a-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca0a-108">說明</span><span class="sxs-lookup"><span data-stu-id="3ca0a-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca0a-109">刪除受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3ca0a-110">示例</span><span class="sxs-lookup"><span data-stu-id="3ca0a-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca0a-111">刪除現有的 managed Kubernetes 群集</span><span class="sxs-lookup"><span data-stu-id="3ca0a-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="3ca0a-112">參數</span><span class="sxs-lookup"><span data-stu-id="3ca0a-112">PARAMETERS</span></span>

### <span data-ttu-id="3ca0a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ca0a-113">-AsJob</span></span>
<span data-ttu-id="3ca0a-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3ca0a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ca0a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0a-115">-DefaultProfile</span></span>
<span data-ttu-id="3ca0a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca0a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3ca0a-117">-Force</span></span>
<span data-ttu-id="3ca0a-118">移除受管理的 Kubernetes 群集而不出現提示</span><span class="sxs-lookup"><span data-stu-id="3ca0a-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="3ca0a-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="3ca0a-119">-Id</span></span>
<span data-ttu-id="3ca0a-120">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="3ca0a-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="3ca0a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca0a-121">-InputObject</span></span>
<span data-ttu-id="3ca0a-122">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3ca0a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ca0a-123">-Name</span></span>
<span data-ttu-id="3ca0a-124">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="3ca0a-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="3ca0a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ca0a-125">-PassThru</span></span>
<span data-ttu-id="3ca0a-126">如果刪除成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="3ca0a-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="3ca0a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca0a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ca0a-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3ca0a-128">Resource group name</span></span>

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

### <span data-ttu-id="3ca0a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="3ca0a-129">-Confirm</span></span>
<span data-ttu-id="3ca0a-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca0a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca0a-131">-WhatIf</span></span>
<span data-ttu-id="3ca0a-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca0a-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca0a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca0a-134">CommonParameters</span></span>
<span data-ttu-id="3ca0a-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca0a-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca0a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3ca0a-137">INPUTS</span></span>

### <span data-ttu-id="3ca0a-138">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="3ca0a-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="3ca0a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3ca0a-139">System.String</span></span>

## <span data-ttu-id="3ca0a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3ca0a-140">OUTPUTS</span></span>

### <span data-ttu-id="3ca0a-141">System.object</span><span class="sxs-lookup"><span data-stu-id="3ca0a-141">System.Boolean</span></span>

## <span data-ttu-id="3ca0a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3ca0a-142">NOTES</span></span>

## <span data-ttu-id="3ca0a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ca0a-143">RELATED LINKS</span></span>