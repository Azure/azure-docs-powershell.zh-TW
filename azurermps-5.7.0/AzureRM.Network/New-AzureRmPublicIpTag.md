---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 56352ff165d2e7dcbf5386e713028fae5c991d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455376"
---
# <span data-ttu-id="7d56b-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="7d56b-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="7d56b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d56b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d56b-103">建立 IP 標籤。</span><span class="sxs-lookup"><span data-stu-id="7d56b-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d56b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d56b-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7d56b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d56b-105">DESCRIPTION</span></span>
<span data-ttu-id="7d56b-106">**新的-AzureRmPublicIpTag** Cmdlet 會建立 IP 標記。</span><span class="sxs-lookup"><span data-stu-id="7d56b-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="7d56b-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d56b-107">EXAMPLES</span></span>

### <span data-ttu-id="7d56b-108">1：建立新的 IP 標籤</span><span class="sxs-lookup"><span data-stu-id="7d56b-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="7d56b-109">這個命令會使用 Tagtype （例如「FirstPartyUsage」）及標記（例如「/Sql」）來建立新的 IP 標記。</span><span class="sxs-lookup"><span data-stu-id="7d56b-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="7d56b-110">在 publicIpAddress 建立中使用這些特定標籤來進行分配。</span><span class="sxs-lookup"><span data-stu-id="7d56b-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="7d56b-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d56b-111">PARAMETERS</span></span>

### <span data-ttu-id="7d56b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d56b-112">-DefaultProfile</span></span>
<span data-ttu-id="7d56b-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d56b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d56b-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="7d56b-114">-IpTagType</span></span>
<span data-ttu-id="7d56b-115">IpTag 類型範例： FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="7d56b-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d56b-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d56b-116">-Tag</span></span>
<span data-ttu-id="7d56b-117">IpTag 值範例：/Sql</span><span class="sxs-lookup"><span data-stu-id="7d56b-117">IpTag value Example:/Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d56b-118">-確認</span><span class="sxs-lookup"><span data-stu-id="7d56b-118">-Confirm</span></span>
<span data-ttu-id="7d56b-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d56b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d56b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d56b-120">-WhatIf</span></span>
<span data-ttu-id="7d56b-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d56b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d56b-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d56b-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="7d56b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7d56b-123">INPUTS</span></span>

### <span data-ttu-id="7d56b-124">System.object</span><span class="sxs-lookup"><span data-stu-id="7d56b-124">System.String</span></span>


## <span data-ttu-id="7d56b-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7d56b-125">OUTPUTS</span></span>

### <span data-ttu-id="7d56b-126">PSPublicIpTag 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d56b-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>


## <span data-ttu-id="7d56b-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7d56b-127">NOTES</span></span>

## <span data-ttu-id="7d56b-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d56b-128">RELATED LINKS</span></span>

