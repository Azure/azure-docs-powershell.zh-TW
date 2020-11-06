---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450504"
---
# <span data-ttu-id="ec38e-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ec38e-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="ec38e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec38e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec38e-103">移除原則集定義。</span><span class="sxs-lookup"><span data-stu-id="ec38e-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec38e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec38e-104">SYNTAX</span></span>

### <span data-ttu-id="ec38e-105">RemoveByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="ec38e-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec38e-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="ec38e-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec38e-107">說明</span><span class="sxs-lookup"><span data-stu-id="ec38e-107">DESCRIPTION</span></span>
<span data-ttu-id="ec38e-108">**AzureRmPolicySetDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="ec38e-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="ec38e-109">示例</span><span class="sxs-lookup"><span data-stu-id="ec38e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec38e-110">範例1：按照資源識別碼移除原則集定義</span><span class="sxs-lookup"><span data-stu-id="ec38e-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="ec38e-111">第一個命令會使用 Get-AzureRmPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="ec38e-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ec38e-112">該命令會將它儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="ec38e-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="ec38e-113">第二個命令會移除由 $PolicySetDefinition 的 **ResourceId** 屬性所識別的原則集定義。</span><span class="sxs-lookup"><span data-stu-id="ec38e-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="ec38e-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec38e-114">PARAMETERS</span></span>

### <span data-ttu-id="ec38e-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ec38e-115">-ApiVersion</span></span>
<span data-ttu-id="ec38e-116">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ec38e-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ec38e-117">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="ec38e-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ec38e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec38e-118">-DefaultProfile</span></span>
<span data-ttu-id="ec38e-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ec38e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec38e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ec38e-120">-Force</span></span>
<span data-ttu-id="ec38e-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ec38e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ec38e-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ec38e-122">-Id</span></span>
<span data-ttu-id="ec38e-123">完全限定的原則集定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec38e-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="ec38e-124">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ec38e-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec38e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec38e-125">-Name</span></span>
<span data-ttu-id="ec38e-126">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ec38e-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec38e-127">-預先</span><span class="sxs-lookup"><span data-stu-id="ec38e-127">-Pre</span></span>
<span data-ttu-id="ec38e-128">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="ec38e-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ec38e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ec38e-129">-Confirm</span></span>
<span data-ttu-id="ec38e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec38e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec38e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec38e-131">-WhatIf</span></span>
<span data-ttu-id="ec38e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec38e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec38e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec38e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec38e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec38e-134">CommonParameters</span></span>
<span data-ttu-id="ec38e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec38e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec38e-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec38e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec38e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ec38e-137">INPUTS</span></span>

### <span data-ttu-id="ec38e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ec38e-138">System.String</span></span>

## <span data-ttu-id="ec38e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ec38e-139">OUTPUTS</span></span>

### <span data-ttu-id="ec38e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ec38e-140">System.Boolean</span></span>

## <span data-ttu-id="ec38e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ec38e-141">NOTES</span></span>

## <span data-ttu-id="ec38e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec38e-142">RELATED LINKS</span></span>
