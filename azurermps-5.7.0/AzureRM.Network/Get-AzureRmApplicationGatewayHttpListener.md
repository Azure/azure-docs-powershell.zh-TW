---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: a28aa5b0f611c8014ae2849e0dee6fe48aedfbe1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451423"
---
# <span data-ttu-id="4aa05-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4aa05-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4aa05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4aa05-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa05-103">取得應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="4aa05-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aa05-104">句法</span><span class="sxs-lookup"><span data-stu-id="4aa05-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa05-105">說明</span><span class="sxs-lookup"><span data-stu-id="4aa05-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa05-106">**AzureRmApplicationGatewayHttpListener** Cmdlet 會取得應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="4aa05-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="4aa05-107">示例</span><span class="sxs-lookup"><span data-stu-id="4aa05-107">EXAMPLES</span></span>

### <span data-ttu-id="4aa05-108">範例1：取得特定的 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="4aa05-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="4aa05-109">這個命令會取得名為 Listener01 的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="4aa05-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="4aa05-110">範例2：取得 HTTP 偵聽程式清單</span><span class="sxs-lookup"><span data-stu-id="4aa05-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="4aa05-111">這個命令會取得 HTTP 偵聽程式的清單。</span><span class="sxs-lookup"><span data-stu-id="4aa05-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="4aa05-112">參數</span><span class="sxs-lookup"><span data-stu-id="4aa05-112">PARAMETERS</span></span>

### <span data-ttu-id="4aa05-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4aa05-113">-ApplicationGateway</span></span>
<span data-ttu-id="4aa05-114">指定包含 HTTP 偵聽程式的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4aa05-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="4aa05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa05-115">-DefaultProfile</span></span>
<span data-ttu-id="4aa05-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4aa05-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aa05-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4aa05-117">-Name</span></span>
<span data-ttu-id="4aa05-118">指定此 Cmdlet 所取得之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aa05-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa05-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa05-119">CommonParameters</span></span>
<span data-ttu-id="4aa05-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4aa05-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa05-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4aa05-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa05-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4aa05-122">INPUTS</span></span>

### <span data-ttu-id="4aa05-123">System.object</span><span class="sxs-lookup"><span data-stu-id="4aa05-123">System.String</span></span>

## <span data-ttu-id="4aa05-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4aa05-124">OUTPUTS</span></span>

### <span data-ttu-id="4aa05-125">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4aa05-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4aa05-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4aa05-126">NOTES</span></span>

## <span data-ttu-id="4aa05-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4aa05-127">RELATED LINKS</span></span>

[<span data-ttu-id="4aa05-128">附加 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4aa05-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4aa05-129">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4aa05-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4aa05-130">移除-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4aa05-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4aa05-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4aa05-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


