---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: ddfe8b1736ef6c037522815dc81019fadc5b6c1f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794310"
---
# <span data-ttu-id="62b34-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62b34-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="62b34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62b34-102">SYNOPSIS</span></span>
<span data-ttu-id="62b34-103">為應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="62b34-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="62b34-104">句法</span><span class="sxs-lookup"><span data-stu-id="62b34-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b34-105">說明</span><span class="sxs-lookup"><span data-stu-id="62b34-105">DESCRIPTION</span></span>
<span data-ttu-id="62b34-106">**新的-AzApplicationGatewayFrontendPort** Cmdlet 會為 Azure 應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="62b34-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="62b34-107">示例</span><span class="sxs-lookup"><span data-stu-id="62b34-107">EXAMPLES</span></span>

### <span data-ttu-id="62b34-108">Example1：建立前端埠</span><span class="sxs-lookup"><span data-stu-id="62b34-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="62b34-109">這個命令會在埠80上建立一個名為 FrontEndPort01 的前端埠，並將結果儲存在名為 $FrontEndPort 的變數中。</span><span class="sxs-lookup"><span data-stu-id="62b34-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="62b34-110">參數</span><span class="sxs-lookup"><span data-stu-id="62b34-110">PARAMETERS</span></span>

### <span data-ttu-id="62b34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b34-111">-DefaultProfile</span></span>
<span data-ttu-id="62b34-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62b34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62b34-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="62b34-113">-Name</span></span>
<span data-ttu-id="62b34-114">指定此 Cmdlet 所建立之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="62b34-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b34-115">-埠</span><span class="sxs-lookup"><span data-stu-id="62b34-115">-Port</span></span>
<span data-ttu-id="62b34-116">指定前端埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="62b34-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b34-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b34-117">CommonParameters</span></span>
<span data-ttu-id="62b34-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62b34-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b34-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62b34-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b34-120">輸入</span><span class="sxs-lookup"><span data-stu-id="62b34-120">INPUTS</span></span>

### <span data-ttu-id="62b34-121">System.object</span><span class="sxs-lookup"><span data-stu-id="62b34-121">System.String</span></span>

## <span data-ttu-id="62b34-122">輸出</span><span class="sxs-lookup"><span data-stu-id="62b34-122">OUTPUTS</span></span>

### <span data-ttu-id="62b34-123">PSApplicationGatewayFrontendPort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="62b34-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="62b34-124">筆記</span><span class="sxs-lookup"><span data-stu-id="62b34-124">NOTES</span></span>

## <span data-ttu-id="62b34-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="62b34-125">RELATED LINKS</span></span>

[<span data-ttu-id="62b34-126">附加 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62b34-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="62b34-127">AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62b34-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="62b34-128">移除-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62b34-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="62b34-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62b34-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


