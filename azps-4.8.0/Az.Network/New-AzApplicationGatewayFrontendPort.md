---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128969"
---
# <span data-ttu-id="37509-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="37509-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="37509-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37509-102">SYNOPSIS</span></span>
<span data-ttu-id="37509-103">為應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="37509-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="37509-104">句法</span><span class="sxs-lookup"><span data-stu-id="37509-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37509-105">說明</span><span class="sxs-lookup"><span data-stu-id="37509-105">DESCRIPTION</span></span>
<span data-ttu-id="37509-106">**新的-AzApplicationGatewayFrontendPort** Cmdlet 會為 Azure 應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="37509-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="37509-107">示例</span><span class="sxs-lookup"><span data-stu-id="37509-107">EXAMPLES</span></span>

### <span data-ttu-id="37509-108">範例1： Example1：建立前端埠</span><span class="sxs-lookup"><span data-stu-id="37509-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="37509-109">這個命令會在埠80上建立一個名為 FrontEndPort01 的前端埠，並將結果儲存在名為 $FrontEndPort 的變數中。</span><span class="sxs-lookup"><span data-stu-id="37509-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="37509-110">參數</span><span class="sxs-lookup"><span data-stu-id="37509-110">PARAMETERS</span></span>

### <span data-ttu-id="37509-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37509-111">-DefaultProfile</span></span>
<span data-ttu-id="37509-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37509-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37509-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="37509-113">-Name</span></span>
<span data-ttu-id="37509-114">指定此 Cmdlet 所建立之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="37509-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="37509-115">-埠</span><span class="sxs-lookup"><span data-stu-id="37509-115">-Port</span></span>
<span data-ttu-id="37509-116">指定前端埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="37509-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="37509-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37509-117">CommonParameters</span></span>
<span data-ttu-id="37509-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37509-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37509-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37509-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37509-120">輸入</span><span class="sxs-lookup"><span data-stu-id="37509-120">INPUTS</span></span>

### <span data-ttu-id="37509-121">所有</span><span class="sxs-lookup"><span data-stu-id="37509-121">None</span></span>

## <span data-ttu-id="37509-122">輸出</span><span class="sxs-lookup"><span data-stu-id="37509-122">OUTPUTS</span></span>

### <span data-ttu-id="37509-123">PSApplicationGatewayFrontendPort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="37509-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="37509-124">筆記</span><span class="sxs-lookup"><span data-stu-id="37509-124">NOTES</span></span>

## <span data-ttu-id="37509-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="37509-125">RELATED LINKS</span></span>

[<span data-ttu-id="37509-126">附加 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="37509-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="37509-127">AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="37509-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="37509-128">移除-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="37509-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="37509-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="37509-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


