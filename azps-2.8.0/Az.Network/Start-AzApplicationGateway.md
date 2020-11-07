---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: f90e35e0b8a88d7fa7b5089adf205bf6fe14e18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791530"
---
# <span data-ttu-id="232f6-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="232f6-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="232f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="232f6-102">SYNOPSIS</span></span>
<span data-ttu-id="232f6-103">啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="232f6-103">Starts an application gateway.</span></span>

## <span data-ttu-id="232f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="232f6-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="232f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="232f6-105">DESCRIPTION</span></span>
<span data-ttu-id="232f6-106">**AzApplicationGateway** Cmdlet 會啟動 Azure 應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="232f6-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="232f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="232f6-107">EXAMPLES</span></span>

### <span data-ttu-id="232f6-108">Example1：啟動應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="232f6-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="232f6-109">這個命令會啟動儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="232f6-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="232f6-110">參數</span><span class="sxs-lookup"><span data-stu-id="232f6-110">PARAMETERS</span></span>

### <span data-ttu-id="232f6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="232f6-111">-ApplicationGateway</span></span>
<span data-ttu-id="232f6-112">指定此 Cmdlet 啟動的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="232f6-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="232f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232f6-113">-DefaultProfile</span></span>
<span data-ttu-id="232f6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="232f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="232f6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232f6-115">CommonParameters</span></span>
<span data-ttu-id="232f6-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="232f6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232f6-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="232f6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232f6-118">輸入</span><span class="sxs-lookup"><span data-stu-id="232f6-118">INPUTS</span></span>

### <span data-ttu-id="232f6-119">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="232f6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="232f6-120">輸出</span><span class="sxs-lookup"><span data-stu-id="232f6-120">OUTPUTS</span></span>

### <span data-ttu-id="232f6-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="232f6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="232f6-122">筆記</span><span class="sxs-lookup"><span data-stu-id="232f6-122">NOTES</span></span>

## <span data-ttu-id="232f6-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="232f6-123">RELATED LINKS</span></span>

[<span data-ttu-id="232f6-124">停止 AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="232f6-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


