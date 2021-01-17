---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448976"
---
# <span data-ttu-id="64ebd-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="64ebd-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="64ebd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="64ebd-103">建立 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="64ebd-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="64ebd-104">句法</span><span class="sxs-lookup"><span data-stu-id="64ebd-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64ebd-105">說明</span><span class="sxs-lookup"><span data-stu-id="64ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="64ebd-106">**新的-AzSecurityPartnerProvider** Cmdlet 會建立 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="64ebd-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="64ebd-107">示例</span><span class="sxs-lookup"><span data-stu-id="64ebd-107">EXAMPLES</span></span>

### <span data-ttu-id="64ebd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="64ebd-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="64ebd-109">參數</span><span class="sxs-lookup"><span data-stu-id="64ebd-109">PARAMETERS</span></span>

### <span data-ttu-id="64ebd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64ebd-110">-AsJob</span></span>
<span data-ttu-id="64ebd-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="64ebd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64ebd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ebd-112">-DefaultProfile</span></span>
<span data-ttu-id="64ebd-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64ebd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ebd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="64ebd-114">-Force</span></span>
<span data-ttu-id="64ebd-115">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="64ebd-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="64ebd-116">-位置</span><span class="sxs-lookup"><span data-stu-id="64ebd-116">-Location</span></span>
<span data-ttu-id="64ebd-117">位於.</span><span class="sxs-lookup"><span data-stu-id="64ebd-117">location.</span></span>

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

### <span data-ttu-id="64ebd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="64ebd-118">-Name</span></span>
<span data-ttu-id="64ebd-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="64ebd-119">The resource name.</span></span>

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

### <span data-ttu-id="64ebd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ebd-120">-ResourceGroupName</span></span>
<span data-ttu-id="64ebd-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ebd-121">The resource group name.</span></span>

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

### <span data-ttu-id="64ebd-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="64ebd-122">-SecurityProviderName</span></span>
<span data-ttu-id="64ebd-123">安全性提供者名稱</span><span class="sxs-lookup"><span data-stu-id="64ebd-123">The Security Provider name</span></span>

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

### <span data-ttu-id="64ebd-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="64ebd-124">-Tag</span></span>
<span data-ttu-id="64ebd-125">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="64ebd-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="64ebd-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="64ebd-126">-VirtualHub</span></span>
<span data-ttu-id="64ebd-127">安全夥伴提供者所附加的虛擬中心 Id</span><span class="sxs-lookup"><span data-stu-id="64ebd-127">The virtual hub Id that the security partner provider is attached to</span></span>

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

### <span data-ttu-id="64ebd-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="64ebd-128">-VirtualHubId</span></span>
<span data-ttu-id="64ebd-129">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="64ebd-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="64ebd-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="64ebd-130">-VirtualHubName</span></span>
<span data-ttu-id="64ebd-131">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="64ebd-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="64ebd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="64ebd-132">-Confirm</span></span>
<span data-ttu-id="64ebd-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64ebd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64ebd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64ebd-134">-WhatIf</span></span>
<span data-ttu-id="64ebd-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64ebd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64ebd-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64ebd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64ebd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ebd-137">CommonParameters</span></span>
<span data-ttu-id="64ebd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64ebd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ebd-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64ebd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ebd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="64ebd-140">INPUTS</span></span>

### <span data-ttu-id="64ebd-141">System.object</span><span class="sxs-lookup"><span data-stu-id="64ebd-141">System.String</span></span>

### <span data-ttu-id="64ebd-142">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64ebd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="64ebd-143">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64ebd-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64ebd-144">輸出</span><span class="sxs-lookup"><span data-stu-id="64ebd-144">OUTPUTS</span></span>

### <span data-ttu-id="64ebd-145">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64ebd-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="64ebd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="64ebd-146">NOTES</span></span>

## <span data-ttu-id="64ebd-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="64ebd-147">RELATED LINKS</span></span>
