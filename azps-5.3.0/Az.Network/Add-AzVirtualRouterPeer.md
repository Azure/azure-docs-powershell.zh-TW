---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436361"
---
# <span data-ttu-id="edc6a-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="edc6a-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="edc6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="edc6a-103">將對等新增至 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="edc6a-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="edc6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="edc6a-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edc6a-105">說明</span><span class="sxs-lookup"><span data-stu-id="edc6a-105">DESCRIPTION</span></span>
<span data-ttu-id="edc6a-106">**AzVirtualRouterPeer** Cmdlet 會將 VirtualRouter 對等新增至 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="edc6a-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="edc6a-107">示例</span><span class="sxs-lookup"><span data-stu-id="edc6a-107">EXAMPLES</span></span>

### <span data-ttu-id="edc6a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="edc6a-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="edc6a-109">參數</span><span class="sxs-lookup"><span data-stu-id="edc6a-109">PARAMETERS</span></span>

### <span data-ttu-id="edc6a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edc6a-110">-AsJob</span></span>
<span data-ttu-id="edc6a-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="edc6a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edc6a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc6a-112">-DefaultProfile</span></span>
<span data-ttu-id="edc6a-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edc6a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc6a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="edc6a-114">-Force</span></span>
<span data-ttu-id="edc6a-115">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="edc6a-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="edc6a-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="edc6a-116">-PeerAsn</span></span>
<span data-ttu-id="edc6a-117">對等 ASN。</span><span class="sxs-lookup"><span data-stu-id="edc6a-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc6a-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="edc6a-118">-PeerIp</span></span>
<span data-ttu-id="edc6a-119">對等 Ip。</span><span class="sxs-lookup"><span data-stu-id="edc6a-119">Peer Ip.</span></span>

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

### <span data-ttu-id="edc6a-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="edc6a-120">-PeerName</span></span>
<span data-ttu-id="edc6a-121">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="edc6a-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="edc6a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc6a-122">-ResourceGroupName</span></span>
<span data-ttu-id="edc6a-123">虛擬路由器/對等的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="edc6a-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="edc6a-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="edc6a-124">-VirtualRouterName</span></span>
<span data-ttu-id="edc6a-125">對等所在的虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="edc6a-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="edc6a-126">-確認</span><span class="sxs-lookup"><span data-stu-id="edc6a-126">-Confirm</span></span>
<span data-ttu-id="edc6a-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="edc6a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edc6a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc6a-128">-WhatIf</span></span>
<span data-ttu-id="edc6a-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edc6a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edc6a-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edc6a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edc6a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc6a-131">CommonParameters</span></span>
<span data-ttu-id="edc6a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edc6a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc6a-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="edc6a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc6a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="edc6a-134">INPUTS</span></span>

### <span data-ttu-id="edc6a-135">System.object</span><span class="sxs-lookup"><span data-stu-id="edc6a-135">System.String</span></span>

### <span data-ttu-id="edc6a-136">UInt32</span><span class="sxs-lookup"><span data-stu-id="edc6a-136">System.UInt32</span></span>

## <span data-ttu-id="edc6a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="edc6a-137">OUTPUTS</span></span>

### <span data-ttu-id="edc6a-138">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="edc6a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="edc6a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="edc6a-139">NOTES</span></span>

## <span data-ttu-id="edc6a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="edc6a-140">RELATED LINKS</span></span>
