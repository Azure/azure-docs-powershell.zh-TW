---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4a40b3fd0045a48d6a69c76970b3835ef2d685c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624775"
---
# <span data-ttu-id="53c63-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="53c63-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="53c63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53c63-102">SYNOPSIS</span></span>
<span data-ttu-id="53c63-103">將資源移至不同的資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="53c63-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53c63-104">句法</span><span class="sxs-lookup"><span data-stu-id="53c63-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53c63-105">說明</span><span class="sxs-lookup"><span data-stu-id="53c63-105">DESCRIPTION</span></span>
<span data-ttu-id="53c63-106">**AzureRmResource** Cmdlet 會將現有資源移至不同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="53c63-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="53c63-107">該資源群組可以是不同的訂閱。</span><span class="sxs-lookup"><span data-stu-id="53c63-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="53c63-108">示例</span><span class="sxs-lookup"><span data-stu-id="53c63-108">EXAMPLES</span></span>

### <span data-ttu-id="53c63-109">範例1：將資源移至資源群組</span><span class="sxs-lookup"><span data-stu-id="53c63-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="53c63-110">第一個命令會使用 Get-AzureRmResource Cmdlet 來取得名為 ContosoStorageAccount 的資源，然後將該資源儲存在 $Resource 變數中。</span><span class="sxs-lookup"><span data-stu-id="53c63-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="53c63-111">第二個命令會將該資源移到名為 ResourceGroup14 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="53c63-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="53c63-112">命令會使用 $Resource 的 **ResourceId** 屬性來識別要移動的資源。</span><span class="sxs-lookup"><span data-stu-id="53c63-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="53c63-113">參數</span><span class="sxs-lookup"><span data-stu-id="53c63-113">PARAMETERS</span></span>

### <span data-ttu-id="53c63-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53c63-114">-ApiVersion</span></span>
<span data-ttu-id="53c63-115">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="53c63-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="53c63-116">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="53c63-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="53c63-117">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c63-117">-DestinationResourceGroupName</span></span>
<span data-ttu-id="53c63-118">指定此 Cmdlet 將資源移動到哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53c63-118">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="53c63-119">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53c63-119">-DestinationSubscriptionId</span></span>
<span data-ttu-id="53c63-120">指定此 Cmdlet 將資源移動到其中的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="53c63-120">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="53c63-121">-Force</span><span class="sxs-lookup"><span data-stu-id="53c63-121">-Force</span></span>
<span data-ttu-id="53c63-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="53c63-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53c63-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="53c63-123">-InformationAction</span></span>
<span data-ttu-id="53c63-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="53c63-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="53c63-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="53c63-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53c63-126">持續</span><span class="sxs-lookup"><span data-stu-id="53c63-126">Continue</span></span>
- <span data-ttu-id="53c63-127">理會</span><span class="sxs-lookup"><span data-stu-id="53c63-127">Ignore</span></span>
- <span data-ttu-id="53c63-128">看</span><span class="sxs-lookup"><span data-stu-id="53c63-128">Inquire</span></span>
- <span data-ttu-id="53c63-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="53c63-129">SilentlyContinue</span></span>
- <span data-ttu-id="53c63-130">停止</span><span class="sxs-lookup"><span data-stu-id="53c63-130">Stop</span></span>
- <span data-ttu-id="53c63-131">封存</span><span class="sxs-lookup"><span data-stu-id="53c63-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c63-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="53c63-132">-InformationVariable</span></span>
<span data-ttu-id="53c63-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="53c63-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c63-134">-預先</span><span class="sxs-lookup"><span data-stu-id="53c63-134">-Pre</span></span>
<span data-ttu-id="53c63-135">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="53c63-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53c63-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53c63-136">-ResourceId</span></span>
<span data-ttu-id="53c63-137">指定此 Cmdlet 所移動之資源的識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="53c63-137">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="53c63-138">-確認</span><span class="sxs-lookup"><span data-stu-id="53c63-138">-Confirm</span></span>
<span data-ttu-id="53c63-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53c63-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c63-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c63-140">-WhatIf</span></span>
<span data-ttu-id="53c63-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53c63-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c63-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53c63-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c63-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c63-143">-DefaultProfile</span></span>
<span data-ttu-id="53c63-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53c63-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53c63-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c63-145">CommonParameters</span></span>
<span data-ttu-id="53c63-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53c63-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c63-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53c63-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c63-148">輸入</span><span class="sxs-lookup"><span data-stu-id="53c63-148">INPUTS</span></span>

### <span data-ttu-id="53c63-149">String []</span><span class="sxs-lookup"><span data-stu-id="53c63-149">String[]</span></span>
<span data-ttu-id="53c63-150">參數 "ResourceId" 接受管道中類型 "String [] 的值</span><span class="sxs-lookup"><span data-stu-id="53c63-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="53c63-151">輸出</span><span class="sxs-lookup"><span data-stu-id="53c63-151">OUTPUTS</span></span>

### <span data-ttu-id="53c63-152">System.object</span><span class="sxs-lookup"><span data-stu-id="53c63-152">System.Boolean</span></span>

## <span data-ttu-id="53c63-153">筆記</span><span class="sxs-lookup"><span data-stu-id="53c63-153">NOTES</span></span>

## <span data-ttu-id="53c63-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="53c63-154">RELATED LINKS</span></span>

[<span data-ttu-id="53c63-155">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="53c63-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="53c63-156">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="53c63-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="53c63-157">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="53c63-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="53c63-158">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="53c63-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="53c63-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="53c63-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


