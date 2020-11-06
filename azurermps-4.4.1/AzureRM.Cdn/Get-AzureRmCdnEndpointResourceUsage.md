---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457288"
---
# <span data-ttu-id="f923d-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f923d-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="f923d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f923d-102">SYNOPSIS</span></span>
<span data-ttu-id="f923d-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="f923d-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f923d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f923d-104">SYNTAX</span></span>

### <span data-ttu-id="f923d-105">預設)  (欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="f923d-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f923d-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="f923d-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f923d-107">說明</span><span class="sxs-lookup"><span data-stu-id="f923d-107">DESCRIPTION</span></span>
<span data-ttu-id="f923d-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="f923d-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f923d-109">示例</span><span class="sxs-lookup"><span data-stu-id="f923d-109">EXAMPLES</span></span>

### <span data-ttu-id="f923d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f923d-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f923d-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="f923d-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="f923d-112">參數</span><span class="sxs-lookup"><span data-stu-id="f923d-112">PARAMETERS</span></span>

### <span data-ttu-id="f923d-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f923d-113">-CdnEndpoint</span></span>
<span data-ttu-id="f923d-114">CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="f923d-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f923d-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="f923d-115">-EndpointName</span></span>
<span data-ttu-id="f923d-116">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="f923d-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f923d-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f923d-117">-ProfileName</span></span>
<span data-ttu-id="f923d-118">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f923d-118">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f923d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f923d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f923d-120">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f923d-120">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f923d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f923d-121">-DefaultProfile</span></span>
<span data-ttu-id="f923d-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f923d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f923d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f923d-123">CommonParameters</span></span>
<span data-ttu-id="f923d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f923d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f923d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f923d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f923d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f923d-126">INPUTS</span></span>

### <span data-ttu-id="f923d-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="f923d-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f923d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f923d-128">OUTPUTS</span></span>

### <span data-ttu-id="f923d-129">PSResourceUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f923d-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="f923d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f923d-130">NOTES</span></span>

## <span data-ttu-id="f923d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f923d-131">RELATED LINKS</span></span>

