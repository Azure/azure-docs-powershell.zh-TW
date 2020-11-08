---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126359"
---
# <span data-ttu-id="52d12-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52d12-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="52d12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52d12-102">SYNOPSIS</span></span>
<span data-ttu-id="52d12-103">啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="52d12-103">Starts an application gateway.</span></span>

## <span data-ttu-id="52d12-104">句法</span><span class="sxs-lookup"><span data-stu-id="52d12-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d12-105">說明</span><span class="sxs-lookup"><span data-stu-id="52d12-105">DESCRIPTION</span></span>
<span data-ttu-id="52d12-106">**AzApplicationGateway** Cmdlet 會啟動 Azure 應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="52d12-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="52d12-107">示例</span><span class="sxs-lookup"><span data-stu-id="52d12-107">EXAMPLES</span></span>

### <span data-ttu-id="52d12-108">Example1：啟動應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="52d12-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="52d12-109">這個命令會啟動儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="52d12-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="52d12-110">參數</span><span class="sxs-lookup"><span data-stu-id="52d12-110">PARAMETERS</span></span>

### <span data-ttu-id="52d12-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52d12-111">-ApplicationGateway</span></span>
<span data-ttu-id="52d12-112">指定此 Cmdlet 啟動的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="52d12-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="52d12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d12-113">-DefaultProfile</span></span>
<span data-ttu-id="52d12-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52d12-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d12-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d12-115">CommonParameters</span></span>
<span data-ttu-id="52d12-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52d12-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d12-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52d12-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d12-118">輸入</span><span class="sxs-lookup"><span data-stu-id="52d12-118">INPUTS</span></span>

### <span data-ttu-id="52d12-119">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52d12-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="52d12-120">輸出</span><span class="sxs-lookup"><span data-stu-id="52d12-120">OUTPUTS</span></span>

### <span data-ttu-id="52d12-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52d12-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="52d12-122">筆記</span><span class="sxs-lookup"><span data-stu-id="52d12-122">NOTES</span></span>

## <span data-ttu-id="52d12-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="52d12-123">RELATED LINKS</span></span>

[<span data-ttu-id="52d12-124">停止 AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52d12-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


