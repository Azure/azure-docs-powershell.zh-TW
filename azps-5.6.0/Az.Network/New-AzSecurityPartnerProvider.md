---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 4cb66f01b8ce61edf9a5399119aa5e6318617db7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902382"
---
# <span data-ttu-id="e3148-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3148-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="e3148-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3148-102">SYNOPSIS</span></span>
<span data-ttu-id="e3148-103">建立 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="e3148-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="e3148-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3148-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3148-105">描述</span><span class="sxs-lookup"><span data-stu-id="e3148-105">DESCRIPTION</span></span>
<span data-ttu-id="e3148-106">**New-AzSecurityPartnerProvider Cmdlet** 會建立 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3148-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="e3148-107">例子</span><span class="sxs-lookup"><span data-stu-id="e3148-107">EXAMPLES</span></span>

### <span data-ttu-id="e3148-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e3148-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="e3148-109">參數</span><span class="sxs-lookup"><span data-stu-id="e3148-109">PARAMETERS</span></span>

### <span data-ttu-id="e3148-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3148-110">-AsJob</span></span>
<span data-ttu-id="e3148-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e3148-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3148-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3148-112">-DefaultProfile</span></span>
<span data-ttu-id="e3148-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3148-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3148-114">-強制</span><span class="sxs-lookup"><span data-stu-id="e3148-114">-Force</span></span>
<span data-ttu-id="e3148-115">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="e3148-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3148-116">-位置</span><span class="sxs-lookup"><span data-stu-id="e3148-116">-Location</span></span>
<span data-ttu-id="e3148-117">位置。</span><span class="sxs-lookup"><span data-stu-id="e3148-117">location.</span></span>

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

### <span data-ttu-id="e3148-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3148-118">-Name</span></span>
<span data-ttu-id="e3148-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e3148-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3148-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3148-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3148-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e3148-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3148-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="e3148-122">-SecurityProviderName</span></span>
<span data-ttu-id="e3148-123">安全性提供者名稱</span><span class="sxs-lookup"><span data-stu-id="e3148-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3148-124">-標記</span><span class="sxs-lookup"><span data-stu-id="e3148-124">-Tag</span></span>
<span data-ttu-id="e3148-125">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e3148-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3148-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3148-126">-VirtualHub</span></span>
<span data-ttu-id="e3148-127">安全性合作夥伴提供者所附加的虛擬中樞識別碼</span><span class="sxs-lookup"><span data-stu-id="e3148-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3148-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="e3148-128">-VirtualHubId</span></span>
<span data-ttu-id="e3148-129">這個 VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="e3148-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="e3148-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="e3148-130">-VirtualHubName</span></span>
<span data-ttu-id="e3148-131">這個 VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="e3148-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3148-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e3148-132">-Confirm</span></span>
<span data-ttu-id="e3148-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e3148-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3148-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3148-134">-WhatIf</span></span>
<span data-ttu-id="e3148-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3148-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3148-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3148-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3148-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3148-137">CommonParameters</span></span>
<span data-ttu-id="e3148-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3148-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3148-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3148-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3148-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e3148-140">INPUTS</span></span>

### <span data-ttu-id="e3148-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e3148-141">System.String</span></span>

### <span data-ttu-id="e3148-142">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3148-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e3148-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3148-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3148-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e3148-144">OUTPUTS</span></span>

### <span data-ttu-id="e3148-145">Microsoft.Azure.Commands.Network.models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3148-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="e3148-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e3148-146">NOTES</span></span>

## <span data-ttu-id="e3148-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3148-147">RELATED LINKS</span></span>
