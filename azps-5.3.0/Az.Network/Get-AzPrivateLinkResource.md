---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287448"
---
# <span data-ttu-id="769d2-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="769d2-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="769d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="769d2-102">SYNOPSIS</span></span>
<span data-ttu-id="769d2-103">取得私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="769d2-103">Gets a private link resource.</span></span>

## <span data-ttu-id="769d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="769d2-104">SYNTAX</span></span>

### <span data-ttu-id="769d2-105">ByPrivateLinkResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="769d2-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="769d2-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="769d2-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="769d2-107">說明</span><span class="sxs-lookup"><span data-stu-id="769d2-107">DESCRIPTION</span></span>
<span data-ttu-id="769d2-108">AzPrivateLinkResource Cmdlet 會 **取得** 所有連結資源（屬於 PrivateLinkResource）。</span><span class="sxs-lookup"><span data-stu-id="769d2-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="769d2-109">示例</span><span class="sxs-lookup"><span data-stu-id="769d2-109">EXAMPLES</span></span>

### <span data-ttu-id="769d2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="769d2-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="769d2-111">這個範例會列出 nbelong 至 sql server （名為 mySql）的所有私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="769d2-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="769d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="769d2-112">PARAMETERS</span></span>

### <span data-ttu-id="769d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769d2-113">-DefaultProfile</span></span>
<span data-ttu-id="769d2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="769d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="769d2-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="769d2-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="769d2-116">私人連結資源的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="769d2-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="769d2-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="769d2-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="769d2-118">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="769d2-118">The private link resource type.</span></span>

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

### <span data-ttu-id="769d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="769d2-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="769d2-120">The resource group name.</span></span>

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

### <span data-ttu-id="769d2-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="769d2-121">-ServiceName</span></span>
<span data-ttu-id="769d2-122">私人連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="769d2-122">The private link service name.</span></span>

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

### <span data-ttu-id="769d2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769d2-123">CommonParameters</span></span>
<span data-ttu-id="769d2-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="769d2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769d2-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="769d2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769d2-126">輸入</span><span class="sxs-lookup"><span data-stu-id="769d2-126">INPUTS</span></span>

### <span data-ttu-id="769d2-127">System.object</span><span class="sxs-lookup"><span data-stu-id="769d2-127">System.String</span></span>

## <span data-ttu-id="769d2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="769d2-128">OUTPUTS</span></span>

### <span data-ttu-id="769d2-129">System.object</span><span class="sxs-lookup"><span data-stu-id="769d2-129">System.Boolean</span></span>

## <span data-ttu-id="769d2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="769d2-130">NOTES</span></span>

## <span data-ttu-id="769d2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="769d2-131">RELATED LINKS</span></span>
