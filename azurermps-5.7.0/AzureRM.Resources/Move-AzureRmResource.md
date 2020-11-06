---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4562c217a771f53995a531a3ca72066da672a144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452072"
---
# <span data-ttu-id="b8136-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8136-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="b8136-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8136-102">SYNOPSIS</span></span>
<span data-ttu-id="b8136-103">將資源移至不同的資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8136-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8136-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8136-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8136-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8136-105">DESCRIPTION</span></span>
<span data-ttu-id="b8136-106">**AzureRmResource** Cmdlet 會將現有資源移至不同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b8136-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="b8136-107">該資源群組可以是不同的訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8136-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="b8136-108">示例</span><span class="sxs-lookup"><span data-stu-id="b8136-108">EXAMPLES</span></span>

### <span data-ttu-id="b8136-109">範例1：將資源移至資源群組</span><span class="sxs-lookup"><span data-stu-id="b8136-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="b8136-110">第一個命令會使用 Get-AzureRmResource Cmdlet 來取得名為 ContosoStorageAccount 的資源，然後將該資源儲存在 $Resource 變數中。</span><span class="sxs-lookup"><span data-stu-id="b8136-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="b8136-111">第二個命令會將該資源移到名為 ResourceGroup14 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="b8136-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="b8136-112">命令會使用 $Resource 的 **ResourceId** 屬性來識別要移動的資源。</span><span class="sxs-lookup"><span data-stu-id="b8136-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="b8136-113">參數</span><span class="sxs-lookup"><span data-stu-id="b8136-113">PARAMETERS</span></span>

### <span data-ttu-id="b8136-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b8136-114">-ApiVersion</span></span>
<span data-ttu-id="b8136-115">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b8136-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b8136-116">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="b8136-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b8136-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8136-117">-DefaultProfile</span></span>
<span data-ttu-id="b8136-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b8136-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8136-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="b8136-120">指定此 Cmdlet 將資源移動到哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8136-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8136-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="b8136-122">指定此 Cmdlet 將資源移動到其中的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8136-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b8136-123">-Force</span></span>
<span data-ttu-id="b8136-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b8136-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8136-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8136-125">-InformationAction</span></span>
<span data-ttu-id="b8136-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b8136-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8136-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b8136-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8136-128">持續</span><span class="sxs-lookup"><span data-stu-id="b8136-128">Continue</span></span>
- <span data-ttu-id="b8136-129">理會</span><span class="sxs-lookup"><span data-stu-id="b8136-129">Ignore</span></span>
- <span data-ttu-id="b8136-130">看</span><span class="sxs-lookup"><span data-stu-id="b8136-130">Inquire</span></span>
- <span data-ttu-id="b8136-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8136-131">SilentlyContinue</span></span>
- <span data-ttu-id="b8136-132">停止</span><span class="sxs-lookup"><span data-stu-id="b8136-132">Stop</span></span>
- <span data-ttu-id="b8136-133">封存</span><span class="sxs-lookup"><span data-stu-id="b8136-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8136-134">-InformationVariable</span></span>
<span data-ttu-id="b8136-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b8136-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-136">-預先</span><span class="sxs-lookup"><span data-stu-id="b8136-136">-Pre</span></span>
<span data-ttu-id="b8136-137">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b8136-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b8136-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8136-138">-ResourceId</span></span>
<span data-ttu-id="b8136-139">指定此 Cmdlet 所移動之資源的識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="b8136-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-140">-確認</span><span class="sxs-lookup"><span data-stu-id="b8136-140">-Confirm</span></span>
<span data-ttu-id="b8136-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8136-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8136-142">-WhatIf</span></span>
<span data-ttu-id="b8136-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8136-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8136-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8136-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8136-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8136-145">CommonParameters</span></span>
<span data-ttu-id="b8136-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8136-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8136-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8136-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8136-148">輸入</span><span class="sxs-lookup"><span data-stu-id="b8136-148">INPUTS</span></span>

### <span data-ttu-id="b8136-149">String []</span><span class="sxs-lookup"><span data-stu-id="b8136-149">String[]</span></span>
<span data-ttu-id="b8136-150">參數 "ResourceId" 接受管道中類型 "String [] 的值</span><span class="sxs-lookup"><span data-stu-id="b8136-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="b8136-151">輸出</span><span class="sxs-lookup"><span data-stu-id="b8136-151">OUTPUTS</span></span>

### <span data-ttu-id="b8136-152">System.object</span><span class="sxs-lookup"><span data-stu-id="b8136-152">System.Boolean</span></span>

## <span data-ttu-id="b8136-153">筆記</span><span class="sxs-lookup"><span data-stu-id="b8136-153">NOTES</span></span>

## <span data-ttu-id="b8136-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8136-154">RELATED LINKS</span></span>

[<span data-ttu-id="b8136-155">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8136-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="b8136-156">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8136-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="b8136-157">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8136-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b8136-158">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8136-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="b8136-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8136-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


