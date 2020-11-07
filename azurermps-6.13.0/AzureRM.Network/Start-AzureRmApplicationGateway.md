---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624236"
---
# <span data-ttu-id="366d4-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="366d4-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="366d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="366d4-102">SYNOPSIS</span></span>
<span data-ttu-id="366d4-103">啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="366d4-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="366d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="366d4-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="366d4-105">說明</span><span class="sxs-lookup"><span data-stu-id="366d4-105">DESCRIPTION</span></span>
<span data-ttu-id="366d4-106">**AzureRmApplicationGateway** Cmdlet 會啟動 Azure 應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="366d4-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="366d4-107">示例</span><span class="sxs-lookup"><span data-stu-id="366d4-107">EXAMPLES</span></span>

### <span data-ttu-id="366d4-108">Example1：啟動應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="366d4-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="366d4-109">這個命令會啟動儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="366d4-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="366d4-110">參數</span><span class="sxs-lookup"><span data-stu-id="366d4-110">PARAMETERS</span></span>

### <span data-ttu-id="366d4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="366d4-111">-ApplicationGateway</span></span>
<span data-ttu-id="366d4-112">指定此 Cmdlet 啟動的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="366d4-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="366d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366d4-113">-DefaultProfile</span></span>
<span data-ttu-id="366d4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="366d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="366d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366d4-115">CommonParameters</span></span>
<span data-ttu-id="366d4-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="366d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366d4-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="366d4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366d4-118">輸入</span><span class="sxs-lookup"><span data-stu-id="366d4-118">INPUTS</span></span>

### <span data-ttu-id="366d4-119">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="366d4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="366d4-120">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="366d4-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="366d4-121">輸出</span><span class="sxs-lookup"><span data-stu-id="366d4-121">OUTPUTS</span></span>

### <span data-ttu-id="366d4-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="366d4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="366d4-123">筆記</span><span class="sxs-lookup"><span data-stu-id="366d4-123">NOTES</span></span>

## <span data-ttu-id="366d4-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="366d4-124">RELATED LINKS</span></span>

[<span data-ttu-id="366d4-125">停止 AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="366d4-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


