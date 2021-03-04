---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: d2df4f7f5ed073d357daa1113a8e0c7477a05cce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902477"
---
# <span data-ttu-id="0c779-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c779-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="0c779-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c779-102">SYNOPSIS</span></span>
<span data-ttu-id="0c779-103">獲得私人端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="0c779-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="0c779-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c779-104">SYNTAX</span></span>

### <span data-ttu-id="0c779-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="0c779-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c779-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0c779-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c779-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="0c779-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c779-108">描述</span><span class="sxs-lookup"><span data-stu-id="0c779-108">DESCRIPTION</span></span>
<span data-ttu-id="0c779-109">**Get-AzPrivateEndpointConnection** Cmdlet 會取回私人端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="0c779-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="0c779-110">例子</span><span class="sxs-lookup"><span data-stu-id="0c779-110">EXAMPLES</span></span>

### <span data-ttu-id="0c779-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0c779-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="0c779-112">此範例會返回所有私人端點連結的清單屬於名為 Mysql 的 sql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="0c779-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="0c779-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="0c779-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="0c779-114">此範例取得名為 MyPrivateEndpointConnection1 的私人端點連接屬於名為 MyPrivateLinkService 的私人連結服務</span><span class="sxs-lookup"><span data-stu-id="0c779-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="0c779-115">參數</span><span class="sxs-lookup"><span data-stu-id="0c779-115">PARAMETERS</span></span>

### <span data-ttu-id="0c779-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c779-116">-DefaultProfile</span></span>
<span data-ttu-id="0c779-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c779-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c779-118">-描述</span><span class="sxs-lookup"><span data-stu-id="0c779-118">-Description</span></span>
<span data-ttu-id="0c779-119">動作原因。</span><span class="sxs-lookup"><span data-stu-id="0c779-119">The reason of action.</span></span>

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

### <span data-ttu-id="0c779-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c779-120">-Name</span></span>
<span data-ttu-id="0c779-121">私人端點連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c779-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c779-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0c779-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="0c779-123">私人端點連接所屬的私人連結資源的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c779-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="0c779-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="0c779-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="0c779-125">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="0c779-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c779-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c779-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c779-127">私人端點連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0c779-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c779-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c779-128">-ResourceId</span></span>
<span data-ttu-id="0c779-129">私人端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c779-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c779-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c779-130">-ServiceName</span></span>
<span data-ttu-id="0c779-131">私人端點連接所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0c779-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="0c779-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c779-132">CommonParameters</span></span>
<span data-ttu-id="0c779-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c779-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c779-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c779-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c779-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0c779-135">INPUTS</span></span>

### <span data-ttu-id="0c779-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0c779-136">System.String</span></span>

## <span data-ttu-id="0c779-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0c779-137">OUTPUTS</span></span>

### <span data-ttu-id="0c779-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c779-138">System.Boolean</span></span>

## <span data-ttu-id="0c779-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0c779-139">NOTES</span></span>

## <span data-ttu-id="0c779-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c779-140">RELATED LINKS</span></span>

[<span data-ttu-id="0c779-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c779-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c779-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c779-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c779-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c779-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c779-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c779-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
