---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970323"
---
# <span data-ttu-id="8597d-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8597d-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="8597d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8597d-102">SYNOPSIS</span></span>
<span data-ttu-id="8597d-103">從網路虛擬裝置資源移除虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="8597d-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8597d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8597d-104">SYNTAX</span></span>

### <span data-ttu-id="8597d-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8597d-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8597d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8597d-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8597d-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8597d-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8597d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8597d-108">DESCRIPTION</span></span>
<span data-ttu-id="8597d-109">[Remove-AzVirtualApplianceSite] 命令會從網路虛擬裝置資源移除虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="8597d-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8597d-110">示例</span><span class="sxs-lookup"><span data-stu-id="8597d-110">EXAMPLES</span></span>

### <span data-ttu-id="8597d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8597d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="8597d-112">刪除虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="8597d-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="8597d-113">參數</span><span class="sxs-lookup"><span data-stu-id="8597d-113">PARAMETERS</span></span>

### <span data-ttu-id="8597d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8597d-114">-AsJob</span></span>
<span data-ttu-id="8597d-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8597d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8597d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8597d-116">-DefaultProfile</span></span>
<span data-ttu-id="8597d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8597d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8597d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8597d-118">-Force</span></span>
<span data-ttu-id="8597d-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8597d-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8597d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8597d-120">-Name</span></span>
<span data-ttu-id="8597d-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8597d-121">The resource name.</span></span>

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

### <span data-ttu-id="8597d-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="8597d-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="8597d-123">與此網站相關聯之網路虛擬裝置的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8597d-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="8597d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8597d-124">-PassThru</span></span>
<span data-ttu-id="8597d-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8597d-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8597d-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8597d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8597d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8597d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8597d-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8597d-128">The resource group name.</span></span>

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

### <span data-ttu-id="8597d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8597d-129">-ResourceId</span></span>
<span data-ttu-id="8597d-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8597d-130">The resource id.</span></span>

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

### <span data-ttu-id="8597d-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8597d-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="8597d-132">虛擬裝置網站物件。</span><span class="sxs-lookup"><span data-stu-id="8597d-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="8597d-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8597d-133">-Confirm</span></span>
<span data-ttu-id="8597d-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8597d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8597d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8597d-135">-WhatIf</span></span>
<span data-ttu-id="8597d-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8597d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8597d-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8597d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8597d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8597d-138">CommonParameters</span></span>
<span data-ttu-id="8597d-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8597d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8597d-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8597d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8597d-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8597d-141">INPUTS</span></span>

### <span data-ttu-id="8597d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="8597d-142">System.String</span></span>

### <span data-ttu-id="8597d-143">PSVirtualApplianceSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8597d-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="8597d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8597d-144">OUTPUTS</span></span>

### <span data-ttu-id="8597d-145">System.object</span><span class="sxs-lookup"><span data-stu-id="8597d-145">System.Boolean</span></span>

## <span data-ttu-id="8597d-146">筆記</span><span class="sxs-lookup"><span data-stu-id="8597d-146">NOTES</span></span>

## <span data-ttu-id="8597d-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="8597d-147">RELATED LINKS</span></span>