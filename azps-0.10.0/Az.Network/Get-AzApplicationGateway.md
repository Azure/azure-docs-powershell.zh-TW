---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794489"
---
# <span data-ttu-id="3c093-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c093-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="3c093-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c093-102">SYNOPSIS</span></span>
<span data-ttu-id="3c093-103">取得應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3c093-103">Gets an application gateway.</span></span>

## <span data-ttu-id="3c093-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c093-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c093-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c093-105">DESCRIPTION</span></span>
<span data-ttu-id="3c093-106">**AzApplicationGateway** Cmdlet 會取得應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3c093-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="3c093-107">示例</span><span class="sxs-lookup"><span data-stu-id="3c093-107">EXAMPLES</span></span>

### <span data-ttu-id="3c093-108">範例1：取得指定的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="3c093-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3c093-109">這個命令會取得名為 [ResourceGroup01] 的 [ApplicationGateway01] 資源群組的應用程式閘道，並將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="3c093-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="3c093-110">範例2：取得資源群組中的應用程式閘道清單</span><span class="sxs-lookup"><span data-stu-id="3c093-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3c093-111">這個命令會取得名為 ResourceGroup01 之資源群組中所有應用程式閘道的清單，並將它儲存在 $AppGwList 變數中。</span><span class="sxs-lookup"><span data-stu-id="3c093-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="3c093-112">範例3：取得訂閱中的應用程式閘道清單</span><span class="sxs-lookup"><span data-stu-id="3c093-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

<span data-ttu-id="3c093-113">這個命令會取得訂閱中所有應用程式閘道的清單，並將它儲存在 $AppGwList 變數中。</span><span class="sxs-lookup"><span data-stu-id="3c093-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="3c093-114">參數</span><span class="sxs-lookup"><span data-stu-id="3c093-114">PARAMETERS</span></span>

### <span data-ttu-id="3c093-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c093-115">-DefaultProfile</span></span>
<span data-ttu-id="3c093-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c093-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c093-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c093-117">-Name</span></span>
<span data-ttu-id="3c093-118">指定此 Cmdlet 所取得之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c093-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c093-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c093-119">-ResourceGroupName</span></span>
<span data-ttu-id="3c093-120">指定包含應用程式閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c093-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c093-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c093-121">CommonParameters</span></span>
<span data-ttu-id="3c093-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c093-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c093-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c093-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c093-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3c093-124">INPUTS</span></span>

### <span data-ttu-id="3c093-125">System.object</span><span class="sxs-lookup"><span data-stu-id="3c093-125">System.String</span></span>

## <span data-ttu-id="3c093-126">輸出</span><span class="sxs-lookup"><span data-stu-id="3c093-126">OUTPUTS</span></span>

### <span data-ttu-id="3c093-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c093-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3c093-128">筆記</span><span class="sxs-lookup"><span data-stu-id="3c093-128">NOTES</span></span>

## <span data-ttu-id="3c093-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c093-129">RELATED LINKS</span></span>

[<span data-ttu-id="3c093-130">停止 AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c093-130">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


