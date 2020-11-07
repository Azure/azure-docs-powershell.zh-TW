---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791605"
---
# <span data-ttu-id="e0493-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e0493-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e0493-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0493-102">SYNOPSIS</span></span>
<span data-ttu-id="e0493-103">更新私人連結服務上的私人端點線上狀態。</span><span class="sxs-lookup"><span data-stu-id="e0493-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="e0493-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0493-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0493-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0493-105">DESCRIPTION</span></span>
<span data-ttu-id="e0493-106">**AzPrivateEndpointConnection** Cmdlet 會更新私人連結服務上的私人端點線上狀態</span><span class="sxs-lookup"><span data-stu-id="e0493-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="e0493-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0493-107">EXAMPLES</span></span>

### <span data-ttu-id="e0493-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e0493-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="e0493-109">這個範例會將私人端點線上狀態更新為 [已核准]。</span><span class="sxs-lookup"><span data-stu-id="e0493-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="e0493-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0493-110">PARAMETERS</span></span>

### <span data-ttu-id="e0493-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0493-111">-DefaultProfile</span></span>
<span data-ttu-id="e0493-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0493-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0493-113">-描述</span><span class="sxs-lookup"><span data-stu-id="e0493-113">-Description</span></span>
<span data-ttu-id="e0493-114">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="e0493-114">The reason of action.</span></span>

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

### <span data-ttu-id="e0493-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0493-115">-Name</span></span>
<span data-ttu-id="e0493-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e0493-116">The resource name.</span></span>

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

### <span data-ttu-id="e0493-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="e0493-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="e0493-118">已核准或拒絕資源。</span><span class="sxs-lookup"><span data-stu-id="e0493-118">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="e0493-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0493-119">-ResourceGroupName</span></span>
<span data-ttu-id="e0493-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0493-120">The resource group name.</span></span>

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

### <span data-ttu-id="e0493-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e0493-121">-ServiceName</span></span>
<span data-ttu-id="e0493-122">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e0493-122">The private link service name.</span></span>

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

### <span data-ttu-id="e0493-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0493-123">CommonParameters</span></span>
<span data-ttu-id="e0493-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0493-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0493-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e0493-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0493-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e0493-126">INPUTS</span></span>

### <span data-ttu-id="e0493-127">System.object</span><span class="sxs-lookup"><span data-stu-id="e0493-127">System.String</span></span>

## <span data-ttu-id="e0493-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e0493-128">OUTPUTS</span></span>

### <span data-ttu-id="e0493-129">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e0493-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e0493-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e0493-130">NOTES</span></span>

## <span data-ttu-id="e0493-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0493-131">RELATED LINKS</span></span>
