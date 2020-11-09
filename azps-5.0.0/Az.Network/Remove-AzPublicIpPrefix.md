---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286816"
---
# <span data-ttu-id="b8604-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8604-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="b8604-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8604-102">SYNOPSIS</span></span>
<span data-ttu-id="b8604-103">移除公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="b8604-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="b8604-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8604-104">SYNTAX</span></span>

### <span data-ttu-id="b8604-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b8604-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8604-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8604-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8604-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8604-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8604-108">說明</span><span class="sxs-lookup"><span data-stu-id="b8604-108">DESCRIPTION</span></span>
<span data-ttu-id="b8604-109">只要沒有指派公用 IP 位址， **AzPublicIpPrefix** Cmdlet 就會移除 AZURE 公用 ip 首碼。</span><span class="sxs-lookup"><span data-stu-id="b8604-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="b8604-110">示例</span><span class="sxs-lookup"><span data-stu-id="b8604-110">EXAMPLES</span></span>

### <span data-ttu-id="b8604-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b8604-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="b8604-112">從 [資源群組] $rgName 移除名稱 $prefixName 的公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="b8604-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="b8604-113">參數</span><span class="sxs-lookup"><span data-stu-id="b8604-113">PARAMETERS</span></span>

### <span data-ttu-id="b8604-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8604-114">-AsJob</span></span>
<span data-ttu-id="b8604-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8604-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8604-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8604-116">-DefaultProfile</span></span>
<span data-ttu-id="b8604-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8604-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8604-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b8604-118">-Force</span></span>
<span data-ttu-id="b8604-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b8604-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b8604-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8604-120">-InputObject</span></span>
<span data-ttu-id="b8604-121">PublicIpPrefix 物件</span><span class="sxs-lookup"><span data-stu-id="b8604-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="b8604-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8604-122">-Name</span></span>
<span data-ttu-id="b8604-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b8604-123">The resource name.</span></span>

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

### <span data-ttu-id="b8604-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8604-124">-PassThru</span></span>
<span data-ttu-id="b8604-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b8604-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b8604-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b8604-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b8604-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8604-127">-ResourceGroupName</span></span>
<span data-ttu-id="b8604-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8604-128">The resource group name.</span></span>

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

### <span data-ttu-id="b8604-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8604-129">-ResourceId</span></span>
<span data-ttu-id="b8604-130">要移除之資源的 resourceId</span><span class="sxs-lookup"><span data-stu-id="b8604-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="b8604-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b8604-131">-Confirm</span></span>
<span data-ttu-id="b8604-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8604-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8604-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8604-133">-WhatIf</span></span>
<span data-ttu-id="b8604-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8604-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8604-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8604-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8604-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8604-136">CommonParameters</span></span>
<span data-ttu-id="b8604-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8604-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8604-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8604-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8604-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b8604-139">INPUTS</span></span>

### <span data-ttu-id="b8604-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b8604-140">System.String</span></span>

### <span data-ttu-id="b8604-141">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8604-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="b8604-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b8604-142">OUTPUTS</span></span>

### <span data-ttu-id="b8604-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b8604-143">System.Boolean</span></span>

## <span data-ttu-id="b8604-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b8604-144">NOTES</span></span>

## <span data-ttu-id="b8604-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8604-145">RELATED LINKS</span></span>

[<span data-ttu-id="b8604-146">AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8604-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="b8604-147">新-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8604-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="b8604-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8604-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
