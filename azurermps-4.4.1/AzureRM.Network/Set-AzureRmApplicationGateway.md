---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: f755c08b880a9ec97315931843d6dca6f5fc3229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457536"
---
# <span data-ttu-id="9e63f-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e63f-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="9e63f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e63f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e63f-103">更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9e63f-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e63f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e63f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e63f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e63f-105">DESCRIPTION</span></span>
<span data-ttu-id="9e63f-106">**AzureRmApplicationGateway** Cmdlet 會更新 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9e63f-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="9e63f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e63f-107">EXAMPLES</span></span>

### <span data-ttu-id="9e63f-108">範例1：更新應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="9e63f-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9e63f-109">這個命令會使用 $AppGw 變數中的設定來更新應用程式閘道，並將更新的閘道儲存在 $UpdatedAppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="9e63f-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="9e63f-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e63f-110">PARAMETERS</span></span>

### <span data-ttu-id="9e63f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e63f-111">-ApplicationGateway</span></span>
<span data-ttu-id="9e63f-112">指定代表應用程式閘道應該設定之狀態的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="9e63f-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="9e63f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e63f-113">-DefaultProfile</span></span>
<span data-ttu-id="9e63f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e63f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e63f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e63f-115">CommonParameters</span></span>
<span data-ttu-id="9e63f-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e63f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e63f-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e63f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e63f-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9e63f-118">INPUTS</span></span>

### <span data-ttu-id="9e63f-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e63f-119">PSApplicationGateway</span></span>
<span data-ttu-id="9e63f-120">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9e63f-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="9e63f-121">輸出</span><span class="sxs-lookup"><span data-stu-id="9e63f-121">OUTPUTS</span></span>

### <span data-ttu-id="9e63f-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e63f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e63f-123">筆記</span><span class="sxs-lookup"><span data-stu-id="9e63f-123">NOTES</span></span>

## <span data-ttu-id="9e63f-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e63f-124">RELATED LINKS</span></span>

[<span data-ttu-id="9e63f-125">開始-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e63f-125">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


