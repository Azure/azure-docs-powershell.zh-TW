---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 4d2f3f225e185678dd1e3b0047810a5e68d4273f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901922"
---
# <span data-ttu-id="8a4a4-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a4a4-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="8a4a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4a4-103">啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8a4a4-103">Starts an application gateway.</span></span>

## <span data-ttu-id="8a4a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a4a4-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a4a4-105">描述</span><span class="sxs-lookup"><span data-stu-id="8a4a4-105">DESCRIPTION</span></span>
<span data-ttu-id="8a4a4-106">**Start-AzApplicationGateway** Cmdlet 會啟動 Azure 應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="8a4a4-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="8a4a4-107">例子</span><span class="sxs-lookup"><span data-stu-id="8a4a4-107">EXAMPLES</span></span>

### <span data-ttu-id="8a4a4-108">範例1：啟動應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="8a4a4-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="8a4a4-109">此命令會啟動儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8a4a4-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="8a4a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="8a4a4-110">PARAMETERS</span></span>

### <span data-ttu-id="8a4a4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a4a4-111">-ApplicationGateway</span></span>
<span data-ttu-id="8a4a4-112">指定此 Cmdlet 啟動的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8a4a4-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8a4a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4a4-113">-DefaultProfile</span></span>
<span data-ttu-id="8a4a4-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a4a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a4a4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4a4-115">CommonParameters</span></span>
<span data-ttu-id="8a4a4-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a4a4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4a4-117">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8a4a4-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4a4-118">輸入</span><span class="sxs-lookup"><span data-stu-id="8a4a4-118">INPUTS</span></span>

### <span data-ttu-id="8a4a4-119">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a4a4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a4a4-120">輸出</span><span class="sxs-lookup"><span data-stu-id="8a4a4-120">OUTPUTS</span></span>

### <span data-ttu-id="8a4a4-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a4a4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a4a4-122">筆記</span><span class="sxs-lookup"><span data-stu-id="8a4a4-122">NOTES</span></span>

## <span data-ttu-id="8a4a4-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a4a4-123">RELATED LINKS</span></span>

[<span data-ttu-id="8a4a4-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a4a4-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


