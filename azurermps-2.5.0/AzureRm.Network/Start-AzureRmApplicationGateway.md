---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801570"
---
# <span data-ttu-id="92561-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92561-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="92561-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92561-102">SYNOPSIS</span></span>
<span data-ttu-id="92561-103">啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="92561-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92561-104">句法</span><span class="sxs-lookup"><span data-stu-id="92561-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92561-105">說明</span><span class="sxs-lookup"><span data-stu-id="92561-105">DESCRIPTION</span></span>
<span data-ttu-id="92561-106">**AzureRmApplicationGateway** Cmdlet 會啟動 Azure 應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="92561-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="92561-107">示例</span><span class="sxs-lookup"><span data-stu-id="92561-107">EXAMPLES</span></span>

### <span data-ttu-id="92561-108">Example1：啟動應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="92561-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="92561-109">這個命令會啟動儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="92561-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="92561-110">參數</span><span class="sxs-lookup"><span data-stu-id="92561-110">PARAMETERS</span></span>

### <span data-ttu-id="92561-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92561-111">-ApplicationGateway</span></span>
<span data-ttu-id="92561-112">指定此 Cmdlet 啟動的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="92561-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92561-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92561-113">-DefaultProfile</span></span>
<span data-ttu-id="92561-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92561-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92561-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92561-115">CommonParameters</span></span>
<span data-ttu-id="92561-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92561-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92561-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92561-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92561-118">輸入</span><span class="sxs-lookup"><span data-stu-id="92561-118">INPUTS</span></span>

### <span data-ttu-id="92561-119">System.object</span><span class="sxs-lookup"><span data-stu-id="92561-119">System.String</span></span>

## <span data-ttu-id="92561-120">輸出</span><span class="sxs-lookup"><span data-stu-id="92561-120">OUTPUTS</span></span>

### <span data-ttu-id="92561-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="92561-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92561-122">筆記</span><span class="sxs-lookup"><span data-stu-id="92561-122">NOTES</span></span>

## <span data-ttu-id="92561-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="92561-123">RELATED LINKS</span></span>

[<span data-ttu-id="92561-124">停止 AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92561-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


