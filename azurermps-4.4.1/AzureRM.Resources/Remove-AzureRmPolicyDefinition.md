---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625685"
---
# <span data-ttu-id="3d4ec-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d4ec-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="3d4ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4ec-103">移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d4ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d4ec-104">SYNTAX</span></span>

### <span data-ttu-id="3d4ec-105">原則定義名稱參數已設定。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-105">The policy definition name parameter set.</span></span> <span data-ttu-id="3d4ec-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="3d4ec-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4ec-107">已設定原則定義識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d4ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="3d4ec-108">DESCRIPTION</span></span>
<span data-ttu-id="3d4ec-109">**AzureRmPolicyDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="3d4ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="3d4ec-110">EXAMPLES</span></span>

### <span data-ttu-id="3d4ec-111">範例1：依名稱移除原則定義</span><span class="sxs-lookup"><span data-stu-id="3d4ec-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="3d4ec-112">這個命令會移除指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="3d4ec-113">範例2：依資源識別碼移除原則定義</span><span class="sxs-lookup"><span data-stu-id="3d4ec-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="3d4ec-114">第一個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3d4ec-115">該命令會將它儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="3d4ec-116">第二個命令會移除由 $PolicyDefinition 的 **ResourceId** 屬性所識別的原則定義。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="3d4ec-117">參數</span><span class="sxs-lookup"><span data-stu-id="3d4ec-117">PARAMETERS</span></span>

### <span data-ttu-id="3d4ec-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d4ec-118">-ApiVersion</span></span>
<span data-ttu-id="3d4ec-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d4ec-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3d4ec-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3d4ec-121">-Force</span></span>
<span data-ttu-id="3d4ec-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d4ec-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="3d4ec-123">-Id</span></span>
<span data-ttu-id="3d4ec-124">指定此 Cmdlet 移除之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4ec-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3d4ec-125">-InformationAction</span></span>
<span data-ttu-id="3d4ec-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3d4ec-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3d4ec-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d4ec-128">持續</span><span class="sxs-lookup"><span data-stu-id="3d4ec-128">Continue</span></span>
- <span data-ttu-id="3d4ec-129">理會</span><span class="sxs-lookup"><span data-stu-id="3d4ec-129">Ignore</span></span>
- <span data-ttu-id="3d4ec-130">看</span><span class="sxs-lookup"><span data-stu-id="3d4ec-130">Inquire</span></span>
- <span data-ttu-id="3d4ec-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3d4ec-131">SilentlyContinue</span></span>
- <span data-ttu-id="3d4ec-132">停止</span><span class="sxs-lookup"><span data-stu-id="3d4ec-132">Stop</span></span>
- <span data-ttu-id="3d4ec-133">封存</span><span class="sxs-lookup"><span data-stu-id="3d4ec-133">Suspend</span></span>

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

### <span data-ttu-id="3d4ec-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3d4ec-134">-InformationVariable</span></span>
<span data-ttu-id="3d4ec-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3d4ec-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d4ec-136">-Name</span></span>
<span data-ttu-id="3d4ec-137">指定此 Cmdlet 移除之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4ec-138">-預先</span><span class="sxs-lookup"><span data-stu-id="3d4ec-138">-Pre</span></span>
<span data-ttu-id="3d4ec-139">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3d4ec-140">-確認</span><span class="sxs-lookup"><span data-stu-id="3d4ec-140">-Confirm</span></span>
<span data-ttu-id="3d4ec-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d4ec-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4ec-142">-WhatIf</span></span>
<span data-ttu-id="3d4ec-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d4ec-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d4ec-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4ec-145">-DefaultProfile</span></span>
<span data-ttu-id="3d4ec-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d4ec-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4ec-147">CommonParameters</span></span>
<span data-ttu-id="3d4ec-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4ec-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d4ec-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4ec-150">輸入</span><span class="sxs-lookup"><span data-stu-id="3d4ec-150">INPUTS</span></span>

## <span data-ttu-id="3d4ec-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3d4ec-151">OUTPUTS</span></span>

### <span data-ttu-id="3d4ec-152">System.object</span><span class="sxs-lookup"><span data-stu-id="3d4ec-152">System.Boolean</span></span>

## <span data-ttu-id="3d4ec-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3d4ec-153">NOTES</span></span>

## <span data-ttu-id="3d4ec-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d4ec-154">RELATED LINKS</span></span>

[<span data-ttu-id="3d4ec-155">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d4ec-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="3d4ec-156">新-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d4ec-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="3d4ec-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d4ec-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


