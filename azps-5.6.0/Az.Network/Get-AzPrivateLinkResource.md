---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 5c341677f5bc741f5848508f80b1a29e29c90b17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902473"
---
# <span data-ttu-id="5c2bd-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="5c2bd-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="5c2bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2bd-103">獲得私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-103">Gets a private link resource.</span></span>

## <span data-ttu-id="5c2bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c2bd-104">SYNTAX</span></span>

### <span data-ttu-id="5c2bd-105">ByPrivateLinkResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="5c2bd-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c2bd-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="5c2bd-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="5c2bd-107">描述</span><span class="sxs-lookup"><span data-stu-id="5c2bd-107">DESCRIPTION</span></span>
<span data-ttu-id="5c2bd-108">**Get-AzPrivateLinkResource** Cmdlet 會取得屬於 PrivateLinkResource 的所有連結資源。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="5c2bd-109">例子</span><span class="sxs-lookup"><span data-stu-id="5c2bd-109">EXAMPLES</span></span>

### <span data-ttu-id="5c2bd-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5c2bd-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="5c2bd-111">此範例列出名為 mySql 的所有私人連結資源 nbelong 到 sql server。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="5c2bd-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c2bd-112">PARAMETERS</span></span>

### <span data-ttu-id="5c2bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2bd-113">-DefaultProfile</span></span>
<span data-ttu-id="5c2bd-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2bd-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="5c2bd-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="5c2bd-116">私人連結資源的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="5c2bd-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="5c2bd-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="5c2bd-118">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c2bd-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-120">The resource group name.</span></span>

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

### <span data-ttu-id="5c2bd-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5c2bd-121">-ServiceName</span></span>
<span data-ttu-id="5c2bd-122">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-122">The private link service name.</span></span>

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

### <span data-ttu-id="5c2bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2bd-123">CommonParameters</span></span>
<span data-ttu-id="5c2bd-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c2bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2bd-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c2bd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2bd-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5c2bd-126">INPUTS</span></span>

### <span data-ttu-id="5c2bd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5c2bd-127">System.String</span></span>

## <span data-ttu-id="5c2bd-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5c2bd-128">OUTPUTS</span></span>

### <span data-ttu-id="5c2bd-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c2bd-129">System.Boolean</span></span>

## <span data-ttu-id="5c2bd-130">筆記</span><span class="sxs-lookup"><span data-stu-id="5c2bd-130">NOTES</span></span>

## <span data-ttu-id="5c2bd-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c2bd-131">RELATED LINKS</span></span>
