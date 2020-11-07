---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623588"
---
# <span data-ttu-id="962e7-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="962e7-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="962e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="962e7-102">SYNOPSIS</span></span>
<span data-ttu-id="962e7-103">移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="962e7-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="962e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="962e7-104">SYNTAX</span></span>

### <span data-ttu-id="962e7-105">RemoveByPolicyDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="962e7-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="962e7-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="962e7-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="962e7-107">說明</span><span class="sxs-lookup"><span data-stu-id="962e7-107">DESCRIPTION</span></span>
<span data-ttu-id="962e7-108">**AzureRmPolicyDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="962e7-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="962e7-109">示例</span><span class="sxs-lookup"><span data-stu-id="962e7-109">EXAMPLES</span></span>

### <span data-ttu-id="962e7-110">範例1：依名稱移除原則定義</span><span class="sxs-lookup"><span data-stu-id="962e7-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="962e7-111">這個命令會移除指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="962e7-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="962e7-112">範例2：依資源識別碼移除原則定義</span><span class="sxs-lookup"><span data-stu-id="962e7-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="962e7-113">第一個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="962e7-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="962e7-114">該命令會將它儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="962e7-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="962e7-115">第二個命令會移除由 $PolicyDefinition 的 **ResourceId** 屬性所識別的原則定義。</span><span class="sxs-lookup"><span data-stu-id="962e7-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="962e7-116">參數</span><span class="sxs-lookup"><span data-stu-id="962e7-116">PARAMETERS</span></span>

### <span data-ttu-id="962e7-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="962e7-117">-ApiVersion</span></span>
<span data-ttu-id="962e7-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="962e7-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="962e7-119">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="962e7-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="962e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962e7-120">-DefaultProfile</span></span>
<span data-ttu-id="962e7-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="962e7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="962e7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="962e7-122">-Force</span></span>
<span data-ttu-id="962e7-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="962e7-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="962e7-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="962e7-124">-Id</span></span>
<span data-ttu-id="962e7-125">指定此 Cmdlet 移除之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="962e7-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962e7-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="962e7-126">-InformationAction</span></span>
<span data-ttu-id="962e7-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="962e7-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="962e7-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="962e7-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="962e7-129">持續</span><span class="sxs-lookup"><span data-stu-id="962e7-129">Continue</span></span>
- <span data-ttu-id="962e7-130">理會</span><span class="sxs-lookup"><span data-stu-id="962e7-130">Ignore</span></span>
- <span data-ttu-id="962e7-131">看</span><span class="sxs-lookup"><span data-stu-id="962e7-131">Inquire</span></span>
- <span data-ttu-id="962e7-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="962e7-132">SilentlyContinue</span></span>
- <span data-ttu-id="962e7-133">停止</span><span class="sxs-lookup"><span data-stu-id="962e7-133">Stop</span></span>
- <span data-ttu-id="962e7-134">封存</span><span class="sxs-lookup"><span data-stu-id="962e7-134">Suspend</span></span>

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

### <span data-ttu-id="962e7-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="962e7-135">-InformationVariable</span></span>
<span data-ttu-id="962e7-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="962e7-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="962e7-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="962e7-137">-Name</span></span>
<span data-ttu-id="962e7-138">指定此 Cmdlet 移除之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="962e7-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962e7-139">-預先</span><span class="sxs-lookup"><span data-stu-id="962e7-139">-Pre</span></span>
<span data-ttu-id="962e7-140">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="962e7-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="962e7-141">-確認</span><span class="sxs-lookup"><span data-stu-id="962e7-141">-Confirm</span></span>
<span data-ttu-id="962e7-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="962e7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962e7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962e7-143">-WhatIf</span></span>
<span data-ttu-id="962e7-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="962e7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="962e7-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="962e7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962e7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962e7-146">CommonParameters</span></span>
<span data-ttu-id="962e7-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="962e7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962e7-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="962e7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962e7-149">輸入</span><span class="sxs-lookup"><span data-stu-id="962e7-149">INPUTS</span></span>

### <span data-ttu-id="962e7-150">所有</span><span class="sxs-lookup"><span data-stu-id="962e7-150">None</span></span>
<span data-ttu-id="962e7-151">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="962e7-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="962e7-152">輸出</span><span class="sxs-lookup"><span data-stu-id="962e7-152">OUTPUTS</span></span>

### <span data-ttu-id="962e7-153">System.object</span><span class="sxs-lookup"><span data-stu-id="962e7-153">System.Boolean</span></span>

## <span data-ttu-id="962e7-154">筆記</span><span class="sxs-lookup"><span data-stu-id="962e7-154">NOTES</span></span>

## <span data-ttu-id="962e7-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="962e7-155">RELATED LINKS</span></span>

[<span data-ttu-id="962e7-156">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="962e7-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="962e7-157">新-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="962e7-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="962e7-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="962e7-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


