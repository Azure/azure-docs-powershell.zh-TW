---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9b47fb1954b13e28268f6b7aad66fa8190e20584
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789733"
---
# <span data-ttu-id="bdce5-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdce5-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="bdce5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdce5-102">SYNOPSIS</span></span>
<span data-ttu-id="bdce5-103">核准私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="bdce5-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="bdce5-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdce5-104">SYNTAX</span></span>

### <span data-ttu-id="bdce5-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="bdce5-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdce5-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="bdce5-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdce5-107">說明</span><span class="sxs-lookup"><span data-stu-id="bdce5-107">DESCRIPTION</span></span>
<span data-ttu-id="bdce5-108">**核准-AzPrivateEndpointConnection** Cmdlet 會核准私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="bdce5-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="bdce5-109">示例</span><span class="sxs-lookup"><span data-stu-id="bdce5-109">EXAMPLES</span></span>

### <span data-ttu-id="bdce5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bdce5-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="bdce5-111">這個範例會核准私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="bdce5-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="bdce5-112">參數</span><span class="sxs-lookup"><span data-stu-id="bdce5-112">PARAMETERS</span></span>

### <span data-ttu-id="bdce5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdce5-113">-DefaultProfile</span></span>
<span data-ttu-id="bdce5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdce5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdce5-115">-描述</span><span class="sxs-lookup"><span data-stu-id="bdce5-115">-Description</span></span>
<span data-ttu-id="bdce5-116">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="bdce5-116">The reason of action.</span></span>

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

### <span data-ttu-id="bdce5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdce5-117">-Name</span></span>
<span data-ttu-id="bdce5-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bdce5-118">The resource name.</span></span>

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

### <span data-ttu-id="bdce5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdce5-119">-ResourceGroupName</span></span>
<span data-ttu-id="bdce5-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bdce5-120">The resource group name.</span></span>

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

### <span data-ttu-id="bdce5-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdce5-121">-ResourceId</span></span>
<span data-ttu-id="bdce5-122">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="bdce5-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="bdce5-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bdce5-123">-ServiceName</span></span>
<span data-ttu-id="bdce5-124">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="bdce5-124">The private link service name.</span></span>

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

### <span data-ttu-id="bdce5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdce5-125">CommonParameters</span></span>
<span data-ttu-id="bdce5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdce5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdce5-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bdce5-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdce5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bdce5-128">INPUTS</span></span>

### <span data-ttu-id="bdce5-129">System.object</span><span class="sxs-lookup"><span data-stu-id="bdce5-129">System.String</span></span>

## <span data-ttu-id="bdce5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bdce5-130">OUTPUTS</span></span>

### <span data-ttu-id="bdce5-131">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bdce5-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="bdce5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="bdce5-132">NOTES</span></span>

## <span data-ttu-id="bdce5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdce5-133">RELATED LINKS</span></span>

[<span data-ttu-id="bdce5-134">AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdce5-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="bdce5-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdce5-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="bdce5-136">移除-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdce5-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)