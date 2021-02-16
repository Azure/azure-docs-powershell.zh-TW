---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135771"
---
# <span data-ttu-id="29324-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="29324-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="29324-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29324-102">SYNOPSIS</span></span>
<span data-ttu-id="29324-103">刪除 Azure IpGroup。</span><span class="sxs-lookup"><span data-stu-id="29324-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="29324-104">句法</span><span class="sxs-lookup"><span data-stu-id="29324-104">SYNTAX</span></span>

### <span data-ttu-id="29324-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29324-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29324-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29324-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29324-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29324-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29324-108">說明</span><span class="sxs-lookup"><span data-stu-id="29324-108">DESCRIPTION</span></span>
<span data-ttu-id="29324-109">**AzIpGroup** Cmdlet 會刪除 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="29324-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="29324-110">示例</span><span class="sxs-lookup"><span data-stu-id="29324-110">EXAMPLES</span></span>

### <span data-ttu-id="29324-111">範例1</span><span class="sxs-lookup"><span data-stu-id="29324-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="29324-112">範例2</span><span class="sxs-lookup"><span data-stu-id="29324-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="29324-113">範例3</span><span class="sxs-lookup"><span data-stu-id="29324-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="29324-114">參數</span><span class="sxs-lookup"><span data-stu-id="29324-114">PARAMETERS</span></span>

### <span data-ttu-id="29324-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29324-115">-AsJob</span></span>
<span data-ttu-id="29324-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="29324-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29324-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29324-117">-DefaultProfile</span></span>
<span data-ttu-id="29324-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29324-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29324-119">-Force</span><span class="sxs-lookup"><span data-stu-id="29324-119">-Force</span></span>
<span data-ttu-id="29324-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="29324-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="29324-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="29324-121">-IpGroup</span></span>
<span data-ttu-id="29324-122">IpGroup 輸入物件。</span><span class="sxs-lookup"><span data-stu-id="29324-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29324-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="29324-123">-Name</span></span>
<span data-ttu-id="29324-124">Ipgroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="29324-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29324-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29324-125">-PassThru</span></span>
<span data-ttu-id="29324-126">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="29324-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="29324-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29324-127">-ResourceGroupName</span></span>
<span data-ttu-id="29324-128">Ipgroup 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="29324-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29324-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29324-129">-ResourceId</span></span>
<span data-ttu-id="29324-130">Ipgroup 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29324-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29324-131">-確認</span><span class="sxs-lookup"><span data-stu-id="29324-131">-Confirm</span></span>
<span data-ttu-id="29324-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29324-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29324-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29324-133">-WhatIf</span></span>
<span data-ttu-id="29324-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29324-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29324-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29324-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29324-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29324-136">CommonParameters</span></span>
<span data-ttu-id="29324-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29324-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29324-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29324-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29324-139">輸入</span><span class="sxs-lookup"><span data-stu-id="29324-139">INPUTS</span></span>

### <span data-ttu-id="29324-140">System.object</span><span class="sxs-lookup"><span data-stu-id="29324-140">System.String</span></span>

### <span data-ttu-id="29324-141">PSIpGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29324-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="29324-142">輸出</span><span class="sxs-lookup"><span data-stu-id="29324-142">OUTPUTS</span></span>

### <span data-ttu-id="29324-143">System.object</span><span class="sxs-lookup"><span data-stu-id="29324-143">System.Boolean</span></span>

## <span data-ttu-id="29324-144">筆記</span><span class="sxs-lookup"><span data-stu-id="29324-144">NOTES</span></span>

## <span data-ttu-id="29324-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="29324-145">RELATED LINKS</span></span>
