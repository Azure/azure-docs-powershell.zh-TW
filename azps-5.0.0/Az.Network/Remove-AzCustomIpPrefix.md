---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139690"
---
# <span data-ttu-id="975c1-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="975c1-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="975c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="975c1-102">SYNOPSIS</span></span>
<span data-ttu-id="975c1-103">移除 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="975c1-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="975c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="975c1-104">SYNTAX</span></span>

### <span data-ttu-id="975c1-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="975c1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975c1-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="975c1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975c1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="975c1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="975c1-108">說明</span><span class="sxs-lookup"><span data-stu-id="975c1-108">DESCRIPTION</span></span>
<span data-ttu-id="975c1-109">**AzCustomIpPrefix** Cmdlet 會移除 CustomIpPrefix。</span><span class="sxs-lookup"><span data-stu-id="975c1-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="975c1-110">示例</span><span class="sxs-lookup"><span data-stu-id="975c1-110">EXAMPLES</span></span>

### <span data-ttu-id="975c1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="975c1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="975c1-112">從 [資源群組] $rgName 移除名稱 $prefixName 的 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="975c1-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="975c1-113">參數</span><span class="sxs-lookup"><span data-stu-id="975c1-113">PARAMETERS</span></span>

### <span data-ttu-id="975c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="975c1-114">-AsJob</span></span>
<span data-ttu-id="975c1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="975c1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="975c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975c1-116">-DefaultProfile</span></span>
<span data-ttu-id="975c1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="975c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975c1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="975c1-118">-Force</span></span>
<span data-ttu-id="975c1-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="975c1-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="975c1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="975c1-120">-InputObject</span></span>
<span data-ttu-id="975c1-121">CustomIpPrefix 物件。</span><span class="sxs-lookup"><span data-stu-id="975c1-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="975c1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="975c1-122">-Name</span></span>
<span data-ttu-id="975c1-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="975c1-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="975c1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="975c1-124">-PassThru</span></span>
<span data-ttu-id="975c1-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="975c1-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="975c1-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="975c1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="975c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="975c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="975c1-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="975c1-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="975c1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="975c1-129">-ResourceId</span></span>
<span data-ttu-id="975c1-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="975c1-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="975c1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="975c1-131">-Confirm</span></span>
<span data-ttu-id="975c1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="975c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="975c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="975c1-133">-WhatIf</span></span>
<span data-ttu-id="975c1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="975c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="975c1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="975c1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="975c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975c1-136">CommonParameters</span></span>
<span data-ttu-id="975c1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="975c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975c1-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="975c1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975c1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="975c1-139">INPUTS</span></span>

### <span data-ttu-id="975c1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="975c1-140">System.String</span></span>

### <span data-ttu-id="975c1-141">PSCustomIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="975c1-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="975c1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="975c1-142">OUTPUTS</span></span>

### <span data-ttu-id="975c1-143">System.object</span><span class="sxs-lookup"><span data-stu-id="975c1-143">System.Boolean</span></span>

## <span data-ttu-id="975c1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="975c1-144">NOTES</span></span>

## <span data-ttu-id="975c1-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="975c1-145">RELATED LINKS</span></span>

[<span data-ttu-id="975c1-146">AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="975c1-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="975c1-147">新-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="975c1-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="975c1-148">更新-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="975c1-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)