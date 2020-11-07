---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965437"
---
# <span data-ttu-id="9f055-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9f055-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="9f055-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f055-102">SYNOPSIS</span></span>
<span data-ttu-id="9f055-103">移除服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="9f055-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="9f055-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f055-104">SYNTAX</span></span>

### <span data-ttu-id="9f055-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9f055-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f055-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f055-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f055-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f055-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f055-108">說明</span><span class="sxs-lookup"><span data-stu-id="9f055-108">DESCRIPTION</span></span>
<span data-ttu-id="9f055-109">**AzServiceEndpointPolicy** Cmdlet 會移除服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="9f055-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="9f055-110">示例</span><span class="sxs-lookup"><span data-stu-id="9f055-110">EXAMPLES</span></span>

### <span data-ttu-id="9f055-111">範例1：使用名稱移除服務端點原則</span><span class="sxs-lookup"><span data-stu-id="9f055-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="9f055-112">這個命令會移除名稱 Policy1 的服務端點原則，名稱為 "resourcegroup1" 的 resourcegroup</span><span class="sxs-lookup"><span data-stu-id="9f055-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="9f055-113">範例2：使用輸入物件移除服務端點原則</span><span class="sxs-lookup"><span data-stu-id="9f055-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="9f055-114">這個命令會移除屬於名為 "resourcegroup1" 的 resourcegroup 的服務端點原則物件 Policy1</span><span class="sxs-lookup"><span data-stu-id="9f055-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="9f055-115">參數</span><span class="sxs-lookup"><span data-stu-id="9f055-115">PARAMETERS</span></span>

### <span data-ttu-id="9f055-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f055-116">-DefaultProfile</span></span>
<span data-ttu-id="9f055-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f055-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f055-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9f055-118">-Force</span></span>
<span data-ttu-id="9f055-119">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="9f055-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9f055-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f055-120">-InputObject</span></span>
<span data-ttu-id="9f055-121">服務端點原則物件。</span><span class="sxs-lookup"><span data-stu-id="9f055-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f055-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f055-122">-Name</span></span>
<span data-ttu-id="9f055-123">服務端點原則的名稱</span><span class="sxs-lookup"><span data-stu-id="9f055-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f055-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f055-124">-PassThru</span></span>
<span data-ttu-id="9f055-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9f055-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="9f055-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f055-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f055-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f055-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f055-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f055-128">-ResourceId</span></span>
<span data-ttu-id="9f055-129">服務端點原則的 ID。</span><span class="sxs-lookup"><span data-stu-id="9f055-129">The ID of service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f055-130">-確認</span><span class="sxs-lookup"><span data-stu-id="9f055-130">-Confirm</span></span>
<span data-ttu-id="9f055-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9f055-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f055-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f055-132">-WhatIf</span></span>
<span data-ttu-id="9f055-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f055-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f055-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f055-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f055-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f055-135">CommonParameters</span></span>
<span data-ttu-id="9f055-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f055-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f055-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f055-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f055-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9f055-138">INPUTS</span></span>

### <span data-ttu-id="9f055-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9f055-139">System.String</span></span>

### <span data-ttu-id="9f055-140">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9f055-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="9f055-141">輸出</span><span class="sxs-lookup"><span data-stu-id="9f055-141">OUTPUTS</span></span>

### <span data-ttu-id="9f055-142">System.object</span><span class="sxs-lookup"><span data-stu-id="9f055-142">System.Boolean</span></span>

## <span data-ttu-id="9f055-143">筆記</span><span class="sxs-lookup"><span data-stu-id="9f055-143">NOTES</span></span>

## <span data-ttu-id="9f055-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f055-144">RELATED LINKS</span></span>

[<span data-ttu-id="9f055-145">AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9f055-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="9f055-146">新-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9f055-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="9f055-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9f055-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
