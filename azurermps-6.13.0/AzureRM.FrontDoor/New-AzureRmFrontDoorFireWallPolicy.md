---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456076"
---
# <span data-ttu-id="42d01-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="42d01-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="42d01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42d01-102">SYNOPSIS</span></span>
<span data-ttu-id="42d01-103">建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="42d01-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42d01-104">句法</span><span class="sxs-lookup"><span data-stu-id="42d01-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d01-105">說明</span><span class="sxs-lookup"><span data-stu-id="42d01-105">DESCRIPTION</span></span>
<span data-ttu-id="42d01-106">**AzureRmFrontDoorFireWallPolicy** Cmdlet 會在指定的資源群組中，在 [目前訂閱] 底下建立新的 Azure WAF 原則</span><span class="sxs-lookup"><span data-stu-id="42d01-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="42d01-107">示例</span><span class="sxs-lookup"><span data-stu-id="42d01-107">EXAMPLES</span></span>

### <span data-ttu-id="42d01-108">範例1：建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="42d01-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="42d01-109">建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="42d01-109">Create WAF policy</span></span>

## <span data-ttu-id="42d01-110">參數</span><span class="sxs-lookup"><span data-stu-id="42d01-110">PARAMETERS</span></span>

### <span data-ttu-id="42d01-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="42d01-111">-Customrule</span></span>
<span data-ttu-id="42d01-112">原則內的自訂規則</span><span class="sxs-lookup"><span data-stu-id="42d01-112">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d01-113">-DefaultProfile</span></span>
<span data-ttu-id="42d01-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42d01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d01-115">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="42d01-115">-EnabledState</span></span>
<span data-ttu-id="42d01-116">原則處於 [啟用] 狀態或 [已停用] 狀態。</span><span class="sxs-lookup"><span data-stu-id="42d01-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="42d01-117">可能的值包括：「已停用」、「已啟用」</span><span class="sxs-lookup"><span data-stu-id="42d01-117">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d01-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="42d01-118">-ManagedRule</span></span>
<span data-ttu-id="42d01-119">原則中的受管理規則</span><span class="sxs-lookup"><span data-stu-id="42d01-119">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d01-120">模式</span><span class="sxs-lookup"><span data-stu-id="42d01-120">-Mode</span></span>
<span data-ttu-id="42d01-121">描述它是否在策略層級的偵測模式或預防模式中。</span><span class="sxs-lookup"><span data-stu-id="42d01-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="42d01-122">可能的值包括：「預防」、「偵測」</span><span class="sxs-lookup"><span data-stu-id="42d01-122">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d01-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="42d01-123">-Name</span></span>
<span data-ttu-id="42d01-124">WebApplicationFireWallPolicy [名稱]。</span><span class="sxs-lookup"><span data-stu-id="42d01-124">WebApplicationFireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d01-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d01-125">-ResourceGroupName</span></span>
<span data-ttu-id="42d01-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="42d01-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d01-127">-確認</span><span class="sxs-lookup"><span data-stu-id="42d01-127">-Confirm</span></span>
<span data-ttu-id="42d01-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42d01-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d01-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d01-129">-WhatIf</span></span>
<span data-ttu-id="42d01-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42d01-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d01-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42d01-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d01-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d01-132">CommonParameters</span></span>
<span data-ttu-id="42d01-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42d01-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d01-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42d01-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d01-135">輸入</span><span class="sxs-lookup"><span data-stu-id="42d01-135">INPUTS</span></span>

### <span data-ttu-id="42d01-136">System.object</span><span class="sxs-lookup"><span data-stu-id="42d01-136">System.String</span></span>

## <span data-ttu-id="42d01-137">輸出</span><span class="sxs-lookup"><span data-stu-id="42d01-137">OUTPUTS</span></span>

### <span data-ttu-id="42d01-138">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="42d01-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="42d01-139">筆記</span><span class="sxs-lookup"><span data-stu-id="42d01-139">NOTES</span></span>

## <span data-ttu-id="42d01-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="42d01-140">RELATED LINKS</span></span>

<span data-ttu-id="42d01-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
[AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
[移除-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
[新-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
[新-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="42d01-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
