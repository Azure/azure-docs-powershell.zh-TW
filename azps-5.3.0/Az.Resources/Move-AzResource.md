---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d14d591ffdc0e20934a0cf758407dc2b4e6e152c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435474"
---
# <span data-ttu-id="c73ed-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="c73ed-101">Move-AzResource</span></span>

## <span data-ttu-id="c73ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c73ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c73ed-103">將資源移至不同的資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="c73ed-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="c73ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="c73ed-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c73ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="c73ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c73ed-106">**AzResource** Cmdlet 會將現有資源移至不同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c73ed-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="c73ed-107">該資源群組可以是不同的訂閱。</span><span class="sxs-lookup"><span data-stu-id="c73ed-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="c73ed-108">示例</span><span class="sxs-lookup"><span data-stu-id="c73ed-108">EXAMPLES</span></span>

### <span data-ttu-id="c73ed-109">範例1：將資源移至資源群組</span><span class="sxs-lookup"><span data-stu-id="c73ed-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="c73ed-110">第一個命令會使用 Get-AzResource Cmdlet 來取得名為 ContosoStorageAccount 的資源，然後將該資源儲存在 $Resource 變數中。</span><span class="sxs-lookup"><span data-stu-id="c73ed-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="c73ed-111">第二個命令會將該資源移到名為 ResourceGroup14 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="c73ed-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="c73ed-112">命令會使用 $Resource 的 **ResourceId** 屬性來識別要移動的資源。</span><span class="sxs-lookup"><span data-stu-id="c73ed-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="c73ed-113">參數</span><span class="sxs-lookup"><span data-stu-id="c73ed-113">PARAMETERS</span></span>

### <span data-ttu-id="c73ed-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c73ed-114">-ApiVersion</span></span>
<span data-ttu-id="c73ed-115">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c73ed-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c73ed-116">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="c73ed-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c73ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73ed-117">-DefaultProfile</span></span>
<span data-ttu-id="c73ed-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c73ed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c73ed-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c73ed-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="c73ed-120">指定此 Cmdlet 將資源移動到哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c73ed-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="c73ed-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c73ed-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="c73ed-122">指定此 Cmdlet 將資源移動到其中的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c73ed-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="c73ed-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c73ed-123">-Force</span></span>
<span data-ttu-id="c73ed-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c73ed-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c73ed-125">-預先</span><span class="sxs-lookup"><span data-stu-id="c73ed-125">-Pre</span></span>
<span data-ttu-id="c73ed-126">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c73ed-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c73ed-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c73ed-127">-ResourceId</span></span>
<span data-ttu-id="c73ed-128">指定此 Cmdlet 所移動之資源的識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="c73ed-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="c73ed-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c73ed-129">-Confirm</span></span>
<span data-ttu-id="c73ed-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c73ed-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c73ed-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c73ed-131">-WhatIf</span></span>
<span data-ttu-id="c73ed-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c73ed-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c73ed-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c73ed-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c73ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73ed-134">CommonParameters</span></span>
<span data-ttu-id="c73ed-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c73ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73ed-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c73ed-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73ed-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c73ed-137">INPUTS</span></span>

### <span data-ttu-id="c73ed-138">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c73ed-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c73ed-139">System.object []</span><span class="sxs-lookup"><span data-stu-id="c73ed-139">System.String[]</span></span>

## <span data-ttu-id="c73ed-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c73ed-140">OUTPUTS</span></span>

### <span data-ttu-id="c73ed-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c73ed-141">System.Boolean</span></span>

## <span data-ttu-id="c73ed-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c73ed-142">NOTES</span></span>

## <span data-ttu-id="c73ed-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c73ed-143">RELATED LINKS</span></span>

[<span data-ttu-id="c73ed-144">AzResource</span><span class="sxs-lookup"><span data-stu-id="c73ed-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="c73ed-145">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="c73ed-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c73ed-146">移除-AzResource</span><span class="sxs-lookup"><span data-stu-id="c73ed-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="c73ed-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="c73ed-147">Set-AzResource</span></span>](./Set-AzResource.md)


