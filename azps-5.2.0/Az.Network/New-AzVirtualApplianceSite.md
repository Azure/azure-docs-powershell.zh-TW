---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275428"
---
# <span data-ttu-id="af5b0-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="af5b0-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="af5b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="af5b0-103">建立連線至網路虛擬裝置的網站。</span><span class="sxs-lookup"><span data-stu-id="af5b0-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="af5b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="af5b0-104">SYNTAX</span></span>

### <span data-ttu-id="af5b0-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="af5b0-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5b0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af5b0-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af5b0-107">說明</span><span class="sxs-lookup"><span data-stu-id="af5b0-107">DESCRIPTION</span></span>
<span data-ttu-id="af5b0-108">New-AzVirtualApplianceSite 命令會建立連線至網路虛擬裝置資源的虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="af5b0-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="af5b0-109">示例</span><span class="sxs-lookup"><span data-stu-id="af5b0-109">EXAMPLES</span></span>

### <span data-ttu-id="af5b0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="af5b0-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="af5b0-111">在 [資源群組] 中建立新的虛擬裝置網站： testrg。</span><span class="sxs-lookup"><span data-stu-id="af5b0-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="af5b0-112">參數</span><span class="sxs-lookup"><span data-stu-id="af5b0-112">PARAMETERS</span></span>

### <span data-ttu-id="af5b0-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="af5b0-113">-AddressPrefix</span></span>
<span data-ttu-id="af5b0-114">網站的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="af5b0-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="af5b0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af5b0-115">-AsJob</span></span>
<span data-ttu-id="af5b0-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="af5b0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af5b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5b0-117">-DefaultProfile</span></span>
<span data-ttu-id="af5b0-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af5b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af5b0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="af5b0-119">-Force</span></span>
<span data-ttu-id="af5b0-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="af5b0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="af5b0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="af5b0-121">-Name</span></span>
<span data-ttu-id="af5b0-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="af5b0-122">The resource name.</span></span>

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

### <span data-ttu-id="af5b0-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="af5b0-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="af5b0-124">此網站附加的網路虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="af5b0-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="af5b0-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="af5b0-125">-O365Policy</span></span>
<span data-ttu-id="af5b0-126">Office 365 的 [專題討論] 原則。</span><span class="sxs-lookup"><span data-stu-id="af5b0-126">The Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="af5b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af5b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="af5b0-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af5b0-128">The resource group name.</span></span>

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

### <span data-ttu-id="af5b0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af5b0-129">-ResourceId</span></span>
<span data-ttu-id="af5b0-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="af5b0-130">The resource id.</span></span>

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

### <span data-ttu-id="af5b0-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="af5b0-131">-Tag</span></span>
<span data-ttu-id="af5b0-132">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="af5b0-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="af5b0-133">-確認</span><span class="sxs-lookup"><span data-stu-id="af5b0-133">-Confirm</span></span>
<span data-ttu-id="af5b0-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af5b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af5b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af5b0-135">-WhatIf</span></span>
<span data-ttu-id="af5b0-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af5b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af5b0-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af5b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af5b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5b0-138">CommonParameters</span></span>
<span data-ttu-id="af5b0-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af5b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5b0-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af5b0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5b0-141">輸入</span><span class="sxs-lookup"><span data-stu-id="af5b0-141">INPUTS</span></span>

### <span data-ttu-id="af5b0-142">System.object</span><span class="sxs-lookup"><span data-stu-id="af5b0-142">System.String</span></span>

### <span data-ttu-id="af5b0-143">PSOffice365PolicyProperties 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af5b0-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="af5b0-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="af5b0-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="af5b0-145">輸出</span><span class="sxs-lookup"><span data-stu-id="af5b0-145">OUTPUTS</span></span>

### <span data-ttu-id="af5b0-146">PSVirtualApplianceSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af5b0-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="af5b0-147">筆記</span><span class="sxs-lookup"><span data-stu-id="af5b0-147">NOTES</span></span>

## <span data-ttu-id="af5b0-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="af5b0-148">RELATED LINKS</span></span>
