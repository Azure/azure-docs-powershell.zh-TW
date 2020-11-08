---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140991"
---
# <span data-ttu-id="0dbf6-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0dbf6-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="0dbf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbf6-103">取得 CDN 端點的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="0dbf6-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="0dbf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dbf6-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dbf6-105">說明</span><span class="sxs-lookup"><span data-stu-id="0dbf6-105">DESCRIPTION</span></span>
<span data-ttu-id="0dbf6-106">**AzCdnEndpointNameAvailability** Cmdlet 會取得 Azure 內容傳遞網路 (CDN) 端點的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="0dbf6-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0dbf6-107">示例</span><span class="sxs-lookup"><span data-stu-id="0dbf6-107">EXAMPLES</span></span>

## <span data-ttu-id="0dbf6-108">參數</span><span class="sxs-lookup"><span data-stu-id="0dbf6-108">PARAMETERS</span></span>

### <span data-ttu-id="0dbf6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbf6-109">-DefaultProfile</span></span>
<span data-ttu-id="0dbf6-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0dbf6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dbf6-111">-終結點</span><span class="sxs-lookup"><span data-stu-id="0dbf6-111">-EndpointName</span></span>
<span data-ttu-id="0dbf6-112">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dbf6-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbf6-113">CommonParameters</span></span>
<span data-ttu-id="0dbf6-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dbf6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbf6-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0dbf6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbf6-116">輸入</span><span class="sxs-lookup"><span data-stu-id="0dbf6-116">INPUTS</span></span>

### <span data-ttu-id="0dbf6-117">所有</span><span class="sxs-lookup"><span data-stu-id="0dbf6-117">None</span></span>

## <span data-ttu-id="0dbf6-118">輸出</span><span class="sxs-lookup"><span data-stu-id="0dbf6-118">OUTPUTS</span></span>

### <span data-ttu-id="0dbf6-119">[PSCheckNameAvailabilityOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="0dbf6-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="0dbf6-120">筆記</span><span class="sxs-lookup"><span data-stu-id="0dbf6-120">NOTES</span></span>

## <span data-ttu-id="0dbf6-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dbf6-121">RELATED LINKS</span></span>
