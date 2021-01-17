---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448891"
---
# <span data-ttu-id="672e2-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="672e2-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="672e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="672e2-102">SYNOPSIS</span></span>
<span data-ttu-id="672e2-103">更新私人連結服務上的私人端點線上狀態。</span><span class="sxs-lookup"><span data-stu-id="672e2-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="672e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="672e2-104">SYNTAX</span></span>

### <span data-ttu-id="672e2-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="672e2-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="672e2-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="672e2-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="672e2-107">說明</span><span class="sxs-lookup"><span data-stu-id="672e2-107">DESCRIPTION</span></span>
<span data-ttu-id="672e2-108">**AzPrivateEndpointConnection** Cmdlet 會更新私人連結服務上的私人端點線上狀態</span><span class="sxs-lookup"><span data-stu-id="672e2-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="672e2-109">示例</span><span class="sxs-lookup"><span data-stu-id="672e2-109">EXAMPLES</span></span>

### <span data-ttu-id="672e2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="672e2-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="672e2-111">這個範例會將私人端點線上狀態更新為 [已核准]。</span><span class="sxs-lookup"><span data-stu-id="672e2-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="672e2-112">參數</span><span class="sxs-lookup"><span data-stu-id="672e2-112">PARAMETERS</span></span>

### <span data-ttu-id="672e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672e2-113">-DefaultProfile</span></span>
<span data-ttu-id="672e2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="672e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="672e2-115">-描述</span><span class="sxs-lookup"><span data-stu-id="672e2-115">-Description</span></span>
<span data-ttu-id="672e2-116">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="672e2-116">The reason of action.</span></span>

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

### <span data-ttu-id="672e2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="672e2-117">-Name</span></span>
<span data-ttu-id="672e2-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="672e2-118">The resource name.</span></span>

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

### <span data-ttu-id="672e2-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="672e2-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="672e2-120">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="672e2-120">The private link resource type.</span></span>

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

### <span data-ttu-id="672e2-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="672e2-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="672e2-122">已核准或拒絕資源。</span><span class="sxs-lookup"><span data-stu-id="672e2-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="672e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="672e2-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="672e2-124">The resource group name.</span></span>

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

### <span data-ttu-id="672e2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="672e2-125">-ResourceId</span></span>
<span data-ttu-id="672e2-126">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="672e2-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="672e2-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="672e2-127">-ServiceName</span></span>
<span data-ttu-id="672e2-128">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="672e2-128">The private link service name.</span></span>

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

### <span data-ttu-id="672e2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672e2-129">CommonParameters</span></span>
<span data-ttu-id="672e2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="672e2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672e2-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="672e2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672e2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="672e2-132">INPUTS</span></span>

### <span data-ttu-id="672e2-133">System.object</span><span class="sxs-lookup"><span data-stu-id="672e2-133">System.String</span></span>

## <span data-ttu-id="672e2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="672e2-134">OUTPUTS</span></span>

### <span data-ttu-id="672e2-135">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="672e2-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="672e2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="672e2-136">NOTES</span></span>

## <span data-ttu-id="672e2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="672e2-137">RELATED LINKS</span></span>

[<span data-ttu-id="672e2-138">核准-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="672e2-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="672e2-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="672e2-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="672e2-140">AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="672e2-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="672e2-141">移除-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="672e2-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)