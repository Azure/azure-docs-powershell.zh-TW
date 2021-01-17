---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436775"
---
# <span data-ttu-id="1d365-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d365-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="1d365-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d365-102">SYNOPSIS</span></span>
<span data-ttu-id="1d365-103">取得私用端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="1d365-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="1d365-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d365-104">SYNTAX</span></span>

### <span data-ttu-id="1d365-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="1d365-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d365-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="1d365-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d365-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="1d365-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d365-108">說明</span><span class="sxs-lookup"><span data-stu-id="1d365-108">DESCRIPTION</span></span>
<span data-ttu-id="1d365-109">**AzPrivateEndpointConnection** Cmdlet 會檢索私人端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="1d365-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="1d365-110">示例</span><span class="sxs-lookup"><span data-stu-id="1d365-110">EXAMPLES</span></span>

### <span data-ttu-id="1d365-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1d365-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="1d365-112">這個範例會傳回屬於「Mysql」的 sql server 所有私人端點連線的清單。</span><span class="sxs-lookup"><span data-stu-id="1d365-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="1d365-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1d365-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="1d365-114">這個範例會取得名為 MyPrivateEndpointConnection1 的私人端點連線屬於名為 MyPrivateLinkService 的私人連結服務</span><span class="sxs-lookup"><span data-stu-id="1d365-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="1d365-115">參數</span><span class="sxs-lookup"><span data-stu-id="1d365-115">PARAMETERS</span></span>

### <span data-ttu-id="1d365-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d365-116">-DefaultProfile</span></span>
<span data-ttu-id="1d365-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d365-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d365-118">-描述</span><span class="sxs-lookup"><span data-stu-id="1d365-118">-Description</span></span>
<span data-ttu-id="1d365-119">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="1d365-119">The reason of action.</span></span>

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

### <span data-ttu-id="1d365-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d365-120">-Name</span></span>
<span data-ttu-id="1d365-121">私人端點連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d365-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="1d365-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="1d365-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="1d365-123">私人端點連線所屬之私人連結資源的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d365-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="1d365-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="1d365-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="1d365-125">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="1d365-125">The private link resource type.</span></span>

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

### <span data-ttu-id="1d365-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d365-126">-ResourceGroupName</span></span>
<span data-ttu-id="1d365-127">私人端點連線的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1d365-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="1d365-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d365-128">-ResourceId</span></span>
<span data-ttu-id="1d365-129">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d365-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="1d365-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1d365-130">-ServiceName</span></span>
<span data-ttu-id="1d365-131">私人端點連線所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="1d365-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="1d365-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d365-132">CommonParameters</span></span>
<span data-ttu-id="1d365-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d365-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d365-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1d365-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d365-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1d365-135">INPUTS</span></span>

### <span data-ttu-id="1d365-136">System.object</span><span class="sxs-lookup"><span data-stu-id="1d365-136">System.String</span></span>

## <span data-ttu-id="1d365-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1d365-137">OUTPUTS</span></span>

### <span data-ttu-id="1d365-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1d365-138">System.Boolean</span></span>

## <span data-ttu-id="1d365-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1d365-139">NOTES</span></span>

## <span data-ttu-id="1d365-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d365-140">RELATED LINKS</span></span>

[<span data-ttu-id="1d365-141">核准-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d365-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="1d365-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d365-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="1d365-143">移除-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d365-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="1d365-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d365-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
