---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284684"
---
# <span data-ttu-id="80261-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="80261-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="80261-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80261-102">SYNOPSIS</span></span>
<span data-ttu-id="80261-103">移除 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="80261-103">Remove WAF policy</span></span>

## <span data-ttu-id="80261-104">句法</span><span class="sxs-lookup"><span data-stu-id="80261-104">SYNTAX</span></span>

### <span data-ttu-id="80261-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="80261-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80261-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80261-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80261-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80261-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80261-108">說明</span><span class="sxs-lookup"><span data-stu-id="80261-108">DESCRIPTION</span></span>
<span data-ttu-id="80261-109">**AzFrontDoorWafPolicy** Cmdlet 會在目前的訂閱底下移除 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="80261-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="80261-110">示例</span><span class="sxs-lookup"><span data-stu-id="80261-110">EXAMPLES</span></span>

### <span data-ttu-id="80261-111">範例1</span><span class="sxs-lookup"><span data-stu-id="80261-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="80261-112">在 $resourceGroupName 中移除稱為 $policyName 的 WAF 原則。</span><span class="sxs-lookup"><span data-stu-id="80261-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="80261-113">範例2</span><span class="sxs-lookup"><span data-stu-id="80261-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="80261-114">移除 $resourceGroupName 中的所有 WAF 原則。</span><span class="sxs-lookup"><span data-stu-id="80261-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="80261-115">參數</span><span class="sxs-lookup"><span data-stu-id="80261-115">PARAMETERS</span></span>

### <span data-ttu-id="80261-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80261-116">-DefaultProfile</span></span>
<span data-ttu-id="80261-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80261-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80261-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80261-118">-InputObject</span></span>
<span data-ttu-id="80261-119">要刪除的 WAF 原則物件。</span><span class="sxs-lookup"><span data-stu-id="80261-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80261-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="80261-120">-Name</span></span>
<span data-ttu-id="80261-121">要刪除之 WAF 原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="80261-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80261-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80261-122">-PassThru</span></span>
<span data-ttu-id="80261-123">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="80261-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="80261-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80261-124">-ResourceGroupName</span></span>
<span data-ttu-id="80261-125">WAF 原則所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="80261-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80261-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80261-126">-ResourceId</span></span>
<span data-ttu-id="80261-127">要刪除之 WAF 原則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="80261-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80261-128">-確認</span><span class="sxs-lookup"><span data-stu-id="80261-128">-Confirm</span></span>
<span data-ttu-id="80261-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80261-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80261-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80261-130">-WhatIf</span></span>
<span data-ttu-id="80261-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80261-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80261-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80261-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80261-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80261-133">CommonParameters</span></span>
<span data-ttu-id="80261-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80261-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80261-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="80261-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80261-136">輸入</span><span class="sxs-lookup"><span data-stu-id="80261-136">INPUTS</span></span>

### <span data-ttu-id="80261-137">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="80261-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="80261-138">System.object</span><span class="sxs-lookup"><span data-stu-id="80261-138">System.String</span></span>

## <span data-ttu-id="80261-139">輸出</span><span class="sxs-lookup"><span data-stu-id="80261-139">OUTPUTS</span></span>

### <span data-ttu-id="80261-140">System.object</span><span class="sxs-lookup"><span data-stu-id="80261-140">System.Boolean</span></span>

## <span data-ttu-id="80261-141">筆記</span><span class="sxs-lookup"><span data-stu-id="80261-141">NOTES</span></span>

## <span data-ttu-id="80261-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="80261-142">RELATED LINKS</span></span>

<span data-ttu-id="80261-143">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="80261-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
