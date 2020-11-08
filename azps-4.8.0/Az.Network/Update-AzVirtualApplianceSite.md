---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135755"
---
# <span data-ttu-id="8d09a-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8d09a-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="8d09a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d09a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d09a-103">變更或修改連線至網路虛擬裝置資源的虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="8d09a-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8d09a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d09a-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d09a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d09a-105">DESCRIPTION</span></span>
<span data-ttu-id="8d09a-106">[Update-AzVirtualApplianceSite] 命令會修改虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="8d09a-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="8d09a-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d09a-107">EXAMPLES</span></span>

### <span data-ttu-id="8d09a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8d09a-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="8d09a-109">修改虛擬裝置網站資源的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="8d09a-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="8d09a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d09a-110">PARAMETERS</span></span>

### <span data-ttu-id="8d09a-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="8d09a-111">-AddresssPrefix</span></span>
<span data-ttu-id="8d09a-112">網站的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="8d09a-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d09a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d09a-113">-AsJob</span></span>
<span data-ttu-id="8d09a-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8d09a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d09a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d09a-115">-DefaultProfile</span></span>
<span data-ttu-id="8d09a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d09a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d09a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8d09a-117">-Force</span></span>
<span data-ttu-id="8d09a-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="8d09a-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8d09a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d09a-119">-Name</span></span>
<span data-ttu-id="8d09a-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8d09a-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d09a-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="8d09a-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="8d09a-122">此網站附加的網路虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="8d09a-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="8d09a-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="8d09a-123">-O365Policy</span></span>
<span data-ttu-id="8d09a-124">Office 365 的 [專題討論] 原則。</span><span class="sxs-lookup"><span data-stu-id="8d09a-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d09a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d09a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d09a-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d09a-126">The resource group name.</span></span>

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

### <span data-ttu-id="8d09a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d09a-127">-Tag</span></span>
<span data-ttu-id="8d09a-128">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="8d09a-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8d09a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="8d09a-129">-Confirm</span></span>
<span data-ttu-id="8d09a-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d09a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d09a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d09a-131">-WhatIf</span></span>
<span data-ttu-id="8d09a-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d09a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d09a-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d09a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d09a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d09a-134">CommonParameters</span></span>
<span data-ttu-id="8d09a-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d09a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d09a-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d09a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d09a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8d09a-137">INPUTS</span></span>

### <span data-ttu-id="8d09a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="8d09a-138">System.String</span></span>

### <span data-ttu-id="8d09a-139">PSOffice365PolicyProperties 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d09a-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="8d09a-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d09a-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8d09a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8d09a-141">OUTPUTS</span></span>

### <span data-ttu-id="8d09a-142">PSVirtualApplianceSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d09a-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="8d09a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8d09a-143">NOTES</span></span>

## <span data-ttu-id="8d09a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d09a-144">RELATED LINKS</span></span>
