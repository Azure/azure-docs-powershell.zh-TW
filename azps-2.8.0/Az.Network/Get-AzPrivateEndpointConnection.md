---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789530"
---
# <span data-ttu-id="e3fbd-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3fbd-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e3fbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fbd-103">取得私用端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="e3fbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3fbd-104">SYNTAX</span></span>

### <span data-ttu-id="e3fbd-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="e3fbd-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3fbd-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="e3fbd-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3fbd-107">說明</span><span class="sxs-lookup"><span data-stu-id="e3fbd-107">DESCRIPTION</span></span>
<span data-ttu-id="e3fbd-108">**AzPrivateEndpointConnection** Cmdlet 會檢索私人端點連接資源。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="e3fbd-109">示例</span><span class="sxs-lookup"><span data-stu-id="e3fbd-109">EXAMPLES</span></span>

### <span data-ttu-id="e3fbd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e3fbd-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="e3fbd-111">這個範例會取得名為 MyPrivateEndpointConnection1 的私人端點連接</span><span class="sxs-lookup"><span data-stu-id="e3fbd-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="e3fbd-112">參數</span><span class="sxs-lookup"><span data-stu-id="e3fbd-112">PARAMETERS</span></span>

### <span data-ttu-id="e3fbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fbd-113">-DefaultProfile</span></span>
<span data-ttu-id="e3fbd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3fbd-115">-描述</span><span class="sxs-lookup"><span data-stu-id="e3fbd-115">-Description</span></span>
<span data-ttu-id="e3fbd-116">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-116">The reason of action.</span></span>

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

### <span data-ttu-id="e3fbd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3fbd-117">-Name</span></span>
<span data-ttu-id="e3fbd-118">私人端點連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-118">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e3fbd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fbd-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3fbd-120">私人端點連線的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-120">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e3fbd-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3fbd-121">-ResourceId</span></span>
<span data-ttu-id="e3fbd-122">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e3fbd-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e3fbd-123">-ServiceName</span></span>
<span data-ttu-id="e3fbd-124">具有專用端點連線之專用連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-124">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="e3fbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fbd-125">CommonParameters</span></span>
<span data-ttu-id="e3fbd-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fbd-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3fbd-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fbd-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e3fbd-128">INPUTS</span></span>

### <span data-ttu-id="e3fbd-129">System.object</span><span class="sxs-lookup"><span data-stu-id="e3fbd-129">System.String</span></span>

## <span data-ttu-id="e3fbd-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e3fbd-130">OUTPUTS</span></span>

### <span data-ttu-id="e3fbd-131">System.object</span><span class="sxs-lookup"><span data-stu-id="e3fbd-131">System.Boolean</span></span>

## <span data-ttu-id="e3fbd-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e3fbd-132">NOTES</span></span>

## <span data-ttu-id="e3fbd-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3fbd-133">RELATED LINKS</span></span>

[<span data-ttu-id="e3fbd-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3fbd-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
