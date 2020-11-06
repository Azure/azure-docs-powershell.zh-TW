---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446710"
---
# <span data-ttu-id="6a489-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a489-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="6a489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a489-102">SYNOPSIS</span></span>
<span data-ttu-id="6a489-103">停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="6a489-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a489-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a489-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a489-105">說明</span><span class="sxs-lookup"><span data-stu-id="6a489-105">DESCRIPTION</span></span>
<span data-ttu-id="6a489-106">**AzureRmApplicationGateway** Cmdlet 會停止應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6a489-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="6a489-107">示例</span><span class="sxs-lookup"><span data-stu-id="6a489-107">EXAMPLES</span></span>

### <span data-ttu-id="6a489-108">範例1：停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="6a489-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="6a489-109">這個命令會停止儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6a489-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="6a489-110">參數</span><span class="sxs-lookup"><span data-stu-id="6a489-110">PARAMETERS</span></span>

### <span data-ttu-id="6a489-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a489-111">-ApplicationGateway</span></span>
<span data-ttu-id="6a489-112">指定此 Cmdlet 停止的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6a489-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6a489-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a489-113">-DefaultProfile</span></span>
<span data-ttu-id="6a489-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a489-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a489-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a489-115">CommonParameters</span></span>
<span data-ttu-id="6a489-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a489-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a489-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a489-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a489-118">輸入</span><span class="sxs-lookup"><span data-stu-id="6a489-118">INPUTS</span></span>

### <span data-ttu-id="6a489-119">System.object</span><span class="sxs-lookup"><span data-stu-id="6a489-119">System.String</span></span>

## <span data-ttu-id="6a489-120">輸出</span><span class="sxs-lookup"><span data-stu-id="6a489-120">OUTPUTS</span></span>

### <span data-ttu-id="6a489-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6a489-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a489-122">筆記</span><span class="sxs-lookup"><span data-stu-id="6a489-122">NOTES</span></span>

## <span data-ttu-id="6a489-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a489-123">RELATED LINKS</span></span>

[<span data-ttu-id="6a489-124">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a489-124">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="6a489-125">新-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a489-125">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="6a489-126">移除-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a489-126">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="6a489-127">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a489-127">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="6a489-128">開始-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a489-128">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


