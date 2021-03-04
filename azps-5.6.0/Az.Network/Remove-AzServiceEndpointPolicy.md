---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 95da37a36c8a97bf507ec8d191728b34a88a25a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915990"
---
# <span data-ttu-id="f9dcf-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dcf-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="f9dcf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dcf-103">移除服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="f9dcf-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9dcf-104">SYNTAX</span></span>

### <span data-ttu-id="f9dcf-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9dcf-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9dcf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9dcf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9dcf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9dcf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9dcf-108">描述</span><span class="sxs-lookup"><span data-stu-id="f9dcf-108">DESCRIPTION</span></span>
<span data-ttu-id="f9dcf-109">**Remove-AzServiceEndpointPolicy** Cmdlet 會移除服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="f9dcf-110">例子</span><span class="sxs-lookup"><span data-stu-id="f9dcf-110">EXAMPLES</span></span>

### <span data-ttu-id="f9dcf-111">範例 1：使用名稱移除服務端點策略</span><span class="sxs-lookup"><span data-stu-id="f9dcf-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="f9dcf-112">此命令會移除名稱為 Policy1 的服務端點策略，該名稱屬於名稱為"resourcegroup1" 的資源組</span><span class="sxs-lookup"><span data-stu-id="f9dcf-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="f9dcf-113">範例 2：使用輸入物件移除服務端點策略</span><span class="sxs-lookup"><span data-stu-id="f9dcf-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="f9dcf-114">此命令會移除服務端點策略物件 Policy1，該物件屬於名稱為 "resourcegroup1" 的資源組</span><span class="sxs-lookup"><span data-stu-id="f9dcf-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="f9dcf-115">參數</span><span class="sxs-lookup"><span data-stu-id="f9dcf-115">PARAMETERS</span></span>

### <span data-ttu-id="f9dcf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dcf-116">-DefaultProfile</span></span>
<span data-ttu-id="f9dcf-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9dcf-118">-強制</span><span class="sxs-lookup"><span data-stu-id="f9dcf-118">-Force</span></span>
<span data-ttu-id="f9dcf-119">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="f9dcf-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f9dcf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9dcf-120">-InputObject</span></span>
<span data-ttu-id="f9dcf-121">服務端點策略物件。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="f9dcf-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9dcf-122">-Name</span></span>
<span data-ttu-id="f9dcf-123">服務端點策略的名稱</span><span class="sxs-lookup"><span data-stu-id="f9dcf-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="f9dcf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9dcf-124">-PassThru</span></span>
<span data-ttu-id="f9dcf-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="f9dcf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dcf-126">-ResourceGroupName</span></span>
<span data-ttu-id="f9dcf-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-127">The resource group name.</span></span>

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

### <span data-ttu-id="f9dcf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9dcf-128">-ResourceId</span></span>
<span data-ttu-id="f9dcf-129">服務端點策略的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="f9dcf-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f9dcf-130">-Confirm</span></span>
<span data-ttu-id="f9dcf-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9dcf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9dcf-132">-WhatIf</span></span>
<span data-ttu-id="f9dcf-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9dcf-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9dcf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dcf-135">CommonParameters</span></span>
<span data-ttu-id="f9dcf-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dcf-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dcf-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f9dcf-138">INPUTS</span></span>

### <span data-ttu-id="f9dcf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f9dcf-139">System.String</span></span>

### <span data-ttu-id="f9dcf-140">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dcf-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f9dcf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f9dcf-141">OUTPUTS</span></span>

### <span data-ttu-id="f9dcf-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9dcf-142">System.Boolean</span></span>

## <span data-ttu-id="f9dcf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f9dcf-143">NOTES</span></span>

## <span data-ttu-id="f9dcf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9dcf-144">RELATED LINKS</span></span>

[<span data-ttu-id="f9dcf-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dcf-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f9dcf-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dcf-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f9dcf-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dcf-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
