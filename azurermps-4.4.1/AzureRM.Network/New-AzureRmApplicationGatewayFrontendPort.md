---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: c12034d41eeecbba2146592247a034f99af94c89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626253"
---
# <span data-ttu-id="35aa1-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="35aa1-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="35aa1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="35aa1-103">為應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="35aa1-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35aa1-104">句法</span><span class="sxs-lookup"><span data-stu-id="35aa1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35aa1-105">說明</span><span class="sxs-lookup"><span data-stu-id="35aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="35aa1-106">**新的-AzureRmApplicationGatewayFrontendPort** Cmdlet 會為 Azure 應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="35aa1-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="35aa1-107">示例</span><span class="sxs-lookup"><span data-stu-id="35aa1-107">EXAMPLES</span></span>

### <span data-ttu-id="35aa1-108">Example1：建立前端埠</span><span class="sxs-lookup"><span data-stu-id="35aa1-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="35aa1-109">這個命令會在埠80上建立一個名為 FrontEndPort01 的前端埠，並將結果儲存在名為 $FrontEndPort 的變數中。</span><span class="sxs-lookup"><span data-stu-id="35aa1-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="35aa1-110">參數</span><span class="sxs-lookup"><span data-stu-id="35aa1-110">PARAMETERS</span></span>

### <span data-ttu-id="35aa1-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="35aa1-111">-Name</span></span>
<span data-ttu-id="35aa1-112">指定此 Cmdlet 所建立之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="35aa1-112">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="35aa1-113">-埠</span><span class="sxs-lookup"><span data-stu-id="35aa1-113">-Port</span></span>
<span data-ttu-id="35aa1-114">指定前端埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="35aa1-114">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35aa1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35aa1-115">-DefaultProfile</span></span>
<span data-ttu-id="35aa1-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35aa1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35aa1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35aa1-117">CommonParameters</span></span>
<span data-ttu-id="35aa1-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35aa1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35aa1-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35aa1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35aa1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="35aa1-120">INPUTS</span></span>

### <span data-ttu-id="35aa1-121">System.object</span><span class="sxs-lookup"><span data-stu-id="35aa1-121">System.String</span></span>

## <span data-ttu-id="35aa1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="35aa1-122">OUTPUTS</span></span>

### <span data-ttu-id="35aa1-123">PSApplicationGatewayFrontendPort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="35aa1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="35aa1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="35aa1-124">NOTES</span></span>

## <span data-ttu-id="35aa1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="35aa1-125">RELATED LINKS</span></span>

[<span data-ttu-id="35aa1-126">附加 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="35aa1-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="35aa1-127">AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="35aa1-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="35aa1-128">移除-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="35aa1-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="35aa1-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="35aa1-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


