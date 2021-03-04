---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: f3072871caa5449606afe18093a463fea58c6dfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908078"
---
# <span data-ttu-id="2ee4a-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2ee4a-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="2ee4a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ee4a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee4a-103">移除公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="2ee4a-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="2ee4a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ee4a-104">SYNTAX</span></span>

### <span data-ttu-id="2ee4a-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2ee4a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ee4a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee4a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ee4a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee4a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ee4a-108">描述</span><span class="sxs-lookup"><span data-stu-id="2ee4a-108">DESCRIPTION</span></span>
<span data-ttu-id="2ee4a-109">只要未配置任何公用 IP 位址 **，Remove-AzPublicIpPrefix** Cmdlet 會移除 Azure 公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="2ee4a-110">例子</span><span class="sxs-lookup"><span data-stu-id="2ee4a-110">EXAMPLES</span></span>

### <span data-ttu-id="2ee4a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2ee4a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="2ee4a-112">移除資源群組中具有名稱$prefixName的公用 IP 首碼$rgName</span><span class="sxs-lookup"><span data-stu-id="2ee4a-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="2ee4a-113">參數</span><span class="sxs-lookup"><span data-stu-id="2ee4a-113">PARAMETERS</span></span>

### <span data-ttu-id="2ee4a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ee4a-114">-AsJob</span></span>
<span data-ttu-id="2ee4a-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2ee4a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ee4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee4a-116">-DefaultProfile</span></span>
<span data-ttu-id="2ee4a-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee4a-118">-強制</span><span class="sxs-lookup"><span data-stu-id="2ee4a-118">-Force</span></span>
<span data-ttu-id="2ee4a-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2ee4a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ee4a-120">-InputObject</span></span>
<span data-ttu-id="2ee4a-121">PublicIpPrefix 物件</span><span class="sxs-lookup"><span data-stu-id="2ee4a-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee4a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ee4a-122">-Name</span></span>
<span data-ttu-id="2ee4a-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee4a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ee4a-124">-PassThru</span></span>
<span data-ttu-id="2ee4a-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ee4a-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ee4a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee4a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ee4a-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-128">The resource group name.</span></span>

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

### <span data-ttu-id="2ee4a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ee4a-129">-ResourceId</span></span>
<span data-ttu-id="2ee4a-130">要移除之資源的資源Id</span><span class="sxs-lookup"><span data-stu-id="2ee4a-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="2ee4a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="2ee4a-131">-Confirm</span></span>
<span data-ttu-id="2ee4a-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee4a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee4a-133">-WhatIf</span></span>
<span data-ttu-id="2ee4a-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee4a-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee4a-136">CommonParameters</span></span>
<span data-ttu-id="2ee4a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee4a-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2ee4a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee4a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2ee4a-139">INPUTS</span></span>

### <span data-ttu-id="2ee4a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2ee4a-140">System.String</span></span>

### <span data-ttu-id="2ee4a-141">Microsoft.Azure.Commands.Network.models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2ee4a-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="2ee4a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="2ee4a-142">OUTPUTS</span></span>

### <span data-ttu-id="2ee4a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ee4a-143">System.Boolean</span></span>

## <span data-ttu-id="2ee4a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="2ee4a-144">NOTES</span></span>

## <span data-ttu-id="2ee4a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ee4a-145">RELATED LINKS</span></span>

[<span data-ttu-id="2ee4a-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2ee4a-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="2ee4a-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2ee4a-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="2ee4a-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2ee4a-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
