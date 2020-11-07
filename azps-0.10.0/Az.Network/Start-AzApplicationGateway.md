---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 8c37ed72659c8b5ab00d54a7ecbe9622cb9f553b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795370"
---
# <span data-ttu-id="335a3-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="335a3-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="335a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="335a3-102">SYNOPSIS</span></span>
<span data-ttu-id="335a3-103">啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="335a3-103">Starts an application gateway.</span></span>

## <span data-ttu-id="335a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="335a3-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="335a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="335a3-105">DESCRIPTION</span></span>
<span data-ttu-id="335a3-106">**AzApplicationGateway** Cmdlet 會啟動 Azure 應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="335a3-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="335a3-107">示例</span><span class="sxs-lookup"><span data-stu-id="335a3-107">EXAMPLES</span></span>

### <span data-ttu-id="335a3-108">Example1：啟動應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="335a3-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="335a3-109">這個命令會啟動儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="335a3-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="335a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="335a3-110">PARAMETERS</span></span>

### <span data-ttu-id="335a3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="335a3-111">-ApplicationGateway</span></span>
<span data-ttu-id="335a3-112">指定此 Cmdlet 啟動的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="335a3-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="335a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335a3-113">-DefaultProfile</span></span>
<span data-ttu-id="335a3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="335a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="335a3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335a3-115">CommonParameters</span></span>
<span data-ttu-id="335a3-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="335a3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335a3-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="335a3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335a3-118">輸入</span><span class="sxs-lookup"><span data-stu-id="335a3-118">INPUTS</span></span>

### <span data-ttu-id="335a3-119">System.object</span><span class="sxs-lookup"><span data-stu-id="335a3-119">System.String</span></span>

## <span data-ttu-id="335a3-120">輸出</span><span class="sxs-lookup"><span data-stu-id="335a3-120">OUTPUTS</span></span>

### <span data-ttu-id="335a3-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="335a3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="335a3-122">筆記</span><span class="sxs-lookup"><span data-stu-id="335a3-122">NOTES</span></span>

## <span data-ttu-id="335a3-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="335a3-123">RELATED LINKS</span></span>

[<span data-ttu-id="335a3-124">停止 AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="335a3-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


