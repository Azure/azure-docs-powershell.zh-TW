---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 16e43df2da9509d7fb222f3299a4c611d146026c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904586"
---
# <span data-ttu-id="af1f5-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="af1f5-101">Move-AzResource</span></span>

## <span data-ttu-id="af1f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="af1f5-103">將資源移至不同的資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="af1f5-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="af1f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="af1f5-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af1f5-105">描述</span><span class="sxs-lookup"><span data-stu-id="af1f5-105">DESCRIPTION</span></span>
<span data-ttu-id="af1f5-106">**Move-AzResource** Cmdlet 會將現有的資源移至不同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="af1f5-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="af1f5-107">資源群組可以在不同的訂閱中。</span><span class="sxs-lookup"><span data-stu-id="af1f5-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="af1f5-108">例子</span><span class="sxs-lookup"><span data-stu-id="af1f5-108">EXAMPLES</span></span>

### <span data-ttu-id="af1f5-109">範例 1：將資源移至資源群組</span><span class="sxs-lookup"><span data-stu-id="af1f5-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="af1f5-110">第一個命令會使用 Get-AzResource Cmdlet 獲得名為 ContosoStorageAccount 的資源，然後將該資源儲存在 $Resource 變數中。</span><span class="sxs-lookup"><span data-stu-id="af1f5-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="af1f5-111">第二個命令會將資源移至名為 ResourceGroup14 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="af1f5-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="af1f5-112">命令會使用資源的 **ResourceId** 屬性來識別要移動$Resource。</span><span class="sxs-lookup"><span data-stu-id="af1f5-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="af1f5-113">參數</span><span class="sxs-lookup"><span data-stu-id="af1f5-113">PARAMETERS</span></span>

### <span data-ttu-id="af1f5-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="af1f5-114">-ApiVersion</span></span>
<span data-ttu-id="af1f5-115">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="af1f5-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="af1f5-116">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="af1f5-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af1f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1f5-117">-DefaultProfile</span></span>
<span data-ttu-id="af1f5-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="af1f5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af1f5-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af1f5-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="af1f5-120">指定此 Cmdlet 將資源移動至其中的資源組名。</span><span class="sxs-lookup"><span data-stu-id="af1f5-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af1f5-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af1f5-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="af1f5-122">指定此 Cmdlet 移動資源的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="af1f5-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af1f5-123">-強制</span><span class="sxs-lookup"><span data-stu-id="af1f5-123">-Force</span></span>
<span data-ttu-id="af1f5-124">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="af1f5-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af1f5-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="af1f5-125">-Pre</span></span>
<span data-ttu-id="af1f5-126">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="af1f5-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="af1f5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af1f5-127">-ResourceId</span></span>
<span data-ttu-id="af1f5-128">指定此 Cmdlet 移動之資源的 ID 陣列。</span><span class="sxs-lookup"><span data-stu-id="af1f5-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af1f5-129">-確認</span><span class="sxs-lookup"><span data-stu-id="af1f5-129">-Confirm</span></span>
<span data-ttu-id="af1f5-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="af1f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af1f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af1f5-131">-WhatIf</span></span>
<span data-ttu-id="af1f5-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af1f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af1f5-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af1f5-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af1f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1f5-134">CommonParameters</span></span>
<span data-ttu-id="af1f5-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af1f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1f5-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af1f5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1f5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="af1f5-137">INPUTS</span></span>

### <span data-ttu-id="af1f5-138">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af1f5-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af1f5-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="af1f5-139">System.String[]</span></span>

## <span data-ttu-id="af1f5-140">輸出</span><span class="sxs-lookup"><span data-stu-id="af1f5-140">OUTPUTS</span></span>

### <span data-ttu-id="af1f5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af1f5-141">System.Boolean</span></span>

## <span data-ttu-id="af1f5-142">筆記</span><span class="sxs-lookup"><span data-stu-id="af1f5-142">NOTES</span></span>

## <span data-ttu-id="af1f5-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="af1f5-143">RELATED LINKS</span></span>

[<span data-ttu-id="af1f5-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="af1f5-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="af1f5-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="af1f5-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="af1f5-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="af1f5-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="af1f5-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="af1f5-147">Set-AzResource</span></span>](./Set-AzResource.md)


