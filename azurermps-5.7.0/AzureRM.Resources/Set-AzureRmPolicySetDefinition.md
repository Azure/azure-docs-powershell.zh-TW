---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444360"
---
# <span data-ttu-id="b1f5f-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b1f5f-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b1f5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f5f-103">修改原則集定義</span><span class="sxs-lookup"><span data-stu-id="b1f5f-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1f5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1f5f-104">SYNTAX</span></span>

### <span data-ttu-id="b1f5f-105">SetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="b1f5f-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1f5f-106">SetById</span><span class="sxs-lookup"><span data-stu-id="b1f5f-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f5f-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1f5f-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f5f-108">**AzureRmPolicySetDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="b1f5f-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1f5f-109">EXAMPLES</span></span>

### <span data-ttu-id="b1f5f-110">範例1：更新原則集定義的描述</span><span class="sxs-lookup"><span data-stu-id="b1f5f-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="b1f5f-111">第一個命令會使用 Get-AzureRmPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b1f5f-112">該命令會將該物件儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="b1f5f-113">第二個命令會更新由 $PolicySetDefinition 的 **ResourceId** 屬性所識別之原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b1f5f-114">參數</span><span class="sxs-lookup"><span data-stu-id="b1f5f-114">PARAMETERS</span></span>

### <span data-ttu-id="b1f5f-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1f5f-115">-ApiVersion</span></span>
<span data-ttu-id="b1f5f-116">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b1f5f-117">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b1f5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f5f-118">-DefaultProfile</span></span>
<span data-ttu-id="b1f5f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b1f5f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1f5f-120">-描述</span><span class="sxs-lookup"><span data-stu-id="b1f5f-120">-Description</span></span>
<span data-ttu-id="b1f5f-121">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f5f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b1f5f-122">-DisplayName</span></span>
<span data-ttu-id="b1f5f-123">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f5f-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b1f5f-124">-Id</span></span>
<span data-ttu-id="b1f5f-125">完全合格的原則定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="b1f5f-126">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b1f5f-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f5f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1f5f-127">-Name</span></span>
<span data-ttu-id="b1f5f-128">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f5f-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b1f5f-129">-PolicyDefinition</span></span>
<span data-ttu-id="b1f5f-130">原則集定義。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-130">The policy set definition.</span></span> <span data-ttu-id="b1f5f-131">這可以是包含原則定義的檔案名路徑，或原則集定義（字串）。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f5f-132">-預先</span><span class="sxs-lookup"><span data-stu-id="b1f5f-132">-Pre</span></span>
<span data-ttu-id="b1f5f-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b1f5f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b1f5f-134">-Confirm</span></span>
<span data-ttu-id="b1f5f-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f5f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f5f-136">-WhatIf</span></span>
<span data-ttu-id="b1f5f-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1f5f-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f5f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f5f-139">CommonParameters</span></span>
<span data-ttu-id="b1f5f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f5f-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1f5f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f5f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b1f5f-142">INPUTS</span></span>

### <span data-ttu-id="b1f5f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b1f5f-143">System.String</span></span>

## <span data-ttu-id="b1f5f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b1f5f-144">OUTPUTS</span></span>

### <span data-ttu-id="b1f5f-145">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="b1f5f-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b1f5f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b1f5f-146">NOTES</span></span>

## <span data-ttu-id="b1f5f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1f5f-147">RELATED LINKS</span></span>
