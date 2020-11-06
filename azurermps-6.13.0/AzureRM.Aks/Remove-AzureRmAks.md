---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 909121a78d09db7d15591a93db9479d0ccc8381b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451967"
---
# <span data-ttu-id="a2d98-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="a2d98-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="a2d98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2d98-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d98-103">刪除受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="a2d98-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2d98-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2d98-104">SYNTAX</span></span>

### <span data-ttu-id="a2d98-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2d98-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d98-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d98-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d98-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d98-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d98-108">說明</span><span class="sxs-lookup"><span data-stu-id="a2d98-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d98-109">刪除受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="a2d98-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a2d98-110">示例</span><span class="sxs-lookup"><span data-stu-id="a2d98-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d98-111">刪除現有的 managed Kubernetes 群集</span><span class="sxs-lookup"><span data-stu-id="a2d98-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="a2d98-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2d98-112">PARAMETERS</span></span>

### <span data-ttu-id="a2d98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2d98-113">-AsJob</span></span>
<span data-ttu-id="a2d98-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2d98-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2d98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d98-115">-DefaultProfile</span></span>
<span data-ttu-id="a2d98-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2d98-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d98-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a2d98-117">-Force</span></span>
<span data-ttu-id="a2d98-118">移除受管理的 Kubernetes 群集而不出現提示</span><span class="sxs-lookup"><span data-stu-id="a2d98-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="a2d98-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a2d98-119">-Id</span></span>
<span data-ttu-id="a2d98-120">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="a2d98-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a2d98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2d98-121">-InputObject</span></span>
<span data-ttu-id="a2d98-122">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a2d98-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2d98-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2d98-123">-Name</span></span>
<span data-ttu-id="a2d98-124">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="a2d98-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a2d98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2d98-125">-PassThru</span></span>
<span data-ttu-id="a2d98-126">如果刪除成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="a2d98-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="a2d98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d98-127">-ResourceGroupName</span></span>
<span data-ttu-id="a2d98-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a2d98-128">Resource group name</span></span>

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

### <span data-ttu-id="a2d98-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a2d98-129">-Confirm</span></span>
<span data-ttu-id="a2d98-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2d98-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d98-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d98-131">-WhatIf</span></span>
<span data-ttu-id="a2d98-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2d98-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d98-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2d98-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d98-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d98-134">CommonParameters</span></span>
<span data-ttu-id="a2d98-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2d98-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d98-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2d98-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d98-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a2d98-137">INPUTS</span></span>

### <span data-ttu-id="a2d98-138">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="a2d98-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="a2d98-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a2d98-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a2d98-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a2d98-140">System.String</span></span>

## <span data-ttu-id="a2d98-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a2d98-141">OUTPUTS</span></span>

### <span data-ttu-id="a2d98-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a2d98-142">System.Boolean</span></span>

## <span data-ttu-id="a2d98-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a2d98-143">NOTES</span></span>

## <span data-ttu-id="a2d98-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2d98-144">RELATED LINKS</span></span>