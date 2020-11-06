---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: f21c8303f1ec156132653a5d05c1149ef10a9ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613552"
---
# <span data-ttu-id="0b036-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0b036-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="0b036-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b036-102">SYNOPSIS</span></span>
<span data-ttu-id="0b036-103">取得 CDN 端點的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="0b036-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="0b036-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b036-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b036-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b036-105">DESCRIPTION</span></span>
<span data-ttu-id="0b036-106">**AzCdnEndpointNameAvailability** Cmdlet 會取得 Azure 內容傳遞網路 (CDN) 端點的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="0b036-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0b036-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b036-107">EXAMPLES</span></span>

## <span data-ttu-id="0b036-108">參數</span><span class="sxs-lookup"><span data-stu-id="0b036-108">PARAMETERS</span></span>

### <span data-ttu-id="0b036-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b036-109">-DefaultProfile</span></span>
<span data-ttu-id="0b036-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0b036-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b036-111">-終結點</span><span class="sxs-lookup"><span data-stu-id="0b036-111">-EndpointName</span></span>
<span data-ttu-id="0b036-112">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b036-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="0b036-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b036-113">CommonParameters</span></span>
<span data-ttu-id="0b036-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b036-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b036-115">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b036-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b036-116">輸入</span><span class="sxs-lookup"><span data-stu-id="0b036-116">INPUTS</span></span>

### <span data-ttu-id="0b036-117">所有</span><span class="sxs-lookup"><span data-stu-id="0b036-117">None</span></span>

## <span data-ttu-id="0b036-118">輸出</span><span class="sxs-lookup"><span data-stu-id="0b036-118">OUTPUTS</span></span>

### <span data-ttu-id="0b036-119">[PSCheckNameAvailabilityOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="0b036-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="0b036-120">筆記</span><span class="sxs-lookup"><span data-stu-id="0b036-120">NOTES</span></span>

## <span data-ttu-id="0b036-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b036-121">RELATED LINKS</span></span>
