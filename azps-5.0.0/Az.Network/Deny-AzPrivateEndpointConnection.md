---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139824"
---
# <span data-ttu-id="f108f-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f108f-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="f108f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f108f-102">SYNOPSIS</span></span>
<span data-ttu-id="f108f-103">拒絕私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="f108f-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="f108f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f108f-104">SYNTAX</span></span>

### <span data-ttu-id="f108f-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="f108f-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f108f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="f108f-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f108f-107">說明</span><span class="sxs-lookup"><span data-stu-id="f108f-107">DESCRIPTION</span></span>
<span data-ttu-id="f108f-108">**Deny-AzPrivateEndpointConnection** Cmdlet 會拒絕私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="f108f-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="f108f-109">示例</span><span class="sxs-lookup"><span data-stu-id="f108f-109">EXAMPLES</span></span>

### <span data-ttu-id="f108f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f108f-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="f108f-111">這個範例會拒絕私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="f108f-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="f108f-112">參數</span><span class="sxs-lookup"><span data-stu-id="f108f-112">PARAMETERS</span></span>

### <span data-ttu-id="f108f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f108f-113">-DefaultProfile</span></span>
<span data-ttu-id="f108f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f108f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f108f-115">-描述</span><span class="sxs-lookup"><span data-stu-id="f108f-115">-Description</span></span>
<span data-ttu-id="f108f-116">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="f108f-116">The reason of action.</span></span>

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

### <span data-ttu-id="f108f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f108f-117">-Name</span></span>
<span data-ttu-id="f108f-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f108f-118">The resource name.</span></span>

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

### <span data-ttu-id="f108f-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f108f-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f108f-120">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="f108f-120">The private link resource type.</span></span>

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

### <span data-ttu-id="f108f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f108f-121">-ResourceGroupName</span></span>
<span data-ttu-id="f108f-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f108f-122">The resource group name.</span></span>

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

### <span data-ttu-id="f108f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f108f-123">-ResourceId</span></span>
<span data-ttu-id="f108f-124">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="f108f-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f108f-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f108f-125">-ServiceName</span></span>
<span data-ttu-id="f108f-126">私人端點連線所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f108f-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="f108f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f108f-127">CommonParameters</span></span>
<span data-ttu-id="f108f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f108f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f108f-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f108f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f108f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f108f-130">INPUTS</span></span>

### <span data-ttu-id="f108f-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f108f-131">System.String</span></span>

## <span data-ttu-id="f108f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f108f-132">OUTPUTS</span></span>

### <span data-ttu-id="f108f-133">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f108f-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="f108f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f108f-134">NOTES</span></span>

## <span data-ttu-id="f108f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f108f-135">RELATED LINKS</span></span>

[<span data-ttu-id="f108f-136">核准-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f108f-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f108f-137">AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f108f-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f108f-138">移除-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f108f-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f108f-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f108f-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)