---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: b62a41c2c97055f0ef090ed5def3dc771ae3c1ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795465"
---
# <span data-ttu-id="8cfc1-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cfc1-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="8cfc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cfc1-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfc1-103">更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8cfc1-103">Updates an application gateway.</span></span>

## <span data-ttu-id="8cfc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cfc1-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cfc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="8cfc1-105">DESCRIPTION</span></span>
<span data-ttu-id="8cfc1-106">**AzApplicationGateway** Cmdlet 會更新 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8cfc1-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="8cfc1-107">示例</span><span class="sxs-lookup"><span data-stu-id="8cfc1-107">EXAMPLES</span></span>

### <span data-ttu-id="8cfc1-108">範例1：更新應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="8cfc1-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="8cfc1-109">這個命令會使用 $AppGw 變數中的設定來更新應用程式閘道，並將更新的閘道儲存在 $UpdatedAppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="8cfc1-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="8cfc1-110">參數</span><span class="sxs-lookup"><span data-stu-id="8cfc1-110">PARAMETERS</span></span>

### <span data-ttu-id="8cfc1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cfc1-111">-ApplicationGateway</span></span>
<span data-ttu-id="8cfc1-112">指定代表應用程式閘道應該設定之狀態的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="8cfc1-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="8cfc1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cfc1-113">-AsJob</span></span>
<span data-ttu-id="8cfc1-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cfc1-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cfc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfc1-115">-DefaultProfile</span></span>
<span data-ttu-id="8cfc1-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cfc1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cfc1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfc1-117">CommonParameters</span></span>
<span data-ttu-id="8cfc1-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cfc1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfc1-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cfc1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfc1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8cfc1-120">INPUTS</span></span>

### <span data-ttu-id="8cfc1-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cfc1-121">PSApplicationGateway</span></span>
<span data-ttu-id="8cfc1-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8cfc1-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="8cfc1-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8cfc1-123">OUTPUTS</span></span>

### <span data-ttu-id="8cfc1-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8cfc1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8cfc1-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8cfc1-125">NOTES</span></span>

## <span data-ttu-id="8cfc1-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cfc1-126">RELATED LINKS</span></span>

[<span data-ttu-id="8cfc1-127">開始-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cfc1-127">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


