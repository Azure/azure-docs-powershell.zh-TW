---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bcc7335076a0f74c89cede8c6fed66f55d88ec9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902409"
---
# <span data-ttu-id="97ccb-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="97ccb-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="97ccb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="97ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="97ccb-103">為應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="97ccb-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="97ccb-104">語法</span><span class="sxs-lookup"><span data-stu-id="97ccb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97ccb-105">描述</span><span class="sxs-lookup"><span data-stu-id="97ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="97ccb-106">**New-AzApplicationGatewayFrontendPort** Cmdlet 會為 Azure 應用程式閘道建立前端埠。</span><span class="sxs-lookup"><span data-stu-id="97ccb-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="97ccb-107">例子</span><span class="sxs-lookup"><span data-stu-id="97ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="97ccb-108">範例 1：範例1：建立前端埠</span><span class="sxs-lookup"><span data-stu-id="97ccb-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="97ccb-109">此命令在埠 80 上建立名為 FrontEndPort01 的前端埠，並儲存在名為 $FrontEndPort 的變數中。</span><span class="sxs-lookup"><span data-stu-id="97ccb-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="97ccb-110">參數</span><span class="sxs-lookup"><span data-stu-id="97ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="97ccb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ccb-111">-DefaultProfile</span></span>
<span data-ttu-id="97ccb-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="97ccb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97ccb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="97ccb-113">-Name</span></span>
<span data-ttu-id="97ccb-114">指定此 Cmdlet 所建立前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="97ccb-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="97ccb-115">-埠</span><span class="sxs-lookup"><span data-stu-id="97ccb-115">-Port</span></span>
<span data-ttu-id="97ccb-116">指定前端埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="97ccb-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="97ccb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ccb-117">CommonParameters</span></span>
<span data-ttu-id="97ccb-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="97ccb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ccb-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="97ccb-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ccb-120">輸入</span><span class="sxs-lookup"><span data-stu-id="97ccb-120">INPUTS</span></span>

### <span data-ttu-id="97ccb-121">沒有</span><span class="sxs-lookup"><span data-stu-id="97ccb-121">None</span></span>

## <span data-ttu-id="97ccb-122">輸出</span><span class="sxs-lookup"><span data-stu-id="97ccb-122">OUTPUTS</span></span>

### <span data-ttu-id="97ccb-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="97ccb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="97ccb-124">筆記</span><span class="sxs-lookup"><span data-stu-id="97ccb-124">NOTES</span></span>

## <span data-ttu-id="97ccb-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="97ccb-125">RELATED LINKS</span></span>

[<span data-ttu-id="97ccb-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="97ccb-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="97ccb-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="97ccb-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="97ccb-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="97ccb-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="97ccb-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="97ccb-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


