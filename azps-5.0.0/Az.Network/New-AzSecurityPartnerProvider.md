---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286855"
---
# <span data-ttu-id="2dabd-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2dabd-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="2dabd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2dabd-102">SYNOPSIS</span></span>
<span data-ttu-id="2dabd-103">建立 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="2dabd-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="2dabd-104">句法</span><span class="sxs-lookup"><span data-stu-id="2dabd-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dabd-105">說明</span><span class="sxs-lookup"><span data-stu-id="2dabd-105">DESCRIPTION</span></span>
<span data-ttu-id="2dabd-106">**新的-AzSecurityPartnerProvider** Cmdlet 會建立 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2dabd-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="2dabd-107">示例</span><span class="sxs-lookup"><span data-stu-id="2dabd-107">EXAMPLES</span></span>

### <span data-ttu-id="2dabd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2dabd-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="2dabd-109">參數</span><span class="sxs-lookup"><span data-stu-id="2dabd-109">PARAMETERS</span></span>

### <span data-ttu-id="2dabd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dabd-110">-AsJob</span></span>
<span data-ttu-id="2dabd-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2dabd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dabd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dabd-112">-DefaultProfile</span></span>
<span data-ttu-id="2dabd-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2dabd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dabd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2dabd-114">-Force</span></span>
<span data-ttu-id="2dabd-115">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="2dabd-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2dabd-116">-位置</span><span class="sxs-lookup"><span data-stu-id="2dabd-116">-Location</span></span>
<span data-ttu-id="2dabd-117">位於.</span><span class="sxs-lookup"><span data-stu-id="2dabd-117">location.</span></span>

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

### <span data-ttu-id="2dabd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2dabd-118">-Name</span></span>
<span data-ttu-id="2dabd-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2dabd-119">The resource name.</span></span>

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

### <span data-ttu-id="2dabd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dabd-120">-ResourceGroupName</span></span>
<span data-ttu-id="2dabd-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dabd-121">The resource group name.</span></span>

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

### <span data-ttu-id="2dabd-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="2dabd-122">-SecurityProviderName</span></span>
<span data-ttu-id="2dabd-123">安全性提供者名稱</span><span class="sxs-lookup"><span data-stu-id="2dabd-123">The Security Provider name</span></span>

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

### <span data-ttu-id="2dabd-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="2dabd-124">-Tag</span></span>
<span data-ttu-id="2dabd-125">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="2dabd-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2dabd-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2dabd-126">-VirtualHub</span></span>
<span data-ttu-id="2dabd-127">安全夥伴提供者所附加的虛擬中心 Id</span><span class="sxs-lookup"><span data-stu-id="2dabd-127">The virtual hub Id that the security partner provider is attached to</span></span>

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

### <span data-ttu-id="2dabd-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="2dabd-128">-VirtualHubId</span></span>
<span data-ttu-id="2dabd-129">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2dabd-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="2dabd-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="2dabd-130">-VirtualHubName</span></span>
<span data-ttu-id="2dabd-131">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2dabd-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="2dabd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="2dabd-132">-Confirm</span></span>
<span data-ttu-id="2dabd-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2dabd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dabd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dabd-134">-WhatIf</span></span>
<span data-ttu-id="2dabd-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2dabd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dabd-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2dabd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dabd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dabd-137">CommonParameters</span></span>
<span data-ttu-id="2dabd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2dabd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dabd-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2dabd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dabd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="2dabd-140">INPUTS</span></span>

### <span data-ttu-id="2dabd-141">System.object</span><span class="sxs-lookup"><span data-stu-id="2dabd-141">System.String</span></span>

### <span data-ttu-id="2dabd-142">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2dabd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="2dabd-143">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2dabd-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2dabd-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2dabd-144">OUTPUTS</span></span>

### <span data-ttu-id="2dabd-145">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2dabd-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2dabd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2dabd-146">NOTES</span></span>

## <span data-ttu-id="2dabd-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dabd-147">RELATED LINKS</span></span>
