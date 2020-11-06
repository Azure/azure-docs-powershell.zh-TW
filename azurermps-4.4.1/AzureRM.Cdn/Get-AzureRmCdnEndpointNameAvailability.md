---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: 6c5c11123ab39d92bb7b702542b007c8c075f9b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452576"
---
# <span data-ttu-id="b83de-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b83de-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="b83de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b83de-102">SYNOPSIS</span></span>
<span data-ttu-id="b83de-103">取得 CDN 端點的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="b83de-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b83de-104">句法</span><span class="sxs-lookup"><span data-stu-id="b83de-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b83de-105">說明</span><span class="sxs-lookup"><span data-stu-id="b83de-105">DESCRIPTION</span></span>
<span data-ttu-id="b83de-106">**AzureRmCdnEndpointNameAvailability** Cmdlet 會取得 Azure 內容傳遞網路 (CDN) 端點的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="b83de-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b83de-107">示例</span><span class="sxs-lookup"><span data-stu-id="b83de-107">EXAMPLES</span></span>

## <span data-ttu-id="b83de-108">參數</span><span class="sxs-lookup"><span data-stu-id="b83de-108">PARAMETERS</span></span>

### <span data-ttu-id="b83de-109">-終結點</span><span class="sxs-lookup"><span data-stu-id="b83de-109">-EndpointName</span></span>
<span data-ttu-id="b83de-110">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b83de-110">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="b83de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83de-111">-DefaultProfile</span></span>
<span data-ttu-id="b83de-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b83de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b83de-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83de-113">CommonParameters</span></span>
<span data-ttu-id="b83de-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b83de-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83de-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b83de-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83de-116">輸入</span><span class="sxs-lookup"><span data-stu-id="b83de-116">INPUTS</span></span>

## <span data-ttu-id="b83de-117">輸出</span><span class="sxs-lookup"><span data-stu-id="b83de-117">OUTPUTS</span></span>

### <span data-ttu-id="b83de-118">[PSCheckNameAvailabilityOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="b83de-118">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="b83de-119">筆記</span><span class="sxs-lookup"><span data-stu-id="b83de-119">NOTES</span></span>

## <span data-ttu-id="b83de-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="b83de-120">RELATED LINKS</span></span>

