---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141410"
---
# <span data-ttu-id="98649-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="98649-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="98649-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98649-102">SYNOPSIS</span></span>
<span data-ttu-id="98649-103">取得 CDN 端點的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="98649-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="98649-104">句法</span><span class="sxs-lookup"><span data-stu-id="98649-104">SYNTAX</span></span>

### <span data-ttu-id="98649-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="98649-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98649-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98649-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98649-107">說明</span><span class="sxs-lookup"><span data-stu-id="98649-107">DESCRIPTION</span></span>
<span data-ttu-id="98649-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="98649-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="98649-109">示例</span><span class="sxs-lookup"><span data-stu-id="98649-109">EXAMPLES</span></span>

### <span data-ttu-id="98649-110">範例1</span><span class="sxs-lookup"><span data-stu-id="98649-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="98649-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="98649-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="98649-112">參數</span><span class="sxs-lookup"><span data-stu-id="98649-112">PARAMETERS</span></span>

### <span data-ttu-id="98649-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98649-113">-CdnEndpoint</span></span>
<span data-ttu-id="98649-114">CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="98649-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="98649-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98649-115">-DefaultProfile</span></span>
<span data-ttu-id="98649-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="98649-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98649-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="98649-117">-EndpointName</span></span>
<span data-ttu-id="98649-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="98649-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="98649-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="98649-119">-ProfileName</span></span>
<span data-ttu-id="98649-120">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="98649-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="98649-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98649-121">-ResourceGroupName</span></span>
<span data-ttu-id="98649-122">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="98649-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="98649-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98649-123">CommonParameters</span></span>
<span data-ttu-id="98649-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98649-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98649-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98649-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98649-126">輸入</span><span class="sxs-lookup"><span data-stu-id="98649-126">INPUTS</span></span>

### <span data-ttu-id="98649-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="98649-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="98649-128">輸出</span><span class="sxs-lookup"><span data-stu-id="98649-128">OUTPUTS</span></span>

### <span data-ttu-id="98649-129">PSResourceUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="98649-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="98649-130">筆記</span><span class="sxs-lookup"><span data-stu-id="98649-130">NOTES</span></span>

## <span data-ttu-id="98649-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="98649-131">RELATED LINKS</span></span>
