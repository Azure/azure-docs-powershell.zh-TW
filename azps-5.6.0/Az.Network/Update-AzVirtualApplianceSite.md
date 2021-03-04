---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 7d0d292cb7eba6b776371493e9ceb7e19ef17115
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901822"
---
# <span data-ttu-id="1119b-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="1119b-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="1119b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1119b-102">SYNOPSIS</span></span>
<span data-ttu-id="1119b-103">變更或修改連接至網路虛擬裝置資源的虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="1119b-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1119b-104">語法</span><span class="sxs-lookup"><span data-stu-id="1119b-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1119b-105">描述</span><span class="sxs-lookup"><span data-stu-id="1119b-105">DESCRIPTION</span></span>
<span data-ttu-id="1119b-106">命令Update-AzVirtualApplianceSite虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="1119b-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="1119b-107">例子</span><span class="sxs-lookup"><span data-stu-id="1119b-107">EXAMPLES</span></span>

### <span data-ttu-id="1119b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1119b-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="1119b-109">修改虛擬裝置網站資源的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="1119b-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="1119b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1119b-110">PARAMETERS</span></span>

### <span data-ttu-id="1119b-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="1119b-111">-AddresssPrefix</span></span>
<span data-ttu-id="1119b-112">網站的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="1119b-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="1119b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1119b-113">-AsJob</span></span>
<span data-ttu-id="1119b-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1119b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1119b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1119b-115">-DefaultProfile</span></span>
<span data-ttu-id="1119b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1119b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1119b-117">-強制</span><span class="sxs-lookup"><span data-stu-id="1119b-117">-Force</span></span>
<span data-ttu-id="1119b-118">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="1119b-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1119b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1119b-119">-Name</span></span>
<span data-ttu-id="1119b-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1119b-120">The resource name.</span></span>

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

### <span data-ttu-id="1119b-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="1119b-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="1119b-122">此網站所附加的網路虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="1119b-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="1119b-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="1119b-123">-O365Policy</span></span>
<span data-ttu-id="1119b-124">Office 365 分組討論策略。</span><span class="sxs-lookup"><span data-stu-id="1119b-124">Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="1119b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1119b-125">-ResourceGroupName</span></span>
<span data-ttu-id="1119b-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1119b-126">The resource group name.</span></span>

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

### <span data-ttu-id="1119b-127">-標記</span><span class="sxs-lookup"><span data-stu-id="1119b-127">-Tag</span></span>
<span data-ttu-id="1119b-128">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1119b-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1119b-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1119b-129">-Confirm</span></span>
<span data-ttu-id="1119b-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1119b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1119b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1119b-131">-WhatIf</span></span>
<span data-ttu-id="1119b-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1119b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1119b-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1119b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1119b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1119b-134">CommonParameters</span></span>
<span data-ttu-id="1119b-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1119b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1119b-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1119b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1119b-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1119b-137">INPUTS</span></span>

### <span data-ttu-id="1119b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1119b-138">System.String</span></span>

### <span data-ttu-id="1119b-139">Microsoft.Azure.Commands.Network.models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="1119b-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="1119b-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1119b-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1119b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1119b-141">OUTPUTS</span></span>

### <span data-ttu-id="1119b-142">Microsoft.Azure.Commands.Network.models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="1119b-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="1119b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1119b-143">NOTES</span></span>

## <span data-ttu-id="1119b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1119b-144">RELATED LINKS</span></span>
