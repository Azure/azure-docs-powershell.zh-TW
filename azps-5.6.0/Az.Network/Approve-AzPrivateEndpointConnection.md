---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 3768bc8769d81056dc8f2de4f42f9f1783f89728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908833"
---
# <span data-ttu-id="49523-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49523-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="49523-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49523-102">SYNOPSIS</span></span>
<span data-ttu-id="49523-103">核准私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="49523-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="49523-104">語法</span><span class="sxs-lookup"><span data-stu-id="49523-104">SYNTAX</span></span>

### <span data-ttu-id="49523-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="49523-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49523-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="49523-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49523-107">描述</span><span class="sxs-lookup"><span data-stu-id="49523-107">DESCRIPTION</span></span>
<span data-ttu-id="49523-108">**Approve-AzPrivateEndpointConnection** Cmdlet 會核准私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="49523-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="49523-109">例子</span><span class="sxs-lookup"><span data-stu-id="49523-109">EXAMPLES</span></span>

### <span data-ttu-id="49523-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="49523-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="49523-111">此範例核准私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="49523-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="49523-112">參數</span><span class="sxs-lookup"><span data-stu-id="49523-112">PARAMETERS</span></span>

### <span data-ttu-id="49523-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49523-113">-DefaultProfile</span></span>
<span data-ttu-id="49523-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49523-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49523-115">-描述</span><span class="sxs-lookup"><span data-stu-id="49523-115">-Description</span></span>
<span data-ttu-id="49523-116">動作原因。</span><span class="sxs-lookup"><span data-stu-id="49523-116">The reason of action.</span></span>

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

### <span data-ttu-id="49523-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="49523-117">-Name</span></span>
<span data-ttu-id="49523-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="49523-118">The resource name.</span></span>

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

### <span data-ttu-id="49523-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="49523-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="49523-120">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="49523-120">The private link resource type.</span></span>

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

### <span data-ttu-id="49523-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49523-121">-ResourceGroupName</span></span>
<span data-ttu-id="49523-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="49523-122">The resource group name.</span></span>

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

### <span data-ttu-id="49523-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49523-123">-ResourceId</span></span>
<span data-ttu-id="49523-124">私人端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="49523-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="49523-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49523-125">-ServiceName</span></span>
<span data-ttu-id="49523-126">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="49523-126">The private link service name.</span></span>

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


### <span data-ttu-id="49523-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49523-127">CommonParameters</span></span>
<span data-ttu-id="49523-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49523-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49523-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49523-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49523-130">輸入</span><span class="sxs-lookup"><span data-stu-id="49523-130">INPUTS</span></span>

### <span data-ttu-id="49523-131">System.String</span><span class="sxs-lookup"><span data-stu-id="49523-131">System.String</span></span>

## <span data-ttu-id="49523-132">輸出</span><span class="sxs-lookup"><span data-stu-id="49523-132">OUTPUTS</span></span>

### <span data-ttu-id="49523-133">Microsoft.Azure.Commands.Network.models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="49523-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="49523-134">筆記</span><span class="sxs-lookup"><span data-stu-id="49523-134">NOTES</span></span>

## <span data-ttu-id="49523-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="49523-135">RELATED LINKS</span></span>

[<span data-ttu-id="49523-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49523-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="49523-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49523-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="49523-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49523-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="49523-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49523-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)