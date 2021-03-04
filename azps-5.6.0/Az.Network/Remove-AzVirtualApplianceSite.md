---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 1456acb101302297e807d6d46bf83183e8a6e523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915985"
---
# <span data-ttu-id="8293c-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8293c-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="8293c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8293c-102">SYNOPSIS</span></span>
<span data-ttu-id="8293c-103">從網路虛擬裝置資源移除虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="8293c-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8293c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8293c-104">SYNTAX</span></span>

### <span data-ttu-id="8293c-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8293c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8293c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8293c-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8293c-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8293c-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8293c-108">描述</span><span class="sxs-lookup"><span data-stu-id="8293c-108">DESCRIPTION</span></span>
<span data-ttu-id="8293c-109">Remove-AzVirtualApplianceSite命令會從網路虛擬裝置資源移除虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="8293c-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8293c-110">例子</span><span class="sxs-lookup"><span data-stu-id="8293c-110">EXAMPLES</span></span>

### <span data-ttu-id="8293c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8293c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="8293c-112">刪除虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="8293c-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="8293c-113">參數</span><span class="sxs-lookup"><span data-stu-id="8293c-113">PARAMETERS</span></span>

### <span data-ttu-id="8293c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8293c-114">-AsJob</span></span>
<span data-ttu-id="8293c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8293c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8293c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8293c-116">-DefaultProfile</span></span>
<span data-ttu-id="8293c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8293c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8293c-118">-強制</span><span class="sxs-lookup"><span data-stu-id="8293c-118">-Force</span></span>
<span data-ttu-id="8293c-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="8293c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8293c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8293c-120">-Name</span></span>
<span data-ttu-id="8293c-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8293c-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8293c-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="8293c-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="8293c-123">與此網站相關聯的網路虛擬裝置資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8293c-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8293c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8293c-124">-PassThru</span></span>
<span data-ttu-id="8293c-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8293c-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8293c-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8293c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8293c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8293c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8293c-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8293c-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8293c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8293c-129">-ResourceId</span></span>
<span data-ttu-id="8293c-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8293c-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8293c-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8293c-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="8293c-132">虛擬裝置網站物件。</span><span class="sxs-lookup"><span data-stu-id="8293c-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8293c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8293c-133">-Confirm</span></span>
<span data-ttu-id="8293c-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8293c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8293c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8293c-135">-WhatIf</span></span>
<span data-ttu-id="8293c-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8293c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8293c-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8293c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8293c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8293c-138">CommonParameters</span></span>
<span data-ttu-id="8293c-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8293c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8293c-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8293c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8293c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8293c-141">INPUTS</span></span>

### <span data-ttu-id="8293c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8293c-142">System.String</span></span>

### <span data-ttu-id="8293c-143">Microsoft.Azure.Commands.Network.models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8293c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="8293c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8293c-144">OUTPUTS</span></span>

### <span data-ttu-id="8293c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8293c-145">System.Boolean</span></span>

## <span data-ttu-id="8293c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="8293c-146">NOTES</span></span>

## <span data-ttu-id="8293c-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="8293c-147">RELATED LINKS</span></span>
