---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: e27d956f8530fb45f5927ece22302d21acafc503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904017"
---
# <span data-ttu-id="3ab99-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3ab99-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="3ab99-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ab99-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab99-103">建立連接至網路虛擬裝置的網站。</span><span class="sxs-lookup"><span data-stu-id="3ab99-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="3ab99-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ab99-104">SYNTAX</span></span>

### <span data-ttu-id="3ab99-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3ab99-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab99-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ab99-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab99-107">描述</span><span class="sxs-lookup"><span data-stu-id="3ab99-107">DESCRIPTION</span></span>
<span data-ttu-id="3ab99-108">New-AzVirtualApplianceSite命令會建立一個連接至網路虛擬裝置資源的虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="3ab99-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3ab99-109">例子</span><span class="sxs-lookup"><span data-stu-id="3ab99-109">EXAMPLES</span></span>

### <span data-ttu-id="3ab99-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3ab99-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="3ab99-111">在資源群組中建立新虛擬裝置網站：testrg。</span><span class="sxs-lookup"><span data-stu-id="3ab99-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="3ab99-112">參數</span><span class="sxs-lookup"><span data-stu-id="3ab99-112">PARAMETERS</span></span>

### <span data-ttu-id="3ab99-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3ab99-113">-AddressPrefix</span></span>
<span data-ttu-id="3ab99-114">網站的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="3ab99-114">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab99-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ab99-115">-AsJob</span></span>
<span data-ttu-id="3ab99-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3ab99-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ab99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab99-117">-DefaultProfile</span></span>
<span data-ttu-id="3ab99-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ab99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab99-119">-強制</span><span class="sxs-lookup"><span data-stu-id="3ab99-119">-Force</span></span>
<span data-ttu-id="3ab99-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="3ab99-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3ab99-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ab99-121">-Name</span></span>
<span data-ttu-id="3ab99-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3ab99-122">The resource name.</span></span>

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

### <span data-ttu-id="3ab99-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="3ab99-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="3ab99-124">此網站所附加的網路虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="3ab99-124">The Network virtual appliance that this site is attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab99-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="3ab99-125">-O365Policy</span></span>
<span data-ttu-id="3ab99-126">Office 365 中斷群組原則。</span><span class="sxs-lookup"><span data-stu-id="3ab99-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab99-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab99-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ab99-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3ab99-128">The resource group name.</span></span>

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

### <span data-ttu-id="3ab99-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ab99-129">-ResourceId</span></span>
<span data-ttu-id="3ab99-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ab99-130">The resource id.</span></span>

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

### <span data-ttu-id="3ab99-131">-標記</span><span class="sxs-lookup"><span data-stu-id="3ab99-131">-Tag</span></span>
<span data-ttu-id="3ab99-132">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3ab99-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab99-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3ab99-133">-Confirm</span></span>
<span data-ttu-id="3ab99-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3ab99-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab99-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab99-135">-WhatIf</span></span>
<span data-ttu-id="3ab99-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ab99-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab99-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ab99-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab99-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab99-138">CommonParameters</span></span>
<span data-ttu-id="3ab99-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ab99-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab99-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ab99-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab99-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3ab99-141">INPUTS</span></span>

### <span data-ttu-id="3ab99-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3ab99-142">System.String</span></span>

### <span data-ttu-id="3ab99-143">Microsoft.Azure.Commands.Network.models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="3ab99-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="3ab99-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ab99-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3ab99-145">輸出</span><span class="sxs-lookup"><span data-stu-id="3ab99-145">OUTPUTS</span></span>

### <span data-ttu-id="3ab99-146">Microsoft.Azure.Commands.Network.models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3ab99-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="3ab99-147">筆記</span><span class="sxs-lookup"><span data-stu-id="3ab99-147">NOTES</span></span>

## <span data-ttu-id="3ab99-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ab99-148">RELATED LINKS</span></span>
