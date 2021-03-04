---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7684072abbef4af8344cc07aa4bef6cab88ad3ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908793"
---
# <span data-ttu-id="e5789-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5789-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e5789-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5789-102">SYNOPSIS</span></span>
<span data-ttu-id="e5789-103">更新私人連結服務上的私人端點連接狀態。</span><span class="sxs-lookup"><span data-stu-id="e5789-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="e5789-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5789-104">SYNTAX</span></span>

### <span data-ttu-id="e5789-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="e5789-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5789-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="e5789-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5789-107">描述</span><span class="sxs-lookup"><span data-stu-id="e5789-107">DESCRIPTION</span></span>
<span data-ttu-id="e5789-108">**Set-AzPrivateEndpointConnection** Cmdlet 會更新私人連結服務上的私人端點連接狀態</span><span class="sxs-lookup"><span data-stu-id="e5789-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="e5789-109">例子</span><span class="sxs-lookup"><span data-stu-id="e5789-109">EXAMPLES</span></span>

### <span data-ttu-id="e5789-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e5789-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="e5789-111">此範例將私人端點連接狀態更新為已核准。</span><span class="sxs-lookup"><span data-stu-id="e5789-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="e5789-112">參數</span><span class="sxs-lookup"><span data-stu-id="e5789-112">PARAMETERS</span></span>

### <span data-ttu-id="e5789-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5789-113">-DefaultProfile</span></span>
<span data-ttu-id="e5789-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5789-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5789-115">-描述</span><span class="sxs-lookup"><span data-stu-id="e5789-115">-Description</span></span>
<span data-ttu-id="e5789-116">動作原因。</span><span class="sxs-lookup"><span data-stu-id="e5789-116">The reason of action.</span></span>

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

### <span data-ttu-id="e5789-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5789-117">-Name</span></span>
<span data-ttu-id="e5789-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e5789-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5789-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="e5789-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="e5789-120">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="e5789-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5789-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="e5789-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="e5789-122">已核准或拒絕資源。</span><span class="sxs-lookup"><span data-stu-id="e5789-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="e5789-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5789-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5789-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e5789-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5789-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5789-125">-ResourceId</span></span>
<span data-ttu-id="e5789-126">私人端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5789-126">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5789-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e5789-127">-ServiceName</span></span>
<span data-ttu-id="e5789-128">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e5789-128">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5789-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5789-129">CommonParameters</span></span>
<span data-ttu-id="e5789-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5789-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5789-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5789-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5789-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e5789-132">INPUTS</span></span>

### <span data-ttu-id="e5789-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e5789-133">System.String</span></span>

## <span data-ttu-id="e5789-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e5789-134">OUTPUTS</span></span>

### <span data-ttu-id="e5789-135">Microsoft.Azure.Commands.Network.models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e5789-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e5789-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e5789-136">NOTES</span></span>

## <span data-ttu-id="e5789-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5789-137">RELATED LINKS</span></span>

[<span data-ttu-id="e5789-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5789-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e5789-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5789-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e5789-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5789-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e5789-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5789-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)