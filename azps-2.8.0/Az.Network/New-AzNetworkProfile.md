---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: 87d753ebaf2d8d4891fc96dbc25f7ad0fa1095af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789314"
---
# <span data-ttu-id="5ff34-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5ff34-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="5ff34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ff34-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff34-103">建立新的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="5ff34-103">Creates a new network profile.</span></span>

## <span data-ttu-id="5ff34-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ff34-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff34-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ff34-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff34-106">**新的-AzNetworkProfile** Cmdlet 會建立新的網路設定檔頂層資源。</span><span class="sxs-lookup"><span data-stu-id="5ff34-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="5ff34-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ff34-107">EXAMPLES</span></span>

### <span data-ttu-id="5ff34-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5ff34-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="5ff34-109">這會建立新的網路設定檔頂層資源</span><span class="sxs-lookup"><span data-stu-id="5ff34-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="5ff34-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ff34-110">PARAMETERS</span></span>

### <span data-ttu-id="5ff34-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ff34-111">-AsJob</span></span>
<span data-ttu-id="5ff34-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ff34-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ff34-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5ff34-113">-ContainerNicConfig</span></span>
<span data-ttu-id="5ff34-114">要新增至此網路設定檔的容器網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="5ff34-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff34-115">-DefaultProfile</span></span>
<span data-ttu-id="5ff34-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ff34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff34-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ff34-117">-Force</span></span>
<span data-ttu-id="5ff34-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="5ff34-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5ff34-119">-位置</span><span class="sxs-lookup"><span data-stu-id="5ff34-119">-Location</span></span>
<span data-ttu-id="5ff34-120">位置。</span><span class="sxs-lookup"><span data-stu-id="5ff34-120">The location.</span></span>

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

### <span data-ttu-id="5ff34-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ff34-121">-Name</span></span>
<span data-ttu-id="5ff34-122">網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ff34-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="5ff34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff34-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ff34-124">網路設定檔的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5ff34-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="5ff34-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ff34-125">-Tag</span></span>
<span data-ttu-id="5ff34-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="5ff34-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5ff34-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5ff34-127">-Confirm</span></span>
<span data-ttu-id="5ff34-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ff34-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff34-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff34-129">-WhatIf</span></span>
<span data-ttu-id="5ff34-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ff34-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff34-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ff34-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff34-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff34-132">CommonParameters</span></span>
<span data-ttu-id="5ff34-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ff34-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff34-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ff34-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff34-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5ff34-135">INPUTS</span></span>

### <span data-ttu-id="5ff34-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5ff34-136">System.String</span></span>

### <span data-ttu-id="5ff34-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ff34-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ff34-138">PSContainerNetworkInterfaceConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="5ff34-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="5ff34-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5ff34-139">OUTPUTS</span></span>

### <span data-ttu-id="5ff34-140">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ff34-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="5ff34-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5ff34-141">NOTES</span></span>

## <span data-ttu-id="5ff34-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ff34-142">RELATED LINKS</span></span>

[<span data-ttu-id="5ff34-143">AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5ff34-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="5ff34-144">移除-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5ff34-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="5ff34-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5ff34-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
