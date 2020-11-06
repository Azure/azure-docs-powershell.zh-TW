---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 28f285ef55acbca3c4226f198f69fb9a70b62364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613550"
---
# <span data-ttu-id="6ac04-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="6ac04-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="6ac04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ac04-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac04-103">取得 CDN 端點的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="6ac04-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="6ac04-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ac04-104">SYNTAX</span></span>

### <span data-ttu-id="6ac04-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6ac04-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ac04-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ac04-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ac04-107">說明</span><span class="sxs-lookup"><span data-stu-id="6ac04-107">DESCRIPTION</span></span>
<span data-ttu-id="6ac04-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="6ac04-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6ac04-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ac04-109">EXAMPLES</span></span>

### <span data-ttu-id="6ac04-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6ac04-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6ac04-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="6ac04-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="6ac04-112">參數</span><span class="sxs-lookup"><span data-stu-id="6ac04-112">PARAMETERS</span></span>

### <span data-ttu-id="6ac04-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ac04-113">-CdnEndpoint</span></span>
<span data-ttu-id="6ac04-114">CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="6ac04-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac04-115">-DefaultProfile</span></span>
<span data-ttu-id="6ac04-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6ac04-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ac04-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="6ac04-117">-EndpointName</span></span>
<span data-ttu-id="6ac04-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac04-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="6ac04-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6ac04-119">-ProfileName</span></span>
<span data-ttu-id="6ac04-120">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac04-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac04-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac04-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ac04-122">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="6ac04-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac04-123">CommonParameters</span></span>
<span data-ttu-id="6ac04-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ac04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac04-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6ac04-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac04-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6ac04-126">INPUTS</span></span>

### <span data-ttu-id="6ac04-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="6ac04-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="6ac04-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6ac04-128">OUTPUTS</span></span>

### <span data-ttu-id="6ac04-129">PSResourceUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ac04-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="6ac04-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6ac04-130">NOTES</span></span>

## <span data-ttu-id="6ac04-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ac04-131">RELATED LINKS</span></span>
