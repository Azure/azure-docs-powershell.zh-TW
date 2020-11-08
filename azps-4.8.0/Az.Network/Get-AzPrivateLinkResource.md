---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126495"
---
# <span data-ttu-id="a7347-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a7347-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="a7347-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7347-102">SYNOPSIS</span></span>
<span data-ttu-id="a7347-103">取得私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="a7347-103">Gets a private link resource.</span></span>

## <span data-ttu-id="a7347-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7347-104">SYNTAX</span></span>

### <span data-ttu-id="a7347-105">ByPrivateLinkResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="a7347-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7347-106">說明</span><span class="sxs-lookup"><span data-stu-id="a7347-106">DESCRIPTION</span></span>
<span data-ttu-id="a7347-107">AzPrivateLinkResource Cmdlet 會 **取得** 所有連結資源（屬於 PrivateLinkResource）。</span><span class="sxs-lookup"><span data-stu-id="a7347-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="a7347-108">示例</span><span class="sxs-lookup"><span data-stu-id="a7347-108">EXAMPLES</span></span>

### <span data-ttu-id="a7347-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a7347-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a7347-110">這個範例會列出 nbelong 至 sql server （名為 mySql）的所有私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="a7347-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="a7347-111">參數</span><span class="sxs-lookup"><span data-stu-id="a7347-111">PARAMETERS</span></span>

### <span data-ttu-id="a7347-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7347-112">-DefaultProfile</span></span>
<span data-ttu-id="a7347-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7347-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7347-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a7347-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a7347-115">私人連結資源的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7347-115">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="a7347-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7347-116">CommonParameters</span></span>
<span data-ttu-id="a7347-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7347-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7347-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a7347-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7347-119">輸入</span><span class="sxs-lookup"><span data-stu-id="a7347-119">INPUTS</span></span>

### <span data-ttu-id="a7347-120">System.object</span><span class="sxs-lookup"><span data-stu-id="a7347-120">System.String</span></span>

## <span data-ttu-id="a7347-121">輸出</span><span class="sxs-lookup"><span data-stu-id="a7347-121">OUTPUTS</span></span>

### <span data-ttu-id="a7347-122">System.object</span><span class="sxs-lookup"><span data-stu-id="a7347-122">System.Boolean</span></span>

## <span data-ttu-id="a7347-123">筆記</span><span class="sxs-lookup"><span data-stu-id="a7347-123">NOTES</span></span>

## <span data-ttu-id="a7347-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7347-124">RELATED LINKS</span></span>
