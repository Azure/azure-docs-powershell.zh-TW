---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126994"
---
# <span data-ttu-id="70ded-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70ded-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="70ded-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70ded-102">SYNOPSIS</span></span>
<span data-ttu-id="70ded-103">取得私用端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="70ded-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="70ded-104">句法</span><span class="sxs-lookup"><span data-stu-id="70ded-104">SYNTAX</span></span>

### <span data-ttu-id="70ded-105">ByPrivateLinkResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="70ded-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ded-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="70ded-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ded-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="70ded-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70ded-108">說明</span><span class="sxs-lookup"><span data-stu-id="70ded-108">DESCRIPTION</span></span>
<span data-ttu-id="70ded-109">**AzPrivateEndpointConnection** Cmdlet 會檢索私人端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="70ded-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="70ded-110">示例</span><span class="sxs-lookup"><span data-stu-id="70ded-110">EXAMPLES</span></span>

### <span data-ttu-id="70ded-111">範例1</span><span class="sxs-lookup"><span data-stu-id="70ded-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="70ded-112">這個範例會傳回屬於「Mysql」的 sql server 所有私人端點連線的清單。</span><span class="sxs-lookup"><span data-stu-id="70ded-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="70ded-113">範例2</span><span class="sxs-lookup"><span data-stu-id="70ded-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="70ded-114">這個範例會取得名為 MyPrivateEndpointConnection1 的私人端點連線屬於名為 MyPrivateLinkService 的私人連結服務</span><span class="sxs-lookup"><span data-stu-id="70ded-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="70ded-115">參數</span><span class="sxs-lookup"><span data-stu-id="70ded-115">PARAMETERS</span></span>

### <span data-ttu-id="70ded-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ded-116">-DefaultProfile</span></span>
<span data-ttu-id="70ded-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70ded-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70ded-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="70ded-118">-Name</span></span>
<span data-ttu-id="70ded-119">私人端點連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="70ded-119">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ded-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="70ded-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="70ded-121">私人端點連線所屬之私人連結資源的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="70ded-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ded-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="70ded-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="70ded-123">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="70ded-123">The private link resource type.</span></span>

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

### <span data-ttu-id="70ded-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ded-124">-ResourceGroupName</span></span>
<span data-ttu-id="70ded-125">私人端點連線的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="70ded-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="70ded-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70ded-126">-ResourceId</span></span>
<span data-ttu-id="70ded-127">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="70ded-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="70ded-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="70ded-128">-ServiceName</span></span>
<span data-ttu-id="70ded-129">私人端點連線所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="70ded-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="70ded-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ded-130">CommonParameters</span></span>
<span data-ttu-id="70ded-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70ded-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ded-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70ded-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ded-133">輸入</span><span class="sxs-lookup"><span data-stu-id="70ded-133">INPUTS</span></span>

### <span data-ttu-id="70ded-134">System.object</span><span class="sxs-lookup"><span data-stu-id="70ded-134">System.String</span></span>

## <span data-ttu-id="70ded-135">輸出</span><span class="sxs-lookup"><span data-stu-id="70ded-135">OUTPUTS</span></span>

### <span data-ttu-id="70ded-136">System.object</span><span class="sxs-lookup"><span data-stu-id="70ded-136">System.Boolean</span></span>

## <span data-ttu-id="70ded-137">筆記</span><span class="sxs-lookup"><span data-stu-id="70ded-137">NOTES</span></span>

## <span data-ttu-id="70ded-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="70ded-138">RELATED LINKS</span></span>

[<span data-ttu-id="70ded-139">核准-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70ded-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="70ded-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70ded-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="70ded-141">移除-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70ded-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="70ded-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70ded-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
