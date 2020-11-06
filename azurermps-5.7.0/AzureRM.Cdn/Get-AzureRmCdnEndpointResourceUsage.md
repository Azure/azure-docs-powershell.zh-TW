---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455528"
---
# <span data-ttu-id="dc093-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="dc093-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="dc093-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc093-102">SYNOPSIS</span></span>
<span data-ttu-id="dc093-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="dc093-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc093-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc093-104">SYNTAX</span></span>

### <span data-ttu-id="dc093-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc093-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc093-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc093-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc093-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc093-107">DESCRIPTION</span></span>
<span data-ttu-id="dc093-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="dc093-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="dc093-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc093-109">EXAMPLES</span></span>

### <span data-ttu-id="dc093-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dc093-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="dc093-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="dc093-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="dc093-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc093-112">PARAMETERS</span></span>

### <span data-ttu-id="dc093-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc093-113">-CdnEndpoint</span></span>
<span data-ttu-id="dc093-114">CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="dc093-114">The CDN endpoint object.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc093-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc093-115">-DefaultProfile</span></span>
<span data-ttu-id="dc093-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dc093-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc093-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="dc093-117">-EndpointName</span></span>
<span data-ttu-id="dc093-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="dc093-118">Azure CDN endpoint name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc093-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="dc093-119">-ProfileName</span></span>
<span data-ttu-id="dc093-120">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="dc093-120">Azure CDN profile name.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc093-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc093-121">-ResourceGroupName</span></span>
<span data-ttu-id="dc093-122">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="dc093-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc093-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc093-123">CommonParameters</span></span>
<span data-ttu-id="dc093-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc093-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc093-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc093-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc093-126">輸入</span><span class="sxs-lookup"><span data-stu-id="dc093-126">INPUTS</span></span>

### <span data-ttu-id="dc093-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="dc093-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="dc093-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dc093-128">OUTPUTS</span></span>

### <span data-ttu-id="dc093-129">PSResourceUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc093-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="dc093-130">筆記</span><span class="sxs-lookup"><span data-stu-id="dc093-130">NOTES</span></span>

## <span data-ttu-id="dc093-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc093-131">RELATED LINKS</span></span>

