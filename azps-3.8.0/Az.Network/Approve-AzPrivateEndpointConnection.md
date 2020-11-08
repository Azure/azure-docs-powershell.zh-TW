---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958461"
---
# <span data-ttu-id="1acb9-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1acb9-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="1acb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1acb9-102">SYNOPSIS</span></span>
<span data-ttu-id="1acb9-103">核准私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="1acb9-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="1acb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="1acb9-104">SYNTAX</span></span>

### <span data-ttu-id="1acb9-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="1acb9-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1acb9-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="1acb9-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1acb9-107">說明</span><span class="sxs-lookup"><span data-stu-id="1acb9-107">DESCRIPTION</span></span>
<span data-ttu-id="1acb9-108">**核准-AzPrivateEndpointConnection** Cmdlet 會核准私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="1acb9-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="1acb9-109">示例</span><span class="sxs-lookup"><span data-stu-id="1acb9-109">EXAMPLES</span></span>

### <span data-ttu-id="1acb9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1acb9-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="1acb9-111">這個範例會核准私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="1acb9-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="1acb9-112">參數</span><span class="sxs-lookup"><span data-stu-id="1acb9-112">PARAMETERS</span></span>

### <span data-ttu-id="1acb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1acb9-113">-DefaultProfile</span></span>
<span data-ttu-id="1acb9-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1acb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1acb9-115">-描述</span><span class="sxs-lookup"><span data-stu-id="1acb9-115">-Description</span></span>
<span data-ttu-id="1acb9-116">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="1acb9-116">The reason of action.</span></span>

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

### <span data-ttu-id="1acb9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1acb9-117">-Name</span></span>
<span data-ttu-id="1acb9-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1acb9-118">The resource name.</span></span>

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

### <span data-ttu-id="1acb9-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="1acb9-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="1acb9-120">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="1acb9-120">The private link resource type.</span></span>

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

### <span data-ttu-id="1acb9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1acb9-121">-ResourceGroupName</span></span>
<span data-ttu-id="1acb9-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1acb9-122">The resource group name.</span></span>

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

### <span data-ttu-id="1acb9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1acb9-123">-ResourceId</span></span>
<span data-ttu-id="1acb9-124">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="1acb9-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="1acb9-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1acb9-125">-ServiceName</span></span>
<span data-ttu-id="1acb9-126">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="1acb9-126">The private link service name.</span></span>

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


### <span data-ttu-id="1acb9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1acb9-127">CommonParameters</span></span>
<span data-ttu-id="1acb9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1acb9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1acb9-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1acb9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1acb9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1acb9-130">INPUTS</span></span>

### <span data-ttu-id="1acb9-131">System.object</span><span class="sxs-lookup"><span data-stu-id="1acb9-131">System.String</span></span>

## <span data-ttu-id="1acb9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1acb9-132">OUTPUTS</span></span>

### <span data-ttu-id="1acb9-133">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1acb9-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="1acb9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1acb9-134">NOTES</span></span>

## <span data-ttu-id="1acb9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1acb9-135">RELATED LINKS</span></span>

[<span data-ttu-id="1acb9-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1acb9-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="1acb9-137">AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1acb9-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="1acb9-138">移除-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1acb9-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="1acb9-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1acb9-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)